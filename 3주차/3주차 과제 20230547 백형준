#include <stdio.h>
#include <unistd.h>
#include <sys/types.h>
#include <sys/wait.h>

int main() {
	pid_t pid;
	int status;
	pid = fork();
	if (pid > 0) {
		wait(&status);
		int ret = WEXITSTATUS(status);
		printf("1에서 10까지 합한 결과는 %d\n", ret);
		return 0;
	}
	else if (pid ==0) {
		execl("./sum", "./sum", NULL);
	}
}
