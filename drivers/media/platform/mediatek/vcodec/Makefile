# SPDX-License-Identifier: GPL-2.0

obj-$(CONFIG_VIDEO_MEDIATEK_VCODEC) += mtk-vcodec-dec.o \
				       mtk-vcodec-enc.o \
				       mtk-vcodec-common.o \
				       mtk-vcodec-dec-hw.o

mtk-vcodec-dec-y := vdec/vdec_h264_if.o \
		vdec/vdec_vp8_if.o \
		vdec/vdec_vp8_req_if.o \
		vdec/vdec_vp9_if.o \
		vdec/vdec_vp9_req_lat_if.o \
		vdec/vdec_av1_req_lat_if.o \
		vdec/vdec_h264_req_if.o \
		vdec/vdec_h264_req_common.o \
		vdec/vdec_h264_req_multi_if.o \
		vdec/vdec_hevc_req_multi_if.o \
		mtk_vcodec_dec_drv.o \
		vdec_drv_if.o \
		vdec_vpu_if.o \
		vdec_msg_queue.o \
		mtk_vcodec_dec.o \
		mtk_vcodec_dec_stateful.o \
		mtk_vcodec_dec_stateless.o \
		mtk_vcodec_dec_pm.o \

mtk-vcodec-dec-hw-y := mtk_vcodec_dec_hw.o

mtk-vcodec-enc-y := venc/venc_vp8_if.o \
		venc/venc_h264_if.o \
		mtk_vcodec_enc.o \
		mtk_vcodec_enc_drv.o \
		mtk_vcodec_enc_pm.o \
		venc_drv_if.o \
		venc_vpu_if.o \


mtk-vcodec-common-y := mtk_vcodec_intr.o \
		mtk_vcodec_util.o \
		mtk_vcodec_fw.o \

ifneq ($(CONFIG_VIDEO_MEDIATEK_VCODEC_VPU),)
mtk-vcodec-common-y += mtk_vcodec_fw_vpu.o
endif

ifneq ($(CONFIG_VIDEO_MEDIATEK_VCODEC_SCP),)
mtk-vcodec-common-y += mtk_vcodec_fw_scp.o
endif

ifneq ($(CONFIG_DEBUG_FS),)
obj-$(CONFIG_VIDEO_MEDIATEK_VCODEC) += mtk-vcodec-dbgfs.o

mtk-vcodec-dbgfs-y := mtk_vcodec_dbgfs.o
endif