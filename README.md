#include <stdio.h>

int main() {
    char timetable[6][6][30]; // 6 days, 6 periods, each subject max 29 chars + '\0'
    char *days[6] = {"Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"};

    printf("Enter your timetable subjects for each day (6 periods per day):\n\n");

    for(int i = 0; i < 6; i++) {
        printf("%s:\n", days[i]);
        for(int j = 0; j < 6; j++) {
            printf("  Period %d: ", j + 1);
            scanf(" %[^\n]", timetable[i][j]); // Read a full line including spaces
        }
        printf("\n");
    }

    // Display the timetable
    printf("\n------ Your Weekly Timetable ------\n\n");
    for(int i = 0; i < 6; i++) {
        printf("%s:\n", days[i]);
        for(int j = 0; j < 6; j++) {
            printf("  Period %d: %s\n", j + 1, timetable[i][j]);
        }
        printf("\n");
    }

    return 0;
}# Project-2
Timetable generator
