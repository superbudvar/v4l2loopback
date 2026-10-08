obj-m		:= v4l2loopback.o

# Enable SPLIT_DEVICES so the #ifdef blocks in v4l2loopback.c are compiled in.
# With SPLIT_DEVICES and split_mode=1, each logical loopback device creates a
# pair of kernel video devices: an OUTPUT-only node (for the writer, e.g.
# pyvirtualcam) and a CAPTURE-only node (for the reader, e.g. Chrome).  The two
# share the same frame buffer so frames written to OUTPUT are immediately
# readable from CAPTURE.
ccflags-y	+= -DSPLIT_DEVICES
