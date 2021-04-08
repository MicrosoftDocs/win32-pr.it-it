---
description: Interfacce per i servizi di modifica DirectShow
ms.assetid: e7fdb387-83b3-4fa2-9608-2f5dc95975bf
title: Interfacce per i servizi di modifica DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba286a340693407287ed370ed401ac6b039593c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747111"
---
# <a name="interfaces-for-directshow-editing-services"></a>Interfacce per i servizi di modifica DirectShow

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Questa sezione contiene argomenti di riferimento per le interfacce di [servizi di modifica DirectShow](directshow-editing-services.md) (des).



| Interfaccia                                                  | Descrizione                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IAMErrorLog**](iamerrorlog.md)                         | Fornisce un metodo di callback per la registrazione degli errori.                                                                                  |
| [**IAMSetErrorLog**](iamseterrorlog.md)                   | Imposta o recupera un log degli errori.                                                                                                |
| [**IAMTimeline**](iamtimeline.md)                         | Fornisce metodi per la modifica della sequenza temporale.                                                                                |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Inserisce o recupera tracce virtuali in una composizione.                                                                          |
| [**IAMTimelineEffect**](iamtimelineeffect.md)             | Fornisce metodi per la modifica degli effetti della sequenza temporale.                                                                            |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | Fornisce metodi per l'aggiunta di effetti a un oggetto della sequenza temporale.                                                                      |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Imposta e recupera le proprietà nei gruppi.                                                                                       |
| [**IAMTimelineObj**](iamtimelineobj.md)                   | Fornisce metodi per la modifica degli oggetti della sequenza temporale.                                                                            |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | Suddivide un oggetto della sequenza temporale.                                                                                                      |
| [**IAMTimelineSrc**](iamtimelinesrc.md)                   | Fornisce metodi per la modifica e l'impostazione delle proprietà negli oggetti di origine.                                                    |
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Fornisce metodi per la modifica di oggetti Track.                                                                               |
| [**IAMTimelineTrans**](iamtimelinetrans.md)               | Fornisce metodi per la modifica degli oggetti di transizione.                                                                          |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | Aggiunge transizioni a un oggetto.                                                                                                 |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Fornisce metodi per l'utilizzo di tracce virtuali.                                                                              |
| [**IDxtAlphaSetter**](idxtalphasetter.md)                 | Imposta le proprietà sull'effetto del [Setter alfa](alpha-setter-effect.md) .                                                         |
| [**IDxtCompositor**](idxtcompositor.md)                   | Imposta le proprietà nella transizione del [compositor](compositor-transition.md) .                                                     |
| [**IDxtJpeg**](idxtjpeg.md)                               | Imposta le proprietà nella transizione di [cancellazione SMPTE](smpte-wipe-transition.md) .                                                     |
| [**IDxtKey**](idxtkey.md)                                 | Imposta le proprietà della transizione della [chiave](key-transition.md) .                                                                   |
| [**IFindCompressorCB**](ifindcompressorcb.md)             | Non supportata.                                                                                                                 |
| [**IGrfCache**](igrfcache.md)                             | Non supportata.                                                                                                                 |
| [**IMediaDet**](imediadet.md)                             | Recupera le informazioni su un file multimediale, ad esempio il numero di flussi e il tipo, la durata e la frequenza dei fotogrammi di ogni flusso. |
| [**IMediaLocator**](imedialocator.md)                     | Fornisce metodi per la convalida dei nomi di file.                                                                                    |
| [**IPropertySetter**](ipropertysetter.md)                 | Imposta le proprietà per un effetto o una transizione.                                                                                    |
| [**IRenderEngine**](irenderengine.md)                     | Esegue il rendering di un progetto DES costruendo un grafico di filtro da una sequenza temporale.                                                          |
| [**IRenderEngine2**](irenderengine2.md)                   | Consente all'applicazione di sostituire il filtro di ridimensionamento video predefinito usato da DES.                                              |
| [**IResize**](iresize.md)                                 | Deve essere supportato da qualsiasi filtro di ridimensionamento video personalizzato.                                                                          |
| [**ISampleGrabber**](isamplegrabber.md)                   | Recupera singoli esempi di supporti durante il passaggio del grafico del filtro.                                                      |
| [**ISampleGrabberCB**](isamplegrabbercb.md)               | Interfaccia di callback per l'interfaccia [**ISampleGrabber**](isamplegrabber.md) .                                                 |
| [**ISmartRenderEngine**](ismartrenderengine.md)           | Fornisce metodi che supportano la ricompressione intelligente.                                                                             |
| [**IXml2Dex**](ixml2dex.md)                               | Salva e carica i file di progetto DES in Extensible Markup Language (XML).                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimenti per la modifica di DirectShow Services C++](directshow-editing-services-c---reference.md)
</dt> </dl>

 

 



