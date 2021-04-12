---
description: Filtri di acquisizione video DirectShow
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: Filtri di acquisizione video DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f18dd77bc40011fa9fc0dbab3192ea81a223f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480876"
---
# <a name="directshow-video-capture-filters"></a>Filtri di acquisizione video DirectShow

I filtri di acquisizione in DirectShow hanno alcune funzionalità che li distinguono da altri tipi di filtri. Sebbene il [Generatore di grafici di acquisizione](capture-graph-builder.md) nasconda molti dei dettagli, è consigliabile leggere questa sezione per avere una conoscenza generale dei grafici di acquisizione DirectShow.

**Aggiungi categorie**

Un filtro di acquisizione ha spesso due o più pin di output che forniscono lo stesso tipo di dati, ad esempio un pin di anteprima e un pin di acquisizione. Pertanto, i tipi di supporto non sono un metodo efficace per distinguere i pin. I pin sono invece distinti dalla relativa funzionalità, che viene identificata usando un GUID, denominato *categoria pin*.

Per informazioni su come eseguire query sui pin per la relativa categoria, vedere [Working with pin Categories](working-with-pin-categories.md). Per la maggior parte delle applicazioni, tuttavia, non sarà necessario eseguire query direttamente sui pin. Al contrario, diversi metodi [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) accettano parametri che specificano la categoria di pin su cui operare. Il generatore del grafico di acquisizione individua automaticamente il PIN corretto.

**Pin di anteprima e pin di acquisizione**

Alcuni dispositivi di acquisizione video hanno PIN di output distinti per l'anteprima e l'acquisizione. Il pin di anteprima viene usato per eseguire il rendering del video sullo schermo, mentre il pin di acquisizione viene usato per scrivere video in un file.

Un pin di anteprima e un pin di acquisizione presentano le differenze seguenti:

-   Un pin di anteprima Elimina i frame necessari per mantenere la velocità effettiva sul pin di acquisizione.
-   Ogni fotogramma di un pin di acquisizione viene stampato con l'ora del flusso in cui è stato acquisito il frame. Un pin di anteprima non rilascia il timestamp degli esempi forniti.

Il motivo per cui i frame di anteprima non hanno timestamp è che il grafico del filtro introduce una piccola quantità di latenza nel flusso. Se il tempo di acquisizione viene usato come ora di presentazione, il renderer video considera ogni campione come leggermente tardivo. In questo modo il renderer video può rilasciare frame mentre tenta di aggiornarsi. La rimozione dei timestamp garantisce che il renderer presenti ogni campione al momento dell'arrivo senza eliminare i frame.

La categoria pin per i pin di anteprima è la \_ categoria pin \_ Preview. La categoria per i pin di acquisizione è l' \_ acquisizione della categoria pin \_ .

**PIN della porta video**

Una porta video è una connessione hardware tra un dispositivo video, ad esempio un sintonizzatore TV analogico, e la scheda video. Una porta video consente al dispositivo di inviare dati video direttamente alla scheda grafica. Il video viene visualizzato sullo schermo usando una sovrapposizione hardware. Una porta video potrebbe essere un cavo effettivo che connette due dispositivi a schede separate; oppure potrebbe trattarsi di una connessione cablata sulla stessa scheda.

Il vantaggio di una porta video è che il video passa direttamente alla memoria video, senza alcuna attività da parte della CPU. Tuttavia, le porte video presentano alcuni svantaggi:

-   Una porta video usa sempre la superficie della sovrimpressione durante l'acquisizione, indipendentemente dal fatto che si desideri visualizzare l'anteprima del video.
-   Il capovolgimento tra i frame viene eseguito automaticamente, rendendo difficile la sincronizzazione del flip con altre operazioni video.

Se un dispositivo di acquisizione usa una porta video, il filtro di acquisizione ha un PIN della porta video anziché un pin di anteprima. La categoria pin per i pin della porta video è PIN \_ categoria \_ VIDEOPORT.

Ogni filtro di acquisizione include almeno un pin di acquisizione. Potrebbe inoltre avere un pin di anteprima o un PIN della porta video, ma mai entrambi. I filtri possono avere più pin di acquisizione e pin di anteprima, ognuno dei quali fornisce un tipo di supporto separato. Un singolo filtro potrebbe quindi avere un pin di acquisizione video, un pin di anteprima video, un pin di acquisizione audio e un pin di anteprima audio. (Tuttavia, non esiste alcun equivalente a una porta video per l'audio).

**Filtri WDM upstream**

I dispositivi Windows Driver Model (WDM) potrebbero richiedere filtri aggiuntivi upstream dal filtro di acquisizione. Questi filtri includono quanto segue:

-   [Filtro sintonizzatore TV](tv-tuner-filter.md). Controlla l'ottimizzazione dei sintonizzatori TV analoghi.
-   [Filtro audio TV](tv-audio-filter.md). Controlla le impostazioni audio per i sintonizzatori TV analoghi.
-   [Filtro traversa video analogo](analog-video-crossbar-filter.md). Instrada i segnali video e audio tramite il dispositivo hardware. Ad esempio, un dispositivo potrebbe avere più input, ad esempio S-video e composite video. Il filtro traversa consente all'applicazione di selezionare l'input.

Sebbene si tratta di filtri distinti in DirectShow, rappresentano in genere lo stesso dispositivo hardware. Ogni filtro controlla una funzione diversa del dispositivo. I filtri sono connessi tramite PIN, ma non vengono spostati dati multimediali tra le connessioni pin. Pertanto, i pin su questi filtri non si connettono stabilendo un tipo di supporto. Usano invece valori GUID denominati *medium*. I GUID medi sono definiti in modo univoco per un determinato dispositivo minidriver. Ad esempio, il filtro del sintonizzatore TV e il filtro di acquisizione video per la stessa scheda TV supporteranno lo stesso supporto, che consente all'applicazione di compilare correttamente il grafo.

In pratica, fino a quando si usa **ICaptureGraphBuilder2** per compilare i grafici di acquisizione, questi filtri vengono aggiunti automaticamente al grafico. Per una descrizione più dettagliata, vedere la pagina relativa ai [filtri driver di classe WDM](wdm-class-driver-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su acquisizione video in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



