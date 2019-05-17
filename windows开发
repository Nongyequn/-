
	HHOOK myhook;
  myhook = SetWindowsHookEx( 
		WH_KEYBOARD_LL, // 监听类型【键盘】
		KeyboardProc,   // 处理函数
		AfxGetInstanceHandle(),      // 当前实例句柄
		0               // 监听窗口句柄(NULL为全局监听)
		); 


LRESULT CALLBACK KeyboardProc(int nCode, WPARAM wParam, LPARAM lParam) 
{   
	PKBDLLHOOKSTRUCT p = (PKBDLLHOOKSTRUCT)lParam;
	const char *info = NULL;
	char text[50], data[20];


	//if (nCode >= 0)
	//{
		if (wParam == WM_KEYDOWN) {
			if (p->vkCode==VK_F2)
			{	
      //相关功能代码
					
          //以下为防止钩子失效进行的操作
					UnhookWindowsHookEx(myhook);
					myhook = SetWindowsHookEx( 
						WH_KEYBOARD_LL, // 监听类型【键盘】
						KeyboardProc,   // 处理函数
						AfxGetInstanceHandle(),      // 当前实例句柄
						0               // 监听窗口句柄(NULL为全局监听)
						); 
            			 
			}
		
		}
			
	/*	else if (wParam == WM_KEYUP)        info = "普通按鍵按下";
		else if (wParam == WM_SYSKEYDOWN)   info = "系統按鍵抬起";
		else if (wParam == WM_SYSKEYUP)     info = "系統按鍵按下";*/


	//}

	return CallNextHookEx(myhook, nCode, wParam, lParam);
} 
