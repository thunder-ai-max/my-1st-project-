#include <stdio.h>
#include <time.h>
#include <windows.h>

int main()
{
    while (1)
    {
        time_t currentTime;
        struct tm *timeInfo;

        // Get the current time
        time(&currentTime);
        timeInfo = localtime(&currentTime);

        // Clear the screen
        system("cls");

        // Print the clock
        printf("\n");https://github.com/thunder-ai-max/my-1st-project-/security
        printf("================================\n");
        printf("            LIVE CLOCK\n");
        printf("================================\n\n");

        printf("             %02d:%02d:%02d\n",
               timeInfo->tm_hour,
               timeInfo->tm_min,
               timeInfo->tm_sec);

        printf("\n================================\n");
        printf("          Running live...\n");

        // Wait for 1 second
        Sleep(1000);
    }

    return 0;
}
