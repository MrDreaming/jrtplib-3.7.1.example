CC_ARM := arm-none-linux-gnueabi-g++
CC_GCC := g++

INCLUDE_PATH := -I/home/zzy/src/jrtplib/src/jthread-1.2.1/_install/include/jthread 
INCLUDE_PATH += -I/home/zzy/src/jrtplib/src/jrtplib-3.7.1/_install/include/jrtplib3 

LOCAL_LDFLAGS_ARM := ./lib_arm/libjrtp.a 
LOCAL_LDFLAGS_ARM += ./lib_arm/libjthread.a

LOCAL_LDFLAGS_GCC := ./lib_gcc/libjrtp.a 
LOCAL_LDFLAGS_GCC += ./lib_gcc/libjthread.a

out:
	$(CC_GCC) example1.cpp -o send.out $(INCLUDE_PATH) $(LOCAL_LDFLAGS_GCC) -lpthread
	$(CC_ARM) example4.cpp -o recv.out $(INCLUDE_PATH) $(LOCAL_LDFLAGS_ARM) -lpthread
	
clean:
	-rm -rf *.out
	