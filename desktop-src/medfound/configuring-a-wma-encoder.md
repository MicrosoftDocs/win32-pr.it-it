---
description: Impostazione di un tipo di output per un codificatore WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Impostazione di un tipo di output per un codificatore WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127962"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Impostazione di un tipo di output per un codificatore WMA

Per creare un tipo di output valido per un codificatore Windows Media Audio (WMA), è necessario disporre delle seguenti informazioni:

-   Sottotipo audio che repesents il formato WMA codificato. Vedere [GUID del sottotipo audio](audio-subtype-guids.md).
-   Proprietà di configurazione da impostare sul codificatore.

    Le proprietà di configurazione sono documentate nella documentazione relativa a Windows Media Audio e codec video e alle API DSP. Per ulteriori informazioni, vedere "proprietà del flusso audio" nelle [proprietà di codifica](configuring-the-encoder.md).

### <a name="windows-vista-or-later"></a>Windows Vista o versioni successive

Per ottenere un tipo di output valido per il codificatore, seguire questa procedura.

1.  Utilizzare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per creare un'istanza del codificatore.
2.  Eseguire una query sul codificatore per l'interfaccia **IPropertyStore** .
3.  Utilizzare l'interfaccia **IPropertyStore** per configurare il codificatore.
4.  Recuperare i tipi di output supportati chiamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in un ciclo fino a quando il codificatore **non restituisce MF \_ e \_ non \_ più \_ tipi** e si sceglie il tipo di supporto di destinazione. I
5.  Chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di compressione nel codificatore.

### <a name="windows-7"></a>Windows 7

Per ottenere un tipo di output valido per il codificatore in Windows 7, Media Foundation fornisce la funzione [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) . Per un'applicazione deve essere necessario passare il sottotipo audio che repesents le proprietà WMA codificate e la codifica. Le proprietà sono necessarie perché il codificatore modifica i tipi di output supportati a seconda della modalità impostata.

> [!Note]  
> [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)è supportato solo per la [codifica della velocità in bit costante](constant-bit-rate-encoding.md).

 

Se la chiamata ha esito positivo, l'applicazione riceve un elenco di puntatori IUnknown dei tipi di supporti di output supportati in un oggetto [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) . Per impostare il tipo di supporto di output, trovare quello che corrisponde al tipo di destinazione e chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di compressione nel codificatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificatori Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



