#Mini piano program

#include <stdio.h>
#include <conio.h>   // for getch()
#include <windows.h> // for Beep() and Sleep()

int main() {
    char ch;
    printf("Mini Piano Program 🎶\n");
    printf("Press keys A–L to play notes.\n");
    printf("Press Z, X, C, V, B, N, M for higher notes.\n");
    printf("Press Q to quit.\n\n");

    while (1) {
        ch = getch(); // get character without Enter

        if (ch == 'q' || ch == 'Q') {
            printf("\nExiting... Goodbye!\n");
            break;
        }

        switch (ch) {
            case 'a': case 'A': Beep(261, 200); printf("C\n"); break;   // C
            case 's': case 'S': Beep(293, 200); printf("D\n"); break;   // D
            case 'd': case 'D': Beep(329, 200); printf("E\n"); break;   // E
            case 'f': case 'F': Beep(349, 200); printf("F\n"); break;   // F
            case 'g': case 'G': Beep(392, 200); printf("G\n"); break;   // G
            case 'h': case 'H': Beep(440, 200); printf("A\n"); break;   // A
            case 'j': case 'J': Beep(493, 200); printf("B\n"); break;   // B
            case 'k': case 'K': Beep(523, 200); printf("C (High)\n"); break; // C5
            case 'l': case 'L': Beep(587, 200); printf("D (High)\n"); break; // D5

            // Higher octave (Z–M keys)
            case 'z': case 'Z': Beep(659, 200); printf("E (High)\n"); break; // E5
            case 'x': case 'X': Beep(698, 200); printf("F (High)\n"); break; // F5
            case 'c': case 'C': Beep(784, 200); printf("G (High)\n"); break; // G5
            case 'v': case 'V': Beep(880, 200); printf("A (High)\n"); break; // A5
            case 'b': case 'B': Beep(987, 200); printf("B (High)\n"); break; // B5
            case 'n': case 'N': Beep(1046, 200); printf("C6\n"); break;      // C6
            case 'm': case 'M': Beep(1174, 200); printf("D6\n"); break;      // D6

            default:
                printf("Invalid key! Press A–L or Z–M.\n");
                break;
        }
    }

    return 0;
}
