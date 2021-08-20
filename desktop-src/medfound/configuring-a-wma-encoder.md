---
description: Impostazione di un tipo di output per un codificatore WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Impostazione di un tipo di output per un codificatore WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48f2731a081138bda30ab3e81f01d353e0348f4d3586fd4c02878b62a7f04393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880572"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Impostazione di un tipo di output per un codificatore WMA

Per creare un tipo di output valido per un Windows Media Audio (WMA), è necessario disporre delle informazioni seguenti:

-   Sottotipo audio che ricorsiva il formato WMA codificato. Vedere [GUID del sottotipo audio](audio-subtype-guids.md).
-   Proprietà di configurazione da impostare nel codificatore.

    Le proprietà di configurazione sono documentate nella documentazione Windows codec audio e video multimediale e api DSP. Per altre informazioni, vedere "Proprietà del flusso audio" in [Proprietà di codifica](configuring-the-encoder.md).

### <a name="windows-vista-or-later"></a>Windows Vista o versioni successive

Per ottenere un tipo di output valido per il codificatore, seguire questa procedura.

1.  Usare la [**funzione MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per creare un'istanza del codificatore.
2.  Eseguire una query sul codificatore per **l'interfaccia IPropertyStore.**
3.  Usare **l'interfaccia IPropertyStore** per configurare il codificatore.
4.  Recuperare i tipi di output supportati chiamando [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in un ciclo finché il codificatore non restituisce **MF \_ E NO MORE \_ \_ \_ TYPES** e non si sceglie il tipo di supporto di destinazione. I
5.  Chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di compressione nel codificatore.

### <a name="windows-7"></a>Windows 7

Per ottenere un tipo di output valido per il codificatore in Windows 7, Media Foundation fornisce la funzione [**MFTranscodeGetAudioOutputAvailableTypes.**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) Un'applicazione deve passare il sottotipo audio che ricorsiva l'WMA codificato e le proprietà di codifica. Le proprietà sono obbligatorie perché il codificatore modifica i tipi di output supportati a seconda del set di modalità.

> [!Note]  
> [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)è supportato solo per [la codifica a velocità in bit costante.](constant-bit-rate-encoding.md)

 

Se la chiamata ha esito positivo, l'applicazione riceve un elenco di puntatori IUnknown dei tipi di supporti di output supportati in un [**oggetto IMFCollection.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) Per impostare il tipo di supporto di output, trovare quello corrispondente al tipo di destinazione e chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di compressione nel codificatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificatori multimediali](windows-media-encoders.md)
</dt> </dl>

 

 



