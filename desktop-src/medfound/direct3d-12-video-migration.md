---
description: Descrive le API video di Direct3D 12 equivalenti alle versioni precedenti.
ms.assetid: ''
title: Video sulla migrazione a Direct3D 12.
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 56af5ba7845db5e1d4bfeac280cae9235f47ebe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305404"
---
# <a name="migrating-to-direct3d-12-video"></a>Video sulla migrazione a Direct3D 12.

Questo articolo descrive le API video Direct3D 12 usate per implementare le funzionalità disponibili nelle versioni precedenti. Per migliorare le prestazioni e l'usabilità delle funzionalità video con priorità più elevata, alcune funzionalità di Direct3D 11 sono completamente o parzialmente non supportate in Direct3D 12. 

Si noti che, sebbene la maggior parte delle funzionalità di Direct3D 11 siano disponibili in Direct3D 12, la progettazione delle API è cambiata, quindi in molti casi non esiste un mapping uno-a-uno delle API tra i due set di API. Le tabelle seguenti hanno lo scopo di puntare verso le API più rilevanti in Direct3D 12 per ogni API Direct3D 11, ma il modo in cui si usano le nuove API potrebbe essere significativamente diverso. Ad esempio:

- Per decodificare un frame di video, le API video Direct3D 11 usano le chiamate a [DecoderBeginFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe), [GetDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer), [SubmitDecoderBuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers)e [DecoderEndFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe). Con Direct3D 12 viene usato un singolo metodo,  [ID3D12VideoDecodeCommandList::D ecodeframe](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe).
- Per l'elaborazione video, Direct3D 11 forniva singoli metodi per l'impostazione dei diversi valori di configurazione, ad esempio [VideoProcessorSetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) e [VideoProcessorSetOutputAlphaFillMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode). In Direct3D 12, questi valori vengono impostati durante la creazione del processore video, nella chiamata a [ID3D12VideoDevice:: CreateVideoProcessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)o quando il frame viene elaborato con una chiamata a [ID3D12VideoProcessCommandList1::P rocessframes1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1).





## <a name="id3d11videocontext"></a>ID3D11VideoContext
Fornisce la funzionalità video di un dispositivo Direct3D 11, inclusa la decodifica video, l'elaborazione video, la protezione del contenuto basata su GPU e la crittografia/decrittografia dei video. Questa funzionalità è parzialmente implementata per Direct3D 12.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [ConfigureAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) | Non implementato |
| [DecoderBeginFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)| [ID3D12VideoDecodeCommandList::D ecodeframe](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe),  [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument), [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream), [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames) |
| [DecoderEndFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) | [ID3D12VideoDecodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videodecodecommandlist) |
| [DecoderExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderextension) | Non implementato. |
| [DecryptionBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)  | Non implementato. |
| [EncryptionBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt) | Non implementato. |
| [FinishSessionKeyRefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh) | Non implementato. |
| [GetDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) | Non implementato. I buffer compressi sono gestiti da app in Direct3D 12. |
| [GetEncryptionBltKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey) | Non implementato. | 
| [NegotiateAuthenticatedChannelKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) | Non implementato. |
| [NegotiateCryptoSessionKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) | Non implementato. |
| [QueryAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel) | Non implementato. |
| [ReleaseDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer) | Non implementato. I buffer compressi sono gestiti da app in Direct3D 12. |
| [StartSessionKeyRefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh) | Non implementato |
| [SubmitDecoderBuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) | [ID3D12VideoDecodeCommandList::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [VideoProcessorBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt) | [ID3D12VideoProcessCommandList1::P rocessFrames1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputalphafillmode) [VideoProcessorSetOutputAlphaFillMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode) VideoProcessorGetOutputAlphaFillMode | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. AlphaFillMode](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputbackgroundcolor) [VideoProcessorSetOutputBackgroundColor](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputbackgroundcolor) VideoProcessorGetOutputBackgroundColor | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. BackgroundColor](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputcolorspace) [VideoProcessorSetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) VideoProcessorGetOutputColorSpace | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. ColorSpace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputconstriction) [VideoProcessorSetOutputConstriction](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputconstriction) VideoProcessorGetOutputConstriction | Non implementato. Il software DRM non è supportato. |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputextension) [VideoProcessorSetOutputExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputextension) VideoProcessorGetOutputExtension | Non implementato. |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputstereomode) [VideoProcessorSetOutputStereoMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputstereomode) VideoProcessorGetOutputStereoMode | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. EnableStereo](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputtargetrect) [VideoProcessorSetOutputTargetRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputtargetrect) VideoProcessorGetOutputTargetRect | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS. TargetRectangle](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamalpha) [VideoProcessorSetStreamAlpha](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamalpha) VideoProcessorGetStreamAlpha  | [D3D12_VIDEO_PROCESS_ALPHA_BLENDING. Alfa](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamautoprocessingmode) [VideoProcessorSetStreamAutoProcessingMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamautoprocessingmode) VideoProcessorGetStreamAutoProcessingMode | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. EnableAutoProcessing](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamcolorspace) [VideoProcessorSetStreamColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamcolorspace) VideoProcessorGetStreamColorSpace | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. ColorSpace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamdestrect) [VideoProcessorSetStreamDestRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamdestrect) VideoProcessorGetStreamDestRect | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. DestinationRectangle](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamextension) [VideoProcessorSetStreamExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamextension) VideoProcessorGetStreamExtension | Non implementato. |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamfilter) [VideoProcessorSetStreamFilter](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamfilter) VideoProcessorGetStreamFilter | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. FilterFlags](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamframeformat) [VideoProcessorSetStreamFrameFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamframeformat) VideoProcessorGetStreamFrameFormat | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Formato](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamlumakey) [VideoProcessorSetStreamLumaKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamlumakey) VideoProcessorGetStreamLumaKey | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. LumaKey](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamoutputrate) [VideoProcessorSetStreamOutputRate](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamoutputrate) VideoProcessorGetStreamOutputRate | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. FrameRate](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampalette) [VideoProcessorSetStreamPalette](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampalette) VideoProcessorGetStreamPalette | Non implementato |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampixelaspectratio) [VideoProcessorSetStreamPixelAspectRatio](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampixelaspectratio) VideoProcessorGetStreamPixelAspectRatio | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Trasformazione](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamrotation) [VideoProcessorSetStreamRotation](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamrotation) VideoProcessorGetStreamRotation | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Trasformazione](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamsourcerect) [VideoProcessorSetStreamSourceRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamsourcerect) VideoProcessorGetStreamSourceRect | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Trasformazione](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamstereoformat) [VideoProcessorSetStreamStereoFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat) VideoProcessorGetStreamStereoFormat | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Trasformazione](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videocontext1"></a>ID3D11VideoContext1

Fornisce funzionalità video estese di un dispositivo Direct3D 11, tra cui DRM hardware, miglioramenti all'utilizzo della superficie, altre funzionalità di elaborazione video. Questa funzionalità è implementata per Direct3D 12 tramite nuove interfacce.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| CheckCryptoSessionStatus | TBD | 
| [DecoderEnableDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [DecoderUpdateDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderenabledownsampling) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [GetDataForNewHardwareKey](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-getdatafornewhardwarekey) | TBD |
| [SubmitDecoderBuffers1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-submitdecoderbuffers1) | [ID3D12VideoDecodeCommandList::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [VideoProcessorGetBehaviorHints](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetbehaviorhints) | TBD |
| [](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputcolorspace1) [VideoProcessorSetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputcolorspace1) VideoProcessorGetOutputColorSpace1 | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. ColorSpace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputshaderusage) [VideoProcessorSetOutputShaderUsage](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputshaderusage) VideoProcessorGetOutputShaderUsage | TBD |
| [](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreamcolorspace1) [VideoProcessorSetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreamcolorspace1) VideoProcessorGetStreamColorSpace1 | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. ColorSpace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreammirror) [VideoProcessorSetStreamMirror](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreammirror) VideoProcessorGetStreamMirror | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Trasformazione](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videodecoder"></a>ID3D11VideoDecoder

Rappresenta un decodificatore video con accelerazione hardware per Direct3D 11. Si tratta di un'interfaccia wrapper intorno a [ID3D11VideoContext](/windows/win32/api/d3d11/nn-d3d11-id3d11videocontext) che espone la funzionalità di decodifica effettiva. Non è disponibile un'API equivalente per il video Direct3D 12.


## <a name="id3d11videodecoderoutputview"></a>ID3D11VideoDecoderOutputView

Identifica le superfici di output a cui è possibile accedere durante la decodifica video. In Direct3D 12, l'interfaccia [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor) USA direttamente gli oggetti [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) .

## <a name="id3d11videodevice"></a>ID3D11VideoDevice

Fornisce la decodifica video e le funzionalità di elaborazione video di un dispositivo Direct3D 11. Questo è il punto di ingresso principale per creare il dispositivo del decodificatore video e la sessione di crittografia e per l'elaborazione video, le funzionalità, i profili e così via. Questa funzionalità è parzialmente implementata per Direct3D 12.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [CheckCryptoKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) | Non implementato. |
| [CheckVideoDecoderFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) | [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [CreateAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) | Non implementato. |
| [CreateCryptoSession](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) | Non implementato. |
| [CreateVideoDecoder](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) | [ID3D12VideoDevice:: CreateVideoDecoder](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder)  [ID3D12VideoDevice:: CreateVideoDecoderHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) |
| [CreateVideoDecoderOutputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [CreateVideoProcessor](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor) | [ID3D12VideoDevice::CreateVideoProcessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)  |
| [CreateVideoProcessorEnumerator](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator) | N/D |
| [CreateVideoProcessorInputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorinputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [CreateVideoProcessorOutputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessoroutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [GetContentProtectionCaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps) | TBD
| [GetVideoDecoderConfig](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) | In Direct3D 12 è supportata solo la modalità VLD. [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [GetVideoDecoderConfigCount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) | N/D |
| [GetVideoDecoderProfile](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [GetVideoDecoderProfileCount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES. ProfileCount](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [SetPrivateData](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedata) | [ID3D12Object::SetPrivateData](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedata) |
| [SetPrivateDataInterface](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedatainterface) | [ID3D12Object::SetPrivateDataInterface](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedatainterface) |

## <a name="id3d11videodevice1"></a>ID3D11VideoDevice1

Fornisce funzionalità estese di decodifica video e elaborazione video di un dispositivo Direct3D 11, incluse altre estensioni, DRM hardware, decodifica sottocampionando, funzionalità di decodificatore video e così via. Questa funzionalità è implementata per Direct3D 12.

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [CheckVideoDecoderDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-checkvideodecoderdownsampling) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [GetCryptoSessionPrivateDataSize](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getcryptosessionprivatedatasize) | TBD |
| [GetVideoDecoderCaps](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getvideodecodercaps) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [RecommendVideoDecoderDownsampleParameters](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-recommendvideodecoderdownsampleparameters) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |


## <a name="id3d11videoprocessor"></a>ID3D11VideoProcessor

Rappresenta un processore video per Direct3D 11. Questa funzionalità è implementata per Direct3D 12 in [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor)

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [GetContentDesc](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getcontentdesc)| Non implementato |
| [GetRateConversionCaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getrateconversioncaps) | Non implementato |


## <a name="id3d11videoprocessorenumerator-and-id3d11videoprocessorenumerator1"></a>ID3D11VideoProcessorEnumerator e ID3D11VideoProcessorEnumerator1

Enumera le funzionalità del processore video di un dispositivo Direct3D 11.
In Direct3D 12 la funzionalità di enumerazione viene sostituita da [ID3D12VideoDevice:: CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport). 

##  <a name="id3d11videoprocessorinputview"></a>ID3D11VideoProcessorInputView

Identifica le aree di input a cui è possibile accedere durante l'elaborazione video.
In Direct3D 12 questa operazione viene sostituita da ID3D12Texture2D.

##  <a name="id3d11videoprocessoroutputview"></a>ID3D11VideoProcessorOutputView

Identifica le superfici di output a cui è possibile accedere durante l'elaborazione video.
In Direct3D 12 questa operazione viene sostituita da ID3D12Texture2D.

## <a name="id3d11authenticatedchannel"></a>ID3D11AuthenticatedChannel

Fornisce un canale di comunicazione protetto con il driver di grafica o il runtime di Microsoft Direct3D. Questa funzionalità non è implementata per il video Direct3D 12.

##  <a name="id3d11cryptosession"></a>ID3D11CryptoSession

Rappresenta una sessione di crittografia. Usato per gli scenari di DRM software e hardware. Non esiste un'API pubblica equivalente per il video Direct3D 12.

## <a name="related-topics"></a>Argomenti correlati

[API video Direct3D 12](direct3d-12-video-apis.md)


 

 




