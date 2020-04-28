# some make-foo from stackoverflow, srsly?
root_dir:=$(shell dirname $(realpath $(firstword $(MAKEFILE_LIST))))

GST := gst-launch-1.0
FILE := uri=file://$(root_dir)/../wikipedia-video.ogv

testbild:
	$(GST) videotestsrc pattern=18 ! autovideosink

playbin:
	$(GST) playbin $(FILE)

shout:
	@echo watch on http://localhost:8000/gstreamer.webm
	$(GST) playbin $(FILE) video-sink="shout2send mount=gstreamer.webm"
