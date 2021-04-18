---
description: Architettura di servizi di modifica DirectShow
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Architettura di servizi di modifica DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303779"
---
# <a name="directshow-editing-services-architecture"></a>Architettura di servizi di modifica DirectShow

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Nella figura seguente è illustrata l'architettura dei [servizi di modifica DirectShow](directshow-editing-services.md) (des).

![architettura di servizi di modifica DirectShow](images/architecture.png)

-   Sequenza temporale: rappresenta una produzione video come raccolta di clip di origine, transizioni ed effetti, organizzati in un set di tracce nidificate. Per ulteriori informazioni, vedere [il modello di sequenza temporale](the-timeline-model.md).
-   Parser XML: analizza la sequenza temporale e genera un file di output oppure legge un file di input e genera una sequenza temporale. DES supporta un formato di persistenza basato su XML.
-   Motore di rendering: converte la sequenza temporale in un modulo di cui è possibile eseguire il rendering come flussi multimediali. Per impostazione predefinita, il motore di rendering genera un grafico di filtro DirectShow (vedere la sezione successiva).
-   Media Locator: mantiene una cache di posizioni di elementi multimediali. Quando un tentativo di apertura di un elemento multimediale ha esito negativo, DES usa la cache per individuare l'elemento, in base a una cronologia di apertura riuscita.

La sequenza temporale è una descrizione astratta di un progetto di modifica video. Specifica le clip di origine utilizzate nel progetto, le ore di inizio e di fine, gli effetti e le transizioni e così via. Tuttavia, la sequenza temporale non esegue il rendering dei flussi video e audio. Al contrario, il motore di rendering converte la sequenza temporale in un grafico di filtro, sia per l'anteprima che per l'output del file. Un'applicazione modifica la sequenza temporale anziché modificare direttamente il grafico del filtro, operazione complessa e soggetta a errori.

Nella tabella seguente sono elencate le attività principali eseguite da una tipica applicazione di modifica video, insieme alle interfacce che supportano ogni attività. Le sezioni successive descrivono queste attività e le interfacce in modo più dettagliato.



| Attività                                     | Interfaccia/e                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| Creare o modificare una sequenza temporale.          | [**IAMTimeline**](iamtimeline.md) e altre interfacce **IAMTimelineXXXX**          |
| Salvare e caricare i file di progetto.             | [**IXml2Dex**](ixml2dex.md)                                                             |
| Visualizzare in anteprima un progetto o scriverlo in un file. | [**IRenderEngine**](irenderengine.md), [ **ISmartRenderEngine**](ismartrenderengine.md) |



 

Inoltre, un'applicazione può eseguire alcune o tutte le attività secondarie riportate di seguito.



| Attività                                                                                           | Interfaccia/e                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Ottenere informazioni sui file multimediali. (Numero di flussi, formato e durata di ogni flusso). | [**IMediaDet**](imediadet.md)                                               |
| Impostare le proprietà per transizioni ed effetti.                                                     | [**IPropertySetter**](ipropertysetter.md)                                   |
| Ricevere una notifica quando si verificano errori durante il rendering.                                       | [**IAMSetErrorLog**](iamseterrorlog.md), [ **IAMErrorLog**](iamerrorlog.md) |
| Recuperare i frame del poster.                                                                        | [**IMediaDet**](imediadet.md), [ **ISampleGrabber**](isamplegrabber.md)     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con i servizi di modifica DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



