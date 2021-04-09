---
description: Creazione di oggetti flusso multimediale ed esempi di flusso
ms.assetid: 1aecdd39-f1b3-490b-b092-86d51439be02
title: Creazione di oggetti flusso multimediale ed esempi di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cdc30129591bf1c67609ad6d15e8fd8286ae23
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968918"
---
# <a name="creating-multimedia-stream-objects-and-stream-samples"></a>Creazione di oggetti flusso multimediale ed esempi di flusso

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.

 

Gli oggetti che supportano l'interfaccia [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) sono i contenitori di base per i flussi di dati multimediali. L'interfaccia **IMultiMediaStream** include metodi che enumerano i flussi di dati dell'oggetto; si tratta in genere di dati audio e video, ma possono includere dati di qualsiasi formato, ad esempio sottotitoli codificati, testo normale o timecode SMPTE. Tuttavia, l'interfaccia **IMultiMediaStream** è un contenitore generico. gli sviluppatori possono creare altre versioni dell'interfaccia che supportano formati di dati specifici. Gli oggetti che implementano l'interfaccia [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) , ad esempio, possono enumerare e controllare i flussi di qualsiasi formato di dati DirectShow. Poiché i singoli flussi di dati sono specifici del formato, supportano almeno due interfacce diverse: una generica e una specifica per i dati. Ogni flusso supporta l'interfaccia [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) , che fornisce i metodi per recuperare il formato e un puntatore al flusso stesso. L'interfaccia [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) , d'altra parte, dispone di metodi che gestiscono in modo specifico il rendering dei dati video. Qualsiasi interfaccia derivata da **IMultiMediaStream** supporta anche la creazione di esempi di flusso, ovvero le unità di base dei dati di streaming.

Un esempio multimediale è un riferimento a un oggetto contenente i dati multimediali. Per un'immagine video, si tratta di una superficie DirectDraw. Il contenuto esatto dell'esempio varia a seconda del tipo di supporto (audio, testo e così via). Poiché un esempio è solo un riferimento all'oggetto dati, un numero qualsiasi di esempi di flusso può fare riferimento allo stesso oggetto. L'interfaccia [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) fornisce metodi che ottengono e impostano le caratteristiche di un campione, ad esempio l'ora di inizio e di fine, lo stato e l'associazione del flusso. Il metodo [**IStreamSample:: Update aggiorna**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) i dati dell'esempio in caso di flussi leggibili. Per i flussi scrivibili, i dati dell'esempio vengono scritti nel flusso. In genere, si usa il metodo **Update** in un ciclo che esegue il rendering, trasferisce o archivia i dati di streaming.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'architettura di streaming multimediale](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



