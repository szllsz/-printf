嵌入式printf
需将下述代码按需添加进main.c以作串口重定向
int _putchar(int ch){
	uint8_t c=ch;
	HAL_UART_Transmit(&huart1, &c, 1, 1000);
	return ch;
}
