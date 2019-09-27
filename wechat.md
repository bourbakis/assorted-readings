'''
NSInvalidArgumentException -[__NSCFString proxySettingsDidChange:]: unrecognized selector sent to instance 0x7f9e61eccc90 
 (
	0   CoreFoundation                      0x000000010d11503c __exceptionPreprocess + 172
	1   libobjc.A.dylib                     0x000000010ea2176e objc_exception_throw + 43
	2   CoreFoundation                      0x000000010d1180ad -[NSObject(NSObject) doesNotRecognizeSelector:] + 205
	3   CoreFoundation                      0x000000010d05dd44 ___forwarding___ + 1028
	4   CoreFoundation                      0x000000010d05d8b8 _CF_forwarding_prep_0 + 120
	5   CoreFoundation                      0x000000010d0d145c __CFNOTIFICATIONCENTER_IS_CALLING_OUT_TO_AN_OBSERVER__ + 12
	6   CoreFoundation                      0x000000010cfc1444 _CFXNotificationPost + 3140
	7   Foundation                          0x000000010bda0881 -[NSNotificationCenter postNotificationName:object:userInfo:] + 66
	8   WeChat                              0x0000000107daf09e WeChat + 4829342
	9   WeChat                              0x0000000107db01ab WeChat + 4833707
	10  WeChat                              0x000000010871441c WeChat + 14681116
	11  WeChat                              0x0000000108723649 WeChat + 14743113
	12  libdispatch.dylib                   0x0000000111927700 _dispatch_call_block_and_release + 12
	13  libdispatch.dylib                   0x0000000111923e73 _dispatch_client_callout + 8
	14  libdispatch.dylib                   0x0000000111934767 _dispatch_main_queue_callback_4CF + 861
	15  CoreFoundation                      0x000000010d068319 __CFRUNLOOP_IS_SERVICING_THE_MAIN_DISPATCH_QUEUE__ + 9
	16  CoreFoundation                      0x000000010d0234af __CFRunLoopRun + 2159
	17  CoreFoundation                      0x000000010d0229f8 CFRunLoopRunSpecific + 296
	18  HIToolbox                           0x0000000110ca056f RunCurrentEventLoopInMode + 235
	19  HIToolbox                           0x0000000110ca02ea ReceiveNextEventCommon + 431
	20  HIToolbox                           0x0000000110ca012b _BlockUntilNextEventMatchingListInModeWithFilter + 71
	21  AppKit                              0x000000010a6f08ab _DPSNextEvent + 978
	22  AppKit                              0x000000010a6efe58 -[NSApplication nextEventMatchingMask:untilDate:inMode:dequeue:] + 346
	23  AppKit                              0x000000010a6e5af3 -[NSApplication run] + 594
	24  WeChat                              0x0000000108414e73 WeChat + 11538035
	25  libdyld.dylib                       0x00000001119795c9 start + 1
)
2019-09-27 16:07:00.402 WeChat[10963:1376633] <WARN> RQD: Note: there is another uncaught exception handler in the project, please check it!
2019-09-27 16:07:00.428 WeChat[10963:1376633] An uncaught exception was raised
libc++abi.dylib: terminate_handler unexpectedly threw an exception
[2]    10963 abort      /Applications/WeChat.app/Contents/MacOS/WeChat

[进程已完成]

'''
