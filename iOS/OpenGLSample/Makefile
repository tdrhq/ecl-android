# This makefile is invoked by Xcode to rebuild libiphone
# We can't invoke ecl directly in the script because it hangs the build process
# (not sure why)

ECL=../../local-install/host/bin/ecl
IOS_SDK_PATH:=$(shell xcodebuild -version -sdk iphonesimulator Path)

all: libopenglsample.a

libopenglsample.a:
	$(ECL) -norc -shell build
	mv libopenglsample.system_ios_universal.a $@

.PHONY: clean libopenglsample.a

clean:
	-rm -rf libopenglsample*.a cache
