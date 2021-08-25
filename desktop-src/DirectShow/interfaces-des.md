---
description: Interfacce per i DirectShow di modifica
ms.assetid: e7fdb387-83b3-4fa2-9608-2f5dc95975bf
title: Interfacce per i DirectShow di modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e913ec6bf17a11a4b772d288b9404113cd6bdc70bf441ed20dcbc69a086f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397592"
---
# <a name="interfaces-for-directshow-editing-services"></a>Interfacce per i DirectShow di modifica

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Questa sezione contiene argomenti di riferimento [per le DirectShow DIS (Editing Services).](directshow-editing-services.md)



| Interfaccia                                                  | Descrizione                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IAMErrorLog**](iamerrorlog.md)                         | Fornisce un metodo di callback per la registrazione degli errori.                                                                                  |
| [**IAMSetErrorLog**](iamseterrorlog.md)                   | Imposta o recupera un log degli errori.                                                                                                |
| [**IAMTimeline**](iamtimeline.md)                         | Fornisce metodi per la modifica della sequenza temporale.                                                                                |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Inserisce o recupera tracce virtuali in una composizione.                                                                          |
| [**IAMTimelineEffect**](iamtimelineeffect.md)             | Fornisce metodi per la modifica degli effetti della sequenza temporale.                                                                            |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | Fornisce metodi per l'aggiunta di effetti a un oggetto sequenza temporale.                                                                      |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Imposta e recupera le proprietà sui gruppi.                                                                                       |
| [**IAMTimelineObj**](iamtimelineobj.md)                   | Fornisce metodi per la modifica di oggetti sequenza temporale.                                                                            |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | Divide un oggetto sequenza temporale.                                                                                                      |
| [**IAMTimelineSrc**](iamtimelinesrc.md)                   | Fornisce metodi per la modifica e l'impostazione delle proprietà sugli oggetti di origine.                                                    |
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Fornisce metodi per la modifica degli oggetti traccia.                                                                               |
| [**IAMTimelineTrans**](iamtimelinetrans.md)               | Fornisce metodi per la modifica degli oggetti di transizione.                                                                          |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | Aggiunge transizioni a un oggetto .                                                                                                 |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Fornisce metodi per l'utilizzo di tracce virtuali.                                                                              |
| [**IDxtAlphaSetter**](idxtalphasetter.md)                 | Imposta le proprietà [sull'effetto Setter](alpha-setter-effect.md) alfa.                                                         |
| [**IDxtCompositor**](idxtcompositor.md)                   | Imposta le proprietà per la [transizione Compositor.](compositor-transition.md)                                                     |
| [**IDxtJpeg**](idxtjpeg.md)                               | Imposta le proprietà nella transizione [di cancellazione SMPTE.](smpte-wipe-transition.md)                                                     |
| [**IDxtKey**](idxtkey.md)                                 | Imposta le proprietà per la [transizione](key-transition.md) key.                                                                   |
| [**IFindCompressorCB**](ifindcompressorcb.md)             | Non supportata.                                                                                                                 |
| [**IGrfCache**](igrfcache.md)                             | Non supportata.                                                                                                                 |
| [**IMediaDet**](imediadet.md)                             | Recupera informazioni su un file multimediale, ad esempio il numero di flussi e il tipo, la durata e la frequenza dei fotogrammi di ogni flusso. |
| [**IMediaLocator**](imedialocator.md)                     | Fornisce metodi per la convalida dei nomi di file.                                                                                    |
| [**IPropertySetter**](ipropertysetter.md)                 | Imposta le proprietà su un effetto o una transizione.                                                                                    |
| [**IRenderEngine**](irenderengine.md)                     | Esegue il rendering di un progetto DES creando un grafico di filtro da una sequenza temporale.                                                          |
| [**IRenderEngine2**](irenderengine2.md)                   | Consente all'applicazione di sostituire il filtro di ridimensionamento video predefinito usato da DES.                                              |
| [**IResize**](iresize.md)                                 | Deve essere supportato da qualsiasi filtro di ridimensionamento video personalizzato.                                                                          |
| [**ISampleGrabber**](isamplegrabber.md)                   | Recupera singoli campioni multimediali durante lo spostamento nel grafico dei filtri.                                                      |
| [**ISampleGrabberCB**](isamplegrabbercb.md)               | Interfaccia di callback per [**l'interfaccia ISampleGrabber.**](isamplegrabber.md)                                                 |
| [**ISmartRenderEngine**](ismartrenderengine.md)           | Fornisce metodi che supportano la ricompressione intelligente.                                                                             |
| [**IXml2Dex**](ixml2dex.md)                               | Salva e carica i file di progetto DES in Extensible Markup Language (XML).                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Informazioni di riferimento su C++ per la modifica di servizi](directshow-editing-services-c---reference.md)
</dt> </dl>

 

 



