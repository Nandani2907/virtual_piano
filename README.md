# virtual_piano
#include <stdio.h>
#include <stdlib.h>
#include <windows.h>  // for Beep() and Sleep()

int main() {
    char ch;
    printf("\nPress keys to play piano: A, S, D, F, G, H, J, K, L\n");
    printf("Press Q to quit.\n");

    while (1) {
        ch = getchar(); // get character without Enter
        if (ch == 'q' || ch == 'Q')
            break;

        switch (ch) {
            case 'A': case 'a': Beep(240, 150); break;
            case 'S': case 's': Beep(270, 150); break;
            case 'D': case 'd': Beep(300, 150); break;
            case 'F': case 'f': Beep(320, 150); break;
            case 'G': case 'g': Beep(360, 150); break;
            case 'H': case 'h': Beep(400, 150); break;
            case 'J': case 'j': Beep(450, 150); break;
            case 'K': case 'k': Beep(500, 150); break;
            case 'L': case 'l': Beep(600, 150); break;
            default: break;
        }
    }
    return 0;
}
