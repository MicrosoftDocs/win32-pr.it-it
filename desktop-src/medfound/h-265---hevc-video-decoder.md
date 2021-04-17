---
description: Il decodificatore Media Foundation H. 265 video è una trasformazione Media Foundation che supporta la decodifica del contenuto H. 265/HEVC nel formato allegato B e può essere usato per la riproduzione di file MP4 e M2TS.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Decodificatore video H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527697"
---
# <a name="h265--hevc-video-decoder"></a>Decodificatore video H. 265/HEVC

Il decodificatore Media Foundation H. 265 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che supporta la decodifica del contenuto H. 265/HEVC nel formato allegato B e può essere usato per la riproduzione di file MP4 e M2TS.

Il decodificatore H. 265 video espone le interfacce seguenti.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supportato in Windows 8)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Per creare un'istanza del decodificatore, chiamare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

## <a name="input-types"></a>Tipi di input

Il tipo di input deve contenere almeno i due attributi seguenti:



| Attributo                                                 | Descrizione                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md) | **Video di MFMediaType \_**                                                                        |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ HEVC](video-subtype-guids.md) o MFVideoFormat \_ HEVC \_ es |



 

Il primo sottotipo di supporto, MFVideoFormat \_ HEVC, indica che gli esempi di supporti contengono il Bitstream H. 265 con i codici iniziali e che il flusso ha Interleaved SPS/PPS. Si presuppone un frame per campione.

Il sottotipo di supporto MFVideoFormat \_ HEVC \_ es indica che gli esempi di supporti contengono un bitstream elementare H. 265, in cui ogni esempio può contenere un'immagine parziale, più immagini, alcune immagini e un'immagine parziale.

I tipi di supporti di input non possono essere modificati dinamicamente tra due tipi. Il decodificatore può rilevare le modifiche al formato di output in fase di elaborazione in base alla sintassi del flusso elementare (proporzioni, dimensioni, flag interlacciati, informazioni colorimetria) e attivare le modifiche del tipo di supporto di output corrispondente.

Per il tipo di supporto di input, il decodificatore prevede che l'origine imposti il profilo corretto. Ad esempio, se il contenuto è 10 bit, il tipo di supporto di input deve specificare il profilo come main10.

## <a name="output-types"></a>Tipi di output

Il decodificatore supporta i sottotipi di output seguenti:

-   **\_NV12 MFVideoFormat**
-   **\_P010 MFVideoFormat**

Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video](video-subtype-guids.md).

## <a name="transform-attributes"></a>Attributi di trasformazione

Il decodificatore H. 265 implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Le applicazioni possono utilizzare questo metodo per ottenere o impostare gli attributi seguenti.



| Attributo                                                                                       | Descrizione                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Codecapis \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                     | Abilita o Disabilita la modalità di decodifica a bassa latenza.                                                                                |
| [Codecapis \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                           | Imposta il numero di thread di lavoro utilizzati dal decodificatore.                                                                        |
| [Codecapis \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Abilita o Disabilita la modalità di generazione delle anteprime.                                                                                |
| [\_set di \_ lunghezza MF Nalu \_](mf-nalu-length-set.md)                                                 | Indica che le informazioni sulla lunghezza di NALU verranno inviate come BLOB con ogni esempio H. 265 compresso.                              |
| [\_ \_ informazioni sulla lunghezza di MF Nalu \_](mf-nalu-length-information.md)                                 | Indica le lunghezze di NALUs nell'esempio. Si tratta di un BLOB MF impostato su esempi di input compressi per il decodificatore H. 265. |
| [\_ \_ numero minimo di \_ campioni di output MF \_ sa \_](mf-sa-minimum-output-sample-count.md)                 | Specifica il numero massimo di campioni di output.                                                                               |



 

Il decodificatore H. 265 supporta l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Questa interfaccia fornisce un'API alternativate per l'impostazione delle proprietà dei codec seguenti.

-   [Codecapis \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)
-   [Codecapis \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [Codecapis \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a>Vincoli di formato

Il decodificatore supporta i formati seguenti:



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Profili/livelli    | Profili principale, Main Still Picture e main10                                                                                                                                                                                                                        |
| Formati Chroma     | Chroma 4:2:0                                                                                                                                                                                                                                                         |
| Risoluzione minima | 48 × 48 pixel                                                                                                                                                                                                                                                       |
| Risoluzione massima | 4096 × 2304 pixel<br/> La risoluzione massima garantita per l'accelerazione DXVA è 1920 × 1088 pixel; con risoluzioni più elevate, la decodifica viene eseguita con DXVA, se supportata dall'hardware sottostante. in caso contrario, la decodifica viene eseguita con il software.<br/> |
| DXVA               | Il decodificatore supporta DX11 e DX12 DXVA, ma non DXVA versione 2 o DXVA versione 1.                                                                                                                                                                                                         |



 

I dati di input devono essere conformi all'allegato B di ITU-T H. 265 \| ISO/IEC 23008-2. I dati devono includere i codici iniziali. Il decodificatore ignora i byte finché non trova un set di parametri di sequenza (SPS) e un set di parametri immagine (PPS) validi nel flusso di byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                              |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| DLL<br/>                      | <dl> <dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
