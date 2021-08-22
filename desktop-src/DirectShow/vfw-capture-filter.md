---
description: Filtro di acquisizione VFW
ms.assetid: 663b6b3b-2a50-4586-9506-600a59869abe
title: Filtro di acquisizione VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 679f8e736564534948d05fe25ecb1bc18bbb787df370aca0f9a3752960f719ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071955"
---
# <a name="vfw-capture-filter"></a>Filtro di acquisizione VFW

Questo filtro funziona con hardware di acquisizione video precedente che usa Video For Windows.

Questo filtro ha due pin di output. Uno è denominato Acquisizione e l'altro è denominato Anteprima o Sovrimpressione.



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | **IPersistPropertyBag,** [**IAMVfwCaptureDialogs,**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) **ISpecifyPropertyPages,** [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Tipi di supporti pin di input                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Interfacce pin di input                     | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipi di supporti pin di output                   | Acquisizione: MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfoOverlay: MEDIATYPE \_ Video, MEDIASUBTYPE \_ Overlay, FORMAT \_ VideoInfo<br/> Anteprima: MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Interfacce pin di output                    | Pin di acquisizione: [**IAMBufferNegotiation,**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) [**IAMDroppedFrames,**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) [**IAMPushSource,**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IKsPropertySet,**](ikspropertyset.md) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)Overlay Pin: [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet,**](ikspropertyset.md) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> Pin di anteprima: [**IAMPushSource,**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IKsPropertySet,**](ikspropertyset.md) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> |
| CLSID del filtro                             | CLSID \_ VfwCapture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID pagina delle proprietà                      | CLSID \_ CaptureProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| File eseguibile                               | qcap.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Merito](merit.md)                       | NON \_ \_ USARE \_                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Categoria filtro](filter-categories.md) | CLSID \_ VideoInputDeviceCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Anche se il pin di acquisizione espone [**l'interfaccia IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) per questa interfaccia vengono implementati solo i metodi **SetFormat** e **GetFormat.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 




