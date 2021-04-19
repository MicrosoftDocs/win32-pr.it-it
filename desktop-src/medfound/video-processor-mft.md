---
description: Il processore video MFT è una trasformazione Microsoft Media Foundation (MFT) che esegue la conversione dello spazio dei colore, il ridimensionamento video, il deinterlacciamento, la conversione della frequenza dei fotogrammi, la rotazione, il ritaglio, la disimballaggio e il mirroring della visualizzazione a destra e a sinistra.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: Processore video MFT (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332600"
---
# <a name="video-processor-mft"></a>Processore video MFT

Il processore video MFT è una trasformazione Microsoft Media Foundation (MFT) che esegue la conversione dello spazio dei colore, il ridimensionamento video, il deinterlacciamento, la conversione della frequenza dei fotogrammi, la rotazione, il ritaglio, la disimballaggio e il mirroring della visualizzazione a destra e a sinistra.

## <a name="clsid"></a>CLSID

\_VIDEOPROCESSORMFT CLSID

## <a name="interfaces"></a>Interfacce

-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFVideoProcessorControl**](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a>Formati di input

-   **\_ARGB32 MFVideoFormat**
-   **\_AYUV MFVideoFormat**
-   **\_I420 MFVideoFormat**
-   **\_IYUV MFVideoFormat**
-   **\_NV11 MFVideoFormat**
-   **\_NV12 MFVideoFormat**
-   **\_RGB24 MFVideoFormat**
-   **\_Rgb32 MFVideoFormat**
-   **\_RGB555 MFVideoFormat**
-   **\_RGB565 MFVideoFormat**
-   **\_RGB8 MFVideoFormat**
-   **\_UYVY MFVideoFormat**
-   **\_V410 MFVideoFormat**
-   **\_Y216 MFVideoFormat**
-   **\_Y41P MFVideoFormat**
-   **\_Y41T MFVideoFormat**
-   **\_Y42T MFVideoFormat**
-   **\_YUY2 MFVideoFormat**
-   **\_YV12 MFVideoFormat**
-   **\_YVYU MFVideoFormat**

## <a name="output-formats"></a>Formati di output

-   **\_ARGB32 MFVideoFormat**
-   **\_AYUV MFVideoFormat**
-   **\_I420 MFVideoFormat**
-   **\_IYUV MFVideoFormat**
-   **\_NV12 MFVideoFormat**
-   **\_RGB24 MFVideoFormat**
-   **\_Rgb32 MFVideoFormat**
-   **\_RGB555 MFVideoFormat**
-   **\_RGB565 MFVideoFormat**
-   **\_UYVY MFVideoFormat**
-   **\_Y216 MFVideoFormat**
-   **\_YUY2 MFVideoFormat**
-   **\_YV12 MFVideoFormat**

Non sono supportate tutte le combinazioni di formati di input e di output. Per verificare se è supportata una conversione, impostare il tipo di input e quindi chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

Per altre informazioni su questi formati, vedere [GUID del sottotipo video](video-subtype-guids.md).

## <a name="remarks"></a>Commenti

È possibile creare un'istanza del processore video in uno dei modi seguenti:

-   Chiamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Il processore video è registrato nella categoria **MFT \_ categoria \_ \_ processore video** .
-   Chiamando la funzione COM **CoCreateInstance** passando il CLSID CLSID **\_ VideoProcessorMFT**.

Le osservazioni seguenti riguardano l'utilizzo di rettangoli di origine e rettangoli di destinazione nel **processore video MFT**. I rettangoli di origine e di destinazione vengono impostati con [**IMFVideoProcessorControl:: SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) e [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) e alcune volte con [**IMFMediaEngineEx:: UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).

-   Il rettangolo di origine deve essere allineato e arrotondato in modo da corrispondere ai requisiti del formato di colore del frame inserito nel processore video. Questo è importante perché i formati come 420 e 422 presentano requisiti relativi alle dimensioni e agli offset che è possibile creare e a cui si accede. Ad esempio, un rettangolo di origine di {1, 0, 319, 240} (a sinistra, in alto, a destra, in basso) verrà arrotondato a {2, 0, 320, 240} quando il formato di input è 420.
-   Sia il rettangolo di destinazione che quello di origine verranno sempre bloccati per adattarsi ai rispettivi frame, ovvero il rettangolo di origine al frame di origine e il rettangolo di destinazione al frame di destinazione. Ciò significa che i valori negativi non sono significativi, ma verranno sempre bloccati a 0.
-   Il rettangolo di origine si trova nel sistema di coordinate del frame di destinazione, meno qualsiasi rettangolo di destinazione. Ciò significa che le trasformazioni come la rotazione vengono annullate nel rettangolo di origine. Pertanto, non è necessario stabilire se il video è stato ruotato o 3D decompresso. Ad esempio, è possibile tracciare un rettangolo sopra il tag video, prendere le coordinate relative (rispetto al tag video), normalizzarle (intervallo compreso tra 0 e 1) e passarle come rettangolo di origine e dovrebbero funzionare come previsto, anche se è in corso la rotazione del video.

Il processore video supporta l'elaborazione video con accelerazione GPU, con Microsoft Direct3D 11. Per ulteriori informazioni, vedere [MF \_ sa \_ d3d11 \_ Aware](mf-sa-d3d11-aware.md).

### <a name="stereoscopic-video"></a>Video stereoscopico

Il processore video supporta la visualizzazione dell'operazione di decompressione nei fotogrammi video 3D:

Se il frame di input contiene due visualizzazioni compresse nello stesso frame, il processore video può suddividere le visualizzazioni in buffer distinti oppure estrarre la visualizzazione di base ed eliminare la seconda visualizzazione. Per abilitare la decompressione della visualizzazione, impostare l'attributo di [ \_ \_ \_ output MF Enable 3DVIDEO](mf-enable-3dvideo-output.md) su **MF3DVideoOutputType \_ stereo** o **MF3DVideoOutputType \_ BaseView**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




