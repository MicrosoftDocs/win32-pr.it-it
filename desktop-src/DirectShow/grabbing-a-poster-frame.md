---
description: Afferrare un frame poster
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Afferrare un frame poster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6668526d83f17c4ceab260f3a31ed43d19ec1d142bd8f8fdae080161350ded8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536571"
---
# <a name="grabbing-a-poster-frame"></a>Afferrare un frame poster

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Questo articolo descrive come visualizzare un frame poster da un file multimediale digitale usando l'oggetto [Media Detector (MediaDet)](media-detector--mediadet.md) fornito con servizi DirectShow [di modifica.](directshow-editing-services.md)

Media Detector è un oggetto helper che può ottenere informazioni sul formato da un file di origine multimediale. Può anche acquisire un'immagine bitmap da un flusso video nel file di origine. Supponendo che il file sia ricercabile, è possibile ottenere l'immagine da qualsiasi punto del file. L'immagine restituita è sempre in formato RGB a 24 bit.

Media Detector non è un filtro e l'applicazione non deve usare Gestione filtri Graph o creare un grafico filtri. Internamente, Media Detector crea un grafo di filtro contenente [**il filtro Grabber di esempio.**](sample-grabber-filter.md) Per ottenere una bitmap, Media Detector cerca e sospende il grafico dei filtri e quindi recupera la bitmap dal filtro Grabber di esempio. L'applicazione comunica con Media Detector tramite [**l'interfaccia IMediaDet.**](imediadet.md) Media Detector è un buon esempio di incapsulamento di un grafo di filtro all'interno di un oggetto helper, per proteggere le applicazioni dai dettagli correlati al grafo.

Media Detector funziona in due modalità. Quando viene creato per la prima volta, Media Detector è in modalità di "raccolta di informazioni". È possibile specificare il nome di un file multimediale e ottenere informazioni su ognuno dei flussi nel file, ad esempio il tipo di formato, la frequenza dei fotogrammi o la durata. Se il file contiene un flusso video, è possibile passare a Media Detector in modalità "grab bitmap" e recuperare bitmap dall'origine. Tuttavia, dopo questa operazione, non è possibile tornare alla modalità originale di Media Detector. è collegato in modo permanente a tale flusso video. Per usare un altro flusso o un altro file, è necessario creare una nuova istanza di Media Detector.

> [!Note]  
> Gli esempi di codice di questa esercitazione usano la classe **ATL CComPtr,** che gestisce automaticamente i conteggi dei riferimenti. Se si preferisce usare puntatori a interfaccia non elaborati, ricordarsi di rilasciare ogni interfaccia al termine dell'operazione. Inoltre, per brevità, gli esempi di codice omettono gran parte del controllo degli errori che un'applicazione deve eseguire. Nel codice funzionante controllare sempre i **valori HRESULT.**

 

Questa esercitazione include i passaggi seguenti:

-   [Passaggio 1: Creare Windows Framework](step-1--create-the-windows-framework.md)
-   [Passaggio 2: Aggiungere un comando di menu per afferrare un frame poster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [Passaggio 3: Implementare la funzione Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)
-   [Passaggio 4: Disegnare la bitmap nell'area client](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei DirectShow di modifica](using-directshow-editing-services.md)
</dt> </dl>

 

 



