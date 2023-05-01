#include <stdio.h>
#include <string.h>

int processString(char str[]) {
    int len = strlen(str);
    int spaceIndex = -1;
    for(int i=0; i<len; i++) {
        if(str[i] == ' ') {
            spaceIndex = i;
            break;
        }
    }
    if(spaceIndex == -1) {
        printf("Invalid input string\n");
        return 0;
    }
    str[0] = toupper(str[0]);
    for(int i=1; i<spaceIndex; i++) {
        str[i] = tolower(str[i]);
    }
    for(int i=spaceIndex+1; i<len; i++) {
        str[i] = toupper(str[i]);
    }
    printf("Revised string: %s\n", str);
    int length = strlen(str);
    printf("Length of the string: %d\n", length);
    if(length < 20) {
        return length;
    } else {
        return sizeof(str);
    }
}
int main() {
    char str[100];
    printf("Enter a string with two words: ");
    fgets(str, sizeof(str), stdin);
    str[strcspn(str, "\n")] = 0;
    int result = processString(str);
    printf("Returned value: %d\n", result);
    return 0;
}
