# Hello-world
This is a project
#include<stdio.h>
#include<string.h>

int main()
{
	int result = 1;
	int i;
	int count = 0;
	char Text[128] = { '\0' };
	char tt[128] = { '\0' };
	while (1) {
		if (result == 1) {
			printf("请输入要加密的密码:");
			scanf_s("%s", &Text);
			count = strlen(Text);
			for (i = 0; i < count; i++) {
				tt[i] = Text[i] + i + 5;
			}
			tt[i] = '\0';
			printf("加密后的明文是:%s\n", tt);
		}
		else if (result == 2) {
			count = strlen(Text);
			for (i = 0; i < count; i++) {
				Text[i] = tt[i] - i - 5;
			}
			Text[i] = '\0';
			printf("解密后的明文是:%s\n", Text);
		}
		else if (result == 3) {
			break;
		}
		else {
			printf("请输入密码:");
		}
		printf("输入1加密新的密码\n输入2对刚加密的密码进行解密\n情人3退出系统\n");
		printf("请输入密码:");
		scanf_s("%d", &result);
	}
	return 0;
}
