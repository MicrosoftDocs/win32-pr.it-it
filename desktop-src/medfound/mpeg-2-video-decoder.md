---
description: MpEG-2 Video Decoder è una Media Foundation che decodifica i video MPEG-1 e MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Decodificatore video MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e2b270cadb114875fb63bc6c57ce2ddd63eecb2815b8fe3bcee175710d1771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012591"
---
# <a name="mpeg-2-video-decoder"></a>Decodificatore video MPEG-2

MpEG-2 Video Decoder è una Media Foundation [che](media-foundation-transforms.md) decodifica i video MPEG-1 e MPEG-2. Il decodificatore supporta video con profilo semplice e principale MPEG-2 (H.262, ISO/IEC 13818-2) e video MPEG-1 (ISO/IEC 11172-2).

## <a name="input-types"></a>Tipi di input

Il decodificatore supporta i tipi di supporti di input seguenti.

| Attributo                                                 | Descrizione                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) | **Video su MFMediaType \_**                                                  |
| [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ MPEG1**<br/> **MFVideoFormat \_ MPEG2**<br/> |



 

## <a name="output-types"></a>Tipi di output

Il decodificatore supporta i tipi di output seguenti.

| Attributo                                                 | Descrizione                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) | **Video su MFMediaType \_**                                                                                                                                                         |
| [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ I420**<br/> **MFVideoFormat \_ IYUV**<br/> **MFVideoFormat \_ NV12**<br/> **MFVideoFormat \_ YUY2**<br/> **MFVideoFormat \_ YV12**<br/> |



 

## <a name="remarks"></a>Commenti

Il decodificatore video MPEG-2 espone le interfacce seguenti:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

L'input per il decodificatore deve essere un flusso elementare. La risoluzione massima supportata è 1920 × 1088 pixel.

Il decodificatore supporta l'accelerazione video DirectX (DXVA) usando Microsoft Direct3D 9 o Microsoft Direct3D 11.

### <a name="special-decoding-modes"></a>Modalità di decodifica speciali

-   **Modalità a bassa latenza.** Questa modalità è appropriata per scenari come le comunicazioni in tempo reale. Riduce la latenza di avvio, quindi il decodificatore produce prima il primo campione di output. Tuttavia, il decodificatore bufferizza un numero inferiore di campioni in questa modalità, il che può potenzialmente causare problemi, perché il decodificatore non decodifica in anticipo il numero di fotogrammi. Per abilitare la modalità a bassa latenza, impostare [l'attributo CODECAPI \_ AVLowLatencyMode.](codecapi-avlowlatencymode.md)
-   **riercare.** Per una ricerca precisa, chiamare [**il metodo IMFTransform::SetOutputBounds.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) Quando viene chiamato questo metodo, il decodificatore restituisce solo i fotogrammi che rientrano nell'intervallo di timestamp specificato dal chiamante.
-   **Modalità di generazione dell'anteprima**. Questa modalità è destinata alla generazione rapida di immagini di anteprima. In questa modalità, il decodificatore decodifica inizialmente solo i fotogrammi I. Se non viene trovato alcun fotogramma I all'interno di un determinato numero di fotogrammi, il decodificatore avvia la decodifica dei fotogrammi P e restituisce i fotogrammi non I a un intervallo fisso (una per *N* immagini) fino a quando non viene raggiunto un fotogramma I. Per abilitare la modalità di generazione delle anteprime, impostare la [proprietà CODECAPI \_ AVDecVideoThumbnailGenerationMode.](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   **Gioco di trick.** Il decodificatore può essere decodificato a velocità più veloci rispetto a quelle in tempo reale. Con velocità di riproduzione più elevate, il decodificatore passa alla decodifica solo dei fotogrammi I. Per la riproduzione inversa, vengono decodificati solo i fotogrammi I.

### <a name="codec-properties"></a>Proprietà codec

Il decodificatore supporta le proprietà seguenti tramite il [**metodo IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)



| Proprietà                                                                                                      | Descrizione                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | Abilita o disabilita la modalità di generazione delle anteprime.                                                             |
| [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | Abilita o disabilita la decodifica con accelerazione hardware.                                                         |
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Abilita o disabilita la modalità a bassa latenza.                                                                      |
| [IL DECODIFICATORE MFT \_ ESPONE I TIPI DI OUTPUT IN ORDINE \_ \_ \_ \_ \_ \_ NATIVO](mft-decoder-expose-output-types-in-native-order.md) | Specifica se il decodificatore espone tipi di output adatti per la transcoding prima di altri formati. |



 

Di queste proprietà, è anche possibile impostare le proprietà seguenti tramite [**l'interfaccia ICodecAPI:**](/windows/win32/api/strmif/nn-strmif-icodecapi)

-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>Limitazioni

-   Il decodificatore non è supportato nelle piattaforme basate su IA-64.
-   Il decodificatore non supporta la decrittografia CSS o la riproduzione di DVD crittografati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                       |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
