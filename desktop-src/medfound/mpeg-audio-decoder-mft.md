---
description: Microsoft MPEG Audio Decoder è una trasformazione Media Foundation (MFT) sincrona che consente di decodificare formati di flusso elementari audio MPEG usando la pipeline Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Decodificatore audio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb908509f9c9f1c55ef7434b33d3265be875bf56443bc69c5a4cf829774bded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722281"
---
# <a name="mpeg-audio-decoder"></a>Decodificatore audio MPEG

Microsoft MPEG Audio Decoder è una trasformazione [Media Foundation](media-foundation-transforms.md) (MFT) sincrona che consente di decodificare formati di flusso elementari audio MPEG usando la pipeline Media Foundation (MF).

Il decodificatore supporta i formati di flusso elementari MPEG seguenti.

-   Livelli audio MPEG-1 I e II (ISO/IEC 11172-3). 2. MPEG-2 compatibile con le versioni precedenti, i livelli I e II (ISO)

-   MPEG-2 compatibile con le versioni precedenti, livelli I e II (ISO/IEC 13818-3), solo mono e stereo

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del decodificatore audio MPEG è **CLSID \_ MSMPEGAudDecMFT,** definito nel file di intestazione wmcodecdsp.h.

## <a name="input-media-types"></a>Tipi di supporti di input

Il decodificatore MPEG Audio supporta gli attributi del tipo di supporto di input seguenti.



| Attributo                                                                               | Valore                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**                                                                                                                                                                                                                                                |
| [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG**                                                                                                                                                                                                                                               |
| [**MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS**](mf-mt-audio-num-channels-attribute.md)              | (Facoltativo) In genere 1 per mono o 2 per stereo, ma può essere fino a 6 canali.<br/>                                                                                                                                                                                |
| [**MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK**](mf-mt-audio-channel-mask-attribute.md)              | (Facoltativo) In 0x4 per mono o 0x3 per stereo, ma può anche essere una qualsiasi delle maschere di canale associate a un massimo di 6 canali (3/2/1, 3/2, 3/1, 2/2, 2/1). Se presente, la maschera di canale deve essere coerente con il numero di canali di input specificato.<br/> |
| [**ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO**](mf-mt-audio-samples-per-second-attribute.md) | (Facoltativo) Uno dei seguenti: 16000, 22050, 24000, 32000, 44100, 48000. Se specificato, la frequenza di campionamento di input deve essere una delle frequenze di campionamento MPEG valide.<br/>                                                                                             |



 

## <a name="output-media-types"></a>Tipi di supporti di output

Il decodificatore MPEG Audio supporterà fino a quattro sottotipi di supporti di output, nell'ordine seguente.

<dl> 1. Stereo a virgola mobile.  
2. Stereo, PCM a 16 bit.  
3. Mono, a virgola mobile (solo se l'input è mono o dual mono).  
4. Mono, PCM a 16 bit (solo se l'input è mono o dual mono).  
</dl>

Il decodificatore supporta sempre l'output stereo e viene enumerato come primo tipo di supporto di output.

Il decodificatore supporta gli attributi del tipo di supporto di output seguenti.



| Attributo                                                                           | Valore                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**                                                     |
| [MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ PCM** o **MFAudioFormat \_ Float**                  |
| [MF \_ MT \_ AUDIO \_ BITS \_ PER \_ SAMPLE](mf-mt-audio-bits-per-sample-attribute.md)       | 16 o 32                                                                   |
| [MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS](mf-mt-audio-num-channels-attribute.md)              | 1 o 2                                                                     |
| [MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK](mf-mt-audio-channel-mask-attribute.md)              | 0x4 per mono o 0x3 per stereo                                             |
| [ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO](mf-mt-audio-samples-per-second-attribute.md) | Uno dei seguenti: 16000, 22050, 24000, 32000, 44100, 48000.<br/> |



 

## <a name="transform-attributes"></a>Attributi di trasformazione

Il decodificatore audio MPEG implementa il [**metodo IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Le applicazioni possono usare questo metodo per ottenere o impostare gli attributi seguenti.



| Attributo                                                                               | Descrizione                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI \_ AVDecAudioDualMono**](../directshow/avdecaudiodualmono-property.md)                   | Specifica se l'audio a 2 canali decodificato è doppio mono o meno. Di sola lettura. Impostata da MFT. Per altre informazioni, [**vedere eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).                                                                                                                               |
| [**CODECAPI \_ AVDecAudioDualMonoReproMode**](../directshow/avdecaudiodualmonorepromode-property.md) | Specifica la modalità di riproduzione dell'audio doppio mono da parte del decodificatore. Il valore predefinito è **eAVDecAudioDualMonoReproMode \_ LEFT \_ MONO.**<br/> Lettura/Scrittura. Le applicazioni possono impostare questa proprietà per modificare il comportamento predefinito. Per altre informazioni, [**vedere eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).<br/> |
| [**CODECAPI \_ AVEncCommonMeanBitRate**](../directshow/avenccommonmeanbitrate-property.md)           | Specifica la velocità in bit del flusso compresso. Di sola lettura. Impostata da MFT.                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
