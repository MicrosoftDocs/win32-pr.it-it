---
description: Microsoft MPEG audio decoder è una trasformazione di Media Foundation sincrona (MFT) che consente di decodificare i formati MPEG audio Elementary Stream usando la pipeline Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Decoder audio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966987"
---
# <a name="mpeg-audio-decoder"></a>Decoder audio MPEG

Microsoft MPEG audio decoder è una trasformazione di [Media Foundation](media-foundation-transforms.md) sincrona (MFT) che consente di decodificare i formati MPEG audio Elementary Stream usando la pipeline Media Foundation (MF).

Il decodificatore supporta i formati MPEG Elementary Stream seguenti.

-   MPEG-1 Audio Layer I e II (ISO/IEC 11172-3). 2. MPEG-2 compatibile con le versioni precedenti, livelli I e II (ISO

-   MPEG-2 compatibile con le versioni precedenti, livelli I e II (ISO/IEC 13818-3), solo mono e stereo

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del decodificatore audio MPEG è **CLSID \_ MSMPEGAudDecMFT**, definito nel file di intestazione wmcodecdsp. h.

## <a name="input-media-types"></a>Tipi di supporti di input

Il decodificatore audio MPEG supporta gli attributi di tipo supporto di input seguenti.



| Attributo                                                                               | Valore                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                               | **\_Audio MFMediaType**                                                                                                                                                                                                                                                |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                      | **\_MPEG MFAudioFormat**                                                                                                                                                                                                                                               |
| [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)              | Opzionale In genere 1 per mono o 2 per stereo, ma può essere composto da un massimo di 6 canali.<br/>                                                                                                                                                                                |
| [**\_ \_ \_ maschera canale audio MF \_ mt**](mf-mt-audio-channel-mask-attribute.md)              | Opzionale In genere 0x4 per mono o 0x3 per stereo, ma può anche essere una qualsiasi delle maschere di canale associate a un massimo di 6 canali (3/2/1, 3/2, 3/1, 2/2, 2/1). Se presente, la maschera del canale deve essere coerente con il numero di canali di input specificato.<br/> |
| [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md) | Opzionale Uno dei seguenti: 16000, 22050, 24000, 32000, 44100, 48000. Se specificato, la frequenza di campionamento dell'input deve essere una delle frequenze di campionamento MPEG valide.<br/>                                                                                             |



 

## <a name="output-media-types"></a>Tipi di supporti di output

Il decodificatore audio MPEG supporta fino a quattro sottotipi di supporti di output, nell'ordine seguente.

<dl> 1. Stereo, a virgola mobile.  
2. Stereo a 16 bit PCM.  
3. Mono, virgola mobile (solo se l'input è mono o dual-mono).  
4. Mono, PCM a 16 bit (solo se l'input è mono o dual-mono).  
</dl>

Il decodificatore supporta sempre l'output stereo ed è enumerato come primo tipo di supporto di output.

Il decodificatore supporta gli attributi di tipo supporto di output seguenti.



| Attributo                                                                           | Valore                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_ \_ tipo principale MF \_ mt](mf-mt-major-type-attribute.md)                               | **\_Audio MFMediaType**                                                     |
| [sottotipo MF \_ mt \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ PCM** o **MFAudioFormat \_ float**                  |
| [\_ \_ bit audio MF \_ mt \_ per \_ campione](mf-mt-audio-bits-per-sample-attribute.md)       | 16 o 32                                                                   |
| [numero \_ di \_ \_ canali audio MF mt \_](mf-mt-audio-num-channels-attribute.md)              | 1 o 2                                                                     |
| [\_ \_ \_ maschera canale audio MF \_ mt](mf-mt-audio-channel-mask-attribute.md)              | 0x4 per mono o 0x3 per stereo                                             |
| [\_ \_ campioni audio MF \_ mt \_ al \_ secondo](mf-mt-audio-samples-per-second-attribute.md) | Uno dei seguenti: 16000, 22050, 24000, 32000, 44100, 48000.<br/> |



 

## <a name="transform-attributes"></a>Attributi di trasformazione

Il decodificatore MPEG audio implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Le applicazioni possono utilizzare questo metodo per ottenere o impostare gli attributi seguenti.



| Attributo                                                                               | Descrizione                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codecapis \_ AVDecAudioDualMono**](../directshow/avdecaudiodualmono-property.md)                   | Specifica se l'audio a 2 canali da decodificare è dual mono o meno. Di sola lettura. Impostato dal MFT. Per ulteriori informazioni, vedere [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).                                                                                                                               |
| [**Codecapis \_ AVDecAudioDualMonoReproMode**](../directshow/avdecaudiodualmonorepromode-property.md) | Specifica il modo in cui il decodificatore riproduce audio mono doppio. Il valore predefinito è **eAVDecAudioDualMonoReproMode \_ Left \_ mono**.<br/> Lettura/Scrittura. Le applicazioni possono impostare questa proprietà per modificare il comportamento predefinito. Per ulteriori informazioni, vedere [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).<br/> |
| [**Codecapis \_ AVEncCommonMeanBitRate**](../directshow/avenccommonmeanbitrate-property.md)           | Specifica la velocità in bit del flusso compresso. Di sola lettura. Impostato dal MFT.                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
