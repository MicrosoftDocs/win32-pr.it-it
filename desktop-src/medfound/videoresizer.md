---
description: Ridimensiona un flusso video.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Video Resizer DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d26dcc53baf38336656d870acc5583066e0816a0bf963217db1da54513ee18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721321"
---
# <a name="video-resizer-dsp"></a>DSP di Ridimensionamento video

Ridimensiona un flusso video.

## <a name="clsid"></a>CLSID

CLSID \_ CResizerDMO

## <a name="interfaces"></a>Interfacce

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResizerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a>Formati

Il DSP di Ridimensionamento video supporta i sottotipi multimediali di input/output seguenti quando funge da oggetto multimediale DirectX (DMO).

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ AYUV
-   MEDIASUBTYPE \_ V216
-   MEDIASUBTYPE \_ YV12

Il DSP di Ridimensionamento video supporta i sottotipi multimediali di input/output seguenti quando funge da Media Foundation Transform (MFT).

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ AYUV
-   MFVideoFormat \_ V216
-   MFVideoFormat \_ YV12

## <a name="properties"></a>Proprietà

-   [MFPKEY \_ RESIZE \_ SRC \_ LEFT](mfpkey-resize-src-left.md)
-   [MFPKEY \_ RESIZE \_ SRC \_ TOP](mfpkey-resize-src-top.md)
-   [MFPKEY \_ RESIZE \_ SRC \_ WIDTH](mfpkey-resize-src-width.md)
-   [MFPKEY \_ RESIZE \_ SRC \_ HEIGHT](mfpkey-resize-src-height.md)
-   [MFPKEY \_ RESIZE \_ DST \_ LEFT](mfpkey-resize-dst-left.md)
-   [MFPKEY \_ RESIZE \_ DST \_ TOP](mfpkey-resize-dst-top.md)
-   [MFPKEY \_ RESIZE \_ DST \_ WIDTH](mfpkey-resize-dst-width.md)
-   [MFPKEY \_ RESIZE \_ DST \_ HEIGHT](mfpkey-resize-dst-height.md)
-   [QUALITÀ DI RIDIMENSIONAMENTO MFPKEY \_ \_](mfpkey-resize-quality.md)
-   [INTERLACE DI RIDIMENSIONAMENTO MFPKEY \_ \_](mfpkey-resize-interlace.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPX](mfpkey-resize-geomapx.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPY](mfpkey-resize-geomapy.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPWIDTH](mfpkey-resize-geomapwidth.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPHEIGHT](mfpkey-resize-geomapheight.md)
-   [MFPKEY \_ RESIZE \_ MINAPX](mfpkey-resize-minapx.md)
-   [MFPKEY \_ RESIZE \_ MINAPY](mfpkey-resize-minapy.md)
-   [MFPKEY \_ RESIZE \_ MINAPWIDTH](mfpkey-resize-minapwidth.md)
-   [MFPKEY \_ RESIZE \_ MINAPHEIGHT](mfpkey-resize-minapheight.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPX](mfpkey-resize-panscanapx.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPY](mfpkey-resize-panscanapy.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPWIDTH](mfpkey-resize-panscanapwidth.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPHEIGHT](mfpkey-resize-panscanapheight.md)
-   [MFPKEY \_ PIXELASPECTRATIO](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a>Commenti

Il DSP di Ridimensionamento video viene implementato come oggetto COM che può fungere da DMO o MFT. L'oggetto ha un singolo identificatore di classe (CLSID) indipendentemente dal fatto che agisca come DMO o MFT. Per informazioni su quando un DSP funge da DMO o MFT, vedere [Processori di segnali digitali](windowsmediadigitalsignalprocessors.md).

I GUID (Globally Unique Identifier) per i sottotipi di supporti RGB variano a seconda che un provider di servizi multimediali agirà come DMO o MFT. I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un provider di servizi DSP agirà come DMO o MFT. Per informazioni sui GUID che rappresentano i sottotipi multimediali, vedere [GUID di sottotipo video](video-subtype-guids.md).

Questo DSP può eseguire sia il ritaglio che il ridimensionamento dell'immagine video. Il formato del tipo di output deve corrispondere al formato del tipo di input. DSP non esegue conversioni dello spazio dei colori.

Prima di impostare il tipo di output, è possibile definire una delle aree seguenti usando le proprietà elencate in questa tabella.



| Region                   | Proprietà                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rettangolo di origine         | MFPKEY \_ RESIZE \_ SRC \_ LEFT<br/> MFPKEY \_ RESIZE \_ SRC \_ TOP<br/> MFPKEY \_ RESIZE \_ SRC \_ WIDTH<br/> MFPKEY \_ RESIZE \_ SRC \_ HEIGHT<br/>            |
| Rettangolo di destinazione    | MFPKEY \_ RESIZE \_ DST \_ LEFT<br/> MFPKEY \_ RESIZE \_ DST \_ TOP<br/> MFPKEY \_ RESIZE \_ DST \_ WIDTH<br/> MFPKEY \_ RESIZE \_ DST \_ HEIGHT<br/>            |
| Apertura geometrica       | MFPKEY \_ RESIZE \_ GEOMAPX<br/> MFPKEY \_ RESIZE \_ GEOMAPY<br/> MFPKEY \_ RESIZE \_ GEOMAPWIDTH<br/> MFPKEY \_ RESIZE \_ GEOMAPHEIGHT<br/>             |
| Apertura minima dello schermo | MFPKEY \_ RESIZE \_ MINAPX<br/> MFPKEY \_ RESIZE \_ MINAPY<br/> MFPKEY \_ RESIZE \_ MINAPWIDTH<br/> MFPKEY \_ RESIZE \_ MINAPHEIGHT<br/>                 |
| Area di panoramica/analisi          | MFPKEY \_ RESIZE \_ PANSCANAPX<br/> MFPKEY \_ RESIZE \_ PANSCANAPY<br/> MFPKEY \_ RESIZE \_ PANSCANAPWIDTH<br/> MFPKEY \_ RESIZE \_ PANSCANAPHEIGHT<br/> |



 

In ogni caso, è necessario impostare tutte le proprietà associate per l'applicazione dell'impostazione.

Il DSP copia la parte dell'immagine di origine definita dal rettangolo di origine e la estende o comprime nel rettangolo di destinazione nel buffer di output. Non è necessario che i rettangoli di origine e di destinazione siano della stessa dimensione. Le dimensioni del frame nel tipo di supporto di output devono essere sufficientemente grandi da contenere il rettangolo di destinazione.

L'apertura geometrica, l'apertura minima dello schermo e l'area panoramica/scansione non influiscono sul ridimensionamento del video da parte del DSP. Tuttavia, potrebbero influire sul modo in cui il componente downstream interpreta il fotogramma video. In particolare, il renderer video avanzato (EVR) usa questi valori quando calcola le proporzioni dell'immagine e l'area di visualizzazione.

Se si usano tipi di Media Foundation, è possibile impostare l'apertura geometrica, l'apertura minima dello schermo e le aree di panoramica/scansione direttamente nel tipo di supporto di output. In caso contrario, se si usano DMO di supporti, impostarli usando le proprietà .

Per altre informazioni, vedere i seguenti argomenti:

-   [**MF \_ MT \_ GEOMETRIC \_ APERTURE**](mf-mt-geometric-aperture-attribute.md)
-   [**MF \_ MT \_ MINIMUM \_ DISPLAY \_ APERTURE**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vidreszr.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
