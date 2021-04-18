---
description: Il decodificatore MPEG-2 video è una trasformazione Media Foundation che decodifica il video MPEG-1 e MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Decoder video MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527901"
---
# <a name="mpeg-2-video-decoder"></a>Decoder video MPEG-2

Il decodificatore MPEG-2 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che decodifica il video MPEG-1 e MPEG-2. Il decodificatore supporta i video MPEG-2 Simple e Main Profile (H. 262, ISO/IEC 13818-2) e MPEG-1 video (ISO/IEC 11172-2).

## <a name="input-types"></a>Tipi di input

Il decodificatore supporta i tipi di supporti di input seguenti.

| Attributo                                                 | Descrizione                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md) | **Video di MFMediaType \_**                                                  |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ MPEG1**<br/> **MFVideoFormat \_ MPEG2**<br/> |



 

## <a name="output-types"></a>Tipi di output

Il decodificatore supporta i tipi di output seguenti.

| Attributo                                                 | Descrizione                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md) | **Video di MFMediaType \_**                                                                                                                                                         |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)        | **\_I420 MFVideoFormat**<br/> **\_IYUV MFVideoFormat**<br/> **\_NV12 MFVideoFormat**<br/> **\_YUY2 MFVideoFormat**<br/> **\_YV12 MFVideoFormat**<br/> |



 

## <a name="remarks"></a>Commenti

Il decodificatore MPEG-2 video espone le interfacce seguenti:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

L'input per il decodificatore deve essere un flusso elementare. La risoluzione massima supportata è 1920 × 1088 pixel.

Il decodificatore supporta l'accelerazione video DirectX (DXVA) con Microsoft Direct3D 9 o Microsoft Direct3D 11.

### <a name="special-decoding-modes"></a>Modalità di decodifica speciali

-   **Modalità a bassa latenza.** Questa modalità è appropriata per scenari come le comunicazioni in tempo reale. Riduce la latenza di avvio, quindi il decodificatore produce prima di tutto il primo esempio di output. Tuttavia, il decodificatore memorizza un minor numero di campioni in questa modalità, che potenzialmente possono causare problemi, perché il decodificatore non decodifica il numero di frame in anticipo. Per abilitare la modalità a bassa latenza, impostare l'attributo [CODEcapis \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) .
-   **La ricerca.** Per una ricerca precisa, chiamare il metodo [**IMFTransform:: SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) . Quando viene chiamato questo metodo, il decodificatore restituisce solo i frame che rientrano nell'intervallo di timestamp specificato dal chiamante.
-   **Modalità di generazione delle anteprime**. Questa modalità è progettata per la generazione rapida di immagini di anteprima. In questa modalità, il decodificatore decodifica inizialmente solo I frame I. Se in un certo numero di frame non viene trovato un frame I, il decodificatore inizia a Decodificare P frame e restituisce frame non-I a intervalli fissi (uno per *N* immagini) finché non viene raggiunto un frame di i. Per abilitare la modalità di generazione delle anteprime, impostare la proprietà [CODEcapis \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) .
-   **Riproduzione di trick.** Il decodificatore può decodificare le tariffe più velocemente rispetto al tempo reale. A una velocità di riproduzione superiore, il decodificatore passa alla decodifica solo I frame I. Per la riproduzione inversa vengono decodificati solo I frame I.

### <a name="codec-properties"></a>Proprietà codec

Il decodificatore supporta le proprietà seguenti tramite il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .



| Proprietà                                                                                                      | Descrizione                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Codecapis \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | Abilita o Disabilita la modalità di generazione delle anteprime.                                                             |
| [Codecapis \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | Abilita o Disabilita la decodifica con accelerazione hardware.                                                         |
| [Codecapis \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Abilita o Disabilita la modalità a bassa latenza.                                                                      |
| [il \_ decodificatore MFT \_ espone i \_ \_ tipi \_ di output in \_ \_ ordine nativo](mft-decoder-expose-output-types-in-native-order.md) | Specifica se il decodificatore espone i tipi di output idonei per la transcodifica prima di altri formati. |



 

Di queste proprietà, è possibile impostare anche i seguenti elementi tramite l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :

-   [Codecapis \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [Codecapis \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [Codecapis \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>Limitazioni

-   Il decodificatore non è supportato nelle piattaforme basate su IA-64.
-   Il decodificatore non supporta la decrittografia CSS o la riproduzione di DVD crittografati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                       |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
