---
description: Acquisizione di un frame di poster
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Acquisizione di un frame di poster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482693"
---
# <a name="grabbing-a-poster-frame"></a>Acquisizione di un frame di poster

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Questo articolo descrive come visualizzare un frame di poster da un file multimediale digitale, usando l'oggetto [mediadet (Media Detector)](media-detector--mediadet.md) fornito con i [servizi di modifica DirectShow](directshow-editing-services.md).

Il rilevatore multimediale è un oggetto helper che può ottenere informazioni sul formato da un file di origine multimediale. Può inoltre acquisire un'immagine bitmap da un flusso video nel file di origine. Supponendo che il file sia ricercabile, è possibile ottenere l'immagine da qualsiasi punto del file. L'immagine restituita è sempre in formato RGB a 24 bit.

Il rilevatore multimediale non è un filtro e non è necessario che l'applicazione usi Filter Graph Manager o crei un grafico di filtro. Internamente, il rilevatore multimediale crea un grafico di filtro che contiene il [**filtro Grabber di esempio**](sample-grabber-filter.md). Per ottenere una bitmap, il rilevatore multimediale Cerca e sospende il grafico del filtro e quindi recupera la bitmap dal filtro Grabber di esempio. L'applicazione comunica con il rilevatore multimediale tramite l'interfaccia [**IMediaDet**](imediadet.md) . Il rilevatore multimediale è un valido esempio di incapsulamento di un grafico di filtro all'interno di un oggetto helper, allo scopo di proteggere le applicazioni dai dettagli correlati al grafo.

Il rilevatore multimediale funziona in due modalità. Quando viene creata per la prima volta, il rilevatore multimediale si trova in modalità "raccolta informazioni". È possibile specificare il nome di un file multimediale e ottenere informazioni su ognuno dei flussi nel file, ad esempio il tipo di formato, la frequenza dei fotogrammi o la durata. Se il file contiene un flusso video, è possibile passare il rilevatore multimediale alla modalità "bitmap" e recuperare le bitmap dall'origine. Tuttavia, una volta eseguita questa operazione, non è possibile riportare il rilevatore multimediale alla modalità originale; viene collegato in modo permanente a tale flusso video. Per usare un altro flusso o un altro file, è necessario creare una nuova istanza del rilevamento multimediale.

> [!Note]  
> Gli esempi di codice in questa esercitazione usano la classe ATL **CComPtr** , che gestisce automaticamente i conteggi dei riferimenti. Se si preferisce usare i puntatori dell'interfaccia raw, ricordarsi di rilasciare ogni interfaccia al termine dell'operazione. Inoltre, per brevità gli esempi di codice omettono gran parte del controllo degli errori che un'applicazione deve eseguire. Nel codice funzionante, controllare sempre i valori **HRESULT** .

 

Questa esercitazione include i passaggi seguenti:

-   [Passaggio 1: creare il Framework Windows](step-1--create-the-windows-framework.md)
-   [Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [Passaggio 3: implementare la funzione Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)
-   [Passaggio 4: creare la bitmap nell'area client](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei servizi di modifica DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



