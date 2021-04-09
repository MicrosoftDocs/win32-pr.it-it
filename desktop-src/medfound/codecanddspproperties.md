---
description: Costanti IPropertyBag codec e DSP.
ms.assetid: 078b0eea-16dd-4427-b984-9e52a43de559
title: Costanti IPropertyBag codec e DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dcf85e22f55082bb9e2c49041490f4c7aceb2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127995"
---
# <a name="codec-and-dsp-ipropertybag-constants"></a>Costanti IPropertyBag codec e DSP

Esistono due metodi per impostare le proprietà degli oggetti codec e DSP a livello di codice, usando l'interfaccia **IPropertyBag** o l'interfaccia **IPropertyStore** . Le proprietà più comuni sono disponibili tramite entrambe le interfacce. L'uso dell'interfaccia **IPropertyStore** è preferibile rispetto a **IPropertyBag**.



| Costante stringa IPropertyBag          | Chiave della proprietà IPropertyStore                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| g \_ wszAvgFrameRate                    | [\_ASFOVERHEADPERFRAME MFPKEY](mfpkey-asfoverheadperframeproperty.md)                               |
| g \_ wszWMACAvgBytesPerSecond           | [MFPKEY \_ WMAENC \_ AVGBYTESPERSEC](mfpkey-wmaenc-avgbytespersecproperty.md)                          |
| g \_ wszWMACDRCSetting                  | [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md)                                        |
| g \_ wszWMACHiResOutput                 | [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md)                                |
| g \_ wszWMACMusicSpeechClassMode        | [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) |
| g \_ wszWMACOriginalWaveFormat          | [MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT](mfpkey-wmaenc-origwaveformatproperty.md)                          |
| g \_ wszWMACSpeakerConfig               | [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md)                                        |
| g \_ wszWMACVoiceBuffer                 | [MFPKEY \_ WMAVOICE \_ enc \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md)                 |
| g \_ wszWMACVoiceBuffer                 | [MFPKEY \_ WMAVOICE \_ enc \_ EDL](mfpkey-wmavoice-enc-edlproperty.md)                                   |
| g \_ wszWMADRCAverageReference          | [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md)                                          |
| g \_ wszWMADRCAverageTarget             | [MFPKEY \_ WMADRC \_ AVGTARGET](mfpkey-wmadrc-avgtargetproperty.md)                                    |
| g \_ wszWMADRCPeakReference             | [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md)                                        |
| g \_ wszWMADRCPeakTarget                | [MFPKEY \_ WMADRC \_ PEAKTARGET](mfpkey-wmadrc-peaktargetproperty.md)                                  |
| g \_ wszWMCPAudioVBRQuality             | [\_VBRQUALITY MFPKEY](mfpkey-vbrqualityproperty.md)                                                 |
| g \_ wszWMCPAudioVBRSupported           | [\_VBRENABLED MFPKEY](mfpkey-vbrenabledproperty.md)                                                 |
| g \_ wszWMCPMaxPasses                   | [\_PASSESRECOMMENDED MFPKEY](mfpkey-passesrecommendedproperty.md)                                   |
| g \_ wszWMVCAvgBitrate                  | [\_RAVG MFPKEY](mfpkey-ravgproperty.md)                                                             |
| g \_ wszWMVCBAvg                        | [\_BAVG MFPKEY](mfpkey-bavgproperty.md)                                                             |
| g \_ wszWMVCBDeltaQP                    | [\_BDELTAQP MFPKEY](mfpkey-bdeltaqpproperty.md)                                                     |
| g \_ wszWMVCBMax                        | [\_BMAX MFPKEY](mfpkey-bmaxproperty.md)                                                             |
| g \_ wszWMVCBufferFullnessInFirstByte   | [\_BUFFERFULLNESSINFIRSTBYTE MFPKEY](mfpkey-bufferfullnessinfirstbyteproperty.md)                   |
| g \_ wszWMVCCodedFrames                 | [\_CODEDFRAMES MFPKEY](mfpkey-codedframesproperty.md)                                               |
| g \_ wszWMVCComplexityEx                | [\_COMPLEXITYEX MFPKEY](mfpkey-complexityexproperty.md)                                             |
| g \_ wszWMVCComplexityMode              | [\_complessità MFPKEY](mfpkey-complexityproperty.md)                                                 |
| g \_ wszWMVCCompressionOptimizationType | [\_COMPRESSIONOPTIMIZATIONTYPE MFPKEY](mfpkey-compressionoptimizationtypeproperty.md)               |
| g \_ wszWMVCCrisp                       | [MFPKEY \_ croccante](mfpkey-crispproperty.md)                                                           |
| g \_ wszWMVCDecoderComplexityProfile    | [\_DECODERCOMPLEXITYPROFILE MFPKEY](mfpkey-decodercomplexityprofileproperty.md)                     |
| g \_ wszWMVCDecoderComplexityRequested  | [\_DECODERCOMPLEXITYREQUESTED MFPKEY](mfpkey-decodercomplexityrequestedproperty.md)                 |
| g \_ wszWMVCDecoderDeinterlacing        | [\_DEinterlacciamento del decodificatore MFPKEY \_](mfpkey-decoder-deinterlacingproperty.md)                          |
| g \_ wszWMVCDenoiseOption               | [\_DENOISEOPTION MFPKEY](mfpkey-denoiseoptionproperty.md)                                           |
| g \_ wszWMVCEndOfPass                   | [\_ENDOFPASS MFPKEY](mfpkey-endofpassproperty.md)                                                   |
| g \_ wszWMVCForceFrameHeight            | [\_FORCEFRAMEHEIGHT MFPKEY](mfpkey-forceframeheightproperty.md)                                     |
| g \_ wszWMVCForceFrameWidth             | [\_FORCEFRAMEWIDTH MFPKEY](mfpkey-forceframewidthproperty.md)                                       |
| g \_ wszWMVCForceMedianSetting          | [\_FORCEMEDIANSETTING MFPKEY](mfpkey-forcemediansettingproperty.md)                                 |
| g \_ wszWMVCFOURCC                      | [\_fourcc MFPKEY](mfpkey-fourccproperty.md)                                                         |
| g \_ wszWMVCInterlacedCodingEnabled     | [\_INTERLACEDCODINGENABLED MFPKEY](mfpkey-interlacedcodingenabledproperty.md)                       |
| g \_ wszWMVCLookAhead                   | [\_lookahead MFPKEY](mfpkey-lookaheadproperty.md)                                                   |
| g \_ wszWMVCLoopFilter                  | [\_LOOPFILTER MFPKEY](mfpkey-loopfilterproperty.md)                                                 |
| g \_ wszWMVCMacroblockModeCostMethod    | [\_MACROBLOCKMODECOSTMETHOD MFPKEY](mfpkey-macroblockmodecostmethodproperty.md)                     |
| g \_ wszWMVCMaxBitrate                  | [\_Rmax MFPKEY](mfpkey-rmaxproperty.md)                                                             |
| g \_ wszWMVCMotionMatchMethod           | [\_MOTIONMATCHMETHOD MFPKEY](mfpkey-motionmatchmethodproperty.md)                                   |
| g \_ wszWMVCMotionSearchLevel           | [\_MOTIONSEARCHLEVEL MFPKEY](mfpkey-motionsearchlevelproperty.md)                                   |
| g \_ wszWMVCMotionSearchRange           | [\_MOTIONSEARCHRANGE MFPKEY](mfpkey-motionsearchrangeproperty.md)                                   |
| g \_ wszWMVCNoiseEdgeRemoval            | [\_NOISEEDGEREMOVAL MFPKEY](mfpkey-noiseedgeremovalproperty.md)                                     |
| g \_ wszWMVCNumThreads                  | [\_numThreads MFPKEY](mfpkey-numthreadsproperty.md)                                                 |
| g \_ wszWMVCPassesRecommended           | [\_PASSESRECOMMENDED MFPKEY](mfpkey-passesrecommendedproperty.md)                                   |
| g \_ wszWMVCPassesUsed                  | [\_PASSESUSED MFPKEY](mfpkey-passesusedproperty.md)                                                 |
| g \_ wszWMVCPerceptualOptLevel          | [\_PERCEPTUALOPTLEVEL MFPKEY](mfpkey-perceptualoptlevelproperty.md)                                 |
| g \_ wszWMVCProduceDummyFrames          | [\_PRODUCEDUMMYFRAMES MFPKEY](mfpkey-producedummyframesproperty.md)                                 |
| g \_ wszWMVCRangeRedux                  | [\_RANGEREDUX MFPKEY](mfpkey-rangereduxproperty.md)                                                 |
| g \_ wszWMVCTotalFrames                 | [\_TOTALFRAMES MFPKEY](mfpkey-totalframesproperty.md)                                               |
| g \_ wszWMVCVBREnabled                  | [\_VBRENABLED MFPKEY](mfpkey-vbrenabledproperty.md)                                                 |
| g \_ wszWMVCVBRQuality                  | [\_VBRQUALITY MFPKEY](mfpkey-vbrqualityproperty.md)                                                 |
| g \_ wszWMVCVideoScaling                | [\_VIDEOSCALING MFPKEY](mfpkey-videoscalingproperty.md)                                             |
| g \_ wszWMVCVType                       | [\_VTYPE MFPKEY](mfpkey-vtypeproperty.md)                                                           |
| g \_ wszWMVCZeroByteFrames              | [\_ZEROBYTEFRAMES MFPKEY](mfpkey-zerobyteframesproperty.md)                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



