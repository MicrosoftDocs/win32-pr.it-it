---
description: Ridimensiona un flusso video.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Video Resizer DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308967"
---
# <a name="video-resizer-dsp"></a>Ridimensionamento video DSP

Ridimensiona un flusso video.

## <a name="clsid"></a>CLSID

\_CRESIZERDMO CLSID

## <a name="interfaces"></a>Interfacce

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResizerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a>Formati

Il video Resizer di ridimensionamento video supporta i sottotipi di supporti di input/output seguenti quando funge da oggetto DMO (DirectX Media Object).

-   \_IYUV MEDIASUBTYPE
-   \_YUY2 MEDIASUBTYPE
-   \_UYVY MEDIASUBTYPE
-   \_I420 MEDIASUBTYPE
-   \_Rgb32 MEDIASUBTYPE
-   \_RGB24 MEDIASUBTYPE
-   \_RGB565 MEDIASUBTYPE
-   \_RGB8 MEDIASUBTYPE
-   \_RGB555 MEDIASUBTYPE
-   \_AYUV MEDIASUBTYPE
-   \_V216 MEDIASUBTYPE
-   \_YV12 MEDIASUBTYPE

Il video Resizer di ridimensionamento video supporta i sottotipi di supporti di input/output seguenti quando funge da trasformazione Media Foundation (MFT).

-   \_IYUV MFVideoFormat
-   \_YUY2 MFVideoFormat
-   \_UYVY MFVideoFormat
-   \_I420 MFVideoFormat
-   \_Rgb32 MFVideoFormat
-   \_RGB24 MFVideoFormat
-   \_RGB565 MFVideoFormat
-   \_RGB8 MFVideoFormat
-   \_RGB555 MFVideoFormat
-   \_AYUV MFVideoFormat
-   \_V216 MFVideoFormat
-   \_YV12 MFVideoFormat

## <a name="properties"></a>Proprietà

-   [MFPKEY \_ ridimensionare \_ src a \_ sinistra](mfpkey-resize-src-left.md)
-   [MFPKEY \_ ridimensionare \_ src in \_ alto](mfpkey-resize-src-top.md)
-   [MFPKEY \_ ridimensionare la \_ \_ larghezza src](mfpkey-resize-src-width.md)
-   [\_altezza src di ridimensionamento MFPKEY \_ \_](mfpkey-resize-src-height.md)
-   [\_ridimensionamento MFPKEY \_ DST a \_ sinistra](mfpkey-resize-dst-left.md)
-   [MFPKEY \_ ridimensionare l' \_ inizio dell'ora legale \_](mfpkey-resize-dst-top.md)
-   [\_larghezza DST MFPKEY ridimensionamento \_ \_](mfpkey-resize-dst-width.md)
-   [MFPKEY \_ ridimensionare l' \_ \_ altezza DST](mfpkey-resize-dst-height.md)
-   [MFPKEY \_ ridimensionare la \_ qualità](mfpkey-resize-quality.md)
-   [MFPKEY \_ ridimensionamento \_ interlacciato](mfpkey-resize-interlace.md)
-   [\_ridimensionamento MFPKEY \_ GEOMAPX](mfpkey-resize-geomapx.md)
-   [\_ridimensionamento MFPKEY \_ GEOMAPY](mfpkey-resize-geomapy.md)
-   [\_ridimensionamento MFPKEY \_ GEOMAPWIDTH](mfpkey-resize-geomapwidth.md)
-   [\_ridimensionamento MFPKEY \_ GEOMAPHEIGHT](mfpkey-resize-geomapheight.md)
-   [\_ridimensionamento MFPKEY \_ MINAPX](mfpkey-resize-minapx.md)
-   [\_ridimensionamento MFPKEY \_ MINAPY](mfpkey-resize-minapy.md)
-   [\_ridimensionamento MFPKEY \_ MINAPWIDTH](mfpkey-resize-minapwidth.md)
-   [\_ridimensionamento MFPKEY \_ MINAPHEIGHT](mfpkey-resize-minapheight.md)
-   [\_ridimensionamento MFPKEY \_ PANSCANAPX](mfpkey-resize-panscanapx.md)
-   [\_ridimensionamento MFPKEY \_ PANSCANAPY](mfpkey-resize-panscanapy.md)
-   [\_ridimensionamento MFPKEY \_ PANSCANAPWIDTH](mfpkey-resize-panscanapwidth.md)
-   [\_ridimensionamento MFPKEY \_ PANSCANAPHEIGHT](mfpkey-resize-panscanapheight.md)
-   [\_PIXELASPECTRATIO MFPKEY](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a>Commenti

Il video Resizer viene implementato come un oggetto COM che può fungere da DMO o da un MFT. L'oggetto ha un singolo identificatore di classe (CLSID), indipendentemente dal fatto che funga da DMO o da MFT. Per informazioni sul momento in cui un DSP funge da DMO o da un MFT, vedere [processori di segnali digitali](windowsmediadigitalsignalprocessors.md).

Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un DSP funga da DMO o da un MFT. I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un DSP funga da DMO o da un MFT. Per informazioni sui GUID che rappresentano sottotipi di supporti, vedere GUID del [sottotipo video](video-subtype-guids.md).

Questo DSP può eseguire sia il ritaglio che la scalabilità nell'immagine video. Il formato del tipo di output deve corrispondere al formato del tipo di input. Il DSP non esegue le conversioni dello spazio dei colori.

Prima di impostare il tipo di output, è possibile definire una delle aree seguenti utilizzando le proprietà elencate in questa tabella.



| Region                   | Proprietà                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rettangolo di origine         | MFPKEY \_ ridimensionare \_ src a \_ sinistra<br/> MFPKEY \_ ridimensionare \_ src in \_ alto<br/> MFPKEY \_ ridimensionare la \_ \_ larghezza src<br/> \_altezza src di ridimensionamento MFPKEY \_ \_<br/>            |
| Rettangolo di destinazione    | \_ridimensionamento MFPKEY \_ DST a \_ sinistra<br/> MFPKEY \_ ridimensionare l' \_ inizio dell'ora legale \_<br/> \_larghezza DST MFPKEY ridimensionamento \_ \_<br/> MFPKEY \_ ridimensionare l' \_ \_ altezza DST<br/>            |
| Apertura geometrica       | \_ridimensionamento MFPKEY \_ GEOMAPX<br/> \_ridimensionamento MFPKEY \_ GEOMAPY<br/> \_ridimensionamento MFPKEY \_ GEOMAPWIDTH<br/> \_ridimensionamento MFPKEY \_ GEOMAPHEIGHT<br/>             |
| Apertura minima visualizzazione | \_ridimensionamento MFPKEY \_ MINAPX<br/> \_ridimensionamento MFPKEY \_ MINAPY<br/> \_ridimensionamento MFPKEY \_ MINAPWIDTH<br/> \_ridimensionamento MFPKEY \_ MINAPHEIGHT<br/>                 |
| Area Pan/Scan          | \_ridimensionamento MFPKEY \_ PANSCANAPX<br/> \_ridimensionamento MFPKEY \_ PANSCANAPY<br/> \_ridimensionamento MFPKEY \_ PANSCANAPWIDTH<br/> \_ridimensionamento MFPKEY \_ PANSCANAPHEIGHT<br/> |



 

In ogni caso, è necessario impostare tutte le proprietà associate affinché l'impostazione abbia effetto.

Il DSP copia la parte dell'immagine di origine definita dal rettangolo di origine e lo estende o comprime nel rettangolo di destinazione nel buffer di output. I rettangoli di origine e di destinazione non devono necessariamente avere le stesse dimensioni. La dimensione del fotogramma nel tipo di supporto di output deve essere sufficientemente grande da contenere il rettangolo di destinazione.

L'apertura geometrica, l'apertura minima dello schermo e l'area di Pan/Scan non influiscono sul modo in cui il DSP ridimensiona il video. Tuttavia, potrebbero influire sul modo in cui il componente downstream interpreta il frame del video. In particolare, il renderer video avanzato (EVR) usa questi valori quando calcola le proporzioni dell'immagine e l'area di visualizzazione.

Se si usano Media Foundation tipi di supporto, è possibile impostare l'apertura geometrica, l'apertura minima dello schermo e le aree di Pan/Scan direttamente nel tipo di supporto di output. In caso contrario, se si usano i tipi di supporto DMO, impostarli usando le proprietà.

Per altre informazioni, vedere i seguenti argomenti:

-   [**\_ \_ apertura geometrica MF mt \_**](mf-mt-geometric-aperture-attribute.md)
-   [**\_ \_ \_ apertura minima schermo \_ MF mt**](mf-mt-minimum-display-aperture-attribute.md)
-   [**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vidreszr.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
