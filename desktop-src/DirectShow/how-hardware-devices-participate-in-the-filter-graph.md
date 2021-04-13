---
description: Come i dispositivi hardware partecipano al grafico di filtro
ms.assetid: 27e1c097-9bb4-4f9c-b9f9-0d4225c0d290
title: Come i dispositivi hardware partecipano al grafico di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68794bbc046e633e9a435b2628a20b8ea8aab174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480740"
---
# <a name="how-hardware-devices-participate-in-the-filter-graph"></a>Come i dispositivi hardware partecipano al grafico di filtro

Questo articolo descrive il modo in cui DirectShow interagisce con hardware audio e video.

**Filtri wrapper**

Tutti i filtri DirectShow sono componenti software in modalità utente. Per consentire a un dispositivo hardware in modalità kernel, ad esempio una scheda di acquisizione video, di aggiungere un grafico filtro DirectShow, il dispositivo deve essere rappresentato come filtro in modalità utente. Questa funzione viene eseguita da filtri "wrapper" specializzati forniti con DirectShow. Questi filtri includono il filtro di [acquisizione audio](audio-capture.md) , il filtro di [acquisizione di VFW](vfw-capture-filter.md) , il filtro del [sintonizzatore TV](tv-tuner-filter.md) , il filtro [audio TV](tv-audio-filter.md) e il filtro per la [traversa video analogo](analog-video-crossbar-filter.md) . DirectShow fornisce anche un filtro denominato KsProxy, che può rappresentare qualsiasi tipo di dispositivo di streaming WDM (Windows Driver Model). I fornitori di hardware possono estendere KsProxy per supportare funzionalità personalizzate, fornendo un *plug-in ksproxy*, che è un oggetto com aggregato da ksproxy.

I filtri wrapper espongono interfacce COM che rappresentano le funzionalità del dispositivo. L'applicazione usa queste interfacce per passare informazioni da e verso il filtro. Il filtro converte le chiamate al metodo COM in chiamate al driver di dispositivo, le passa al driver in modalità kernel e quindi converte di nuovo il risultato nell'applicazione. Il sintonizzatore TV, audio TV, traversa video analogo e i filtri KsProxy supportano le proprietà del driver personalizzato tramite l'interfaccia [**IKsPropertySet**](ikspropertyset.md) . Il filtro di acquisizione VFW e il filtro di acquisizione audio non sono estendibili in questo modo.

Per gli sviluppatori di applicazioni, i filtri wrapper consentono all'applicazione di controllare i dispositivi così come controllano qualsiasi altro filtro DirectShow. Non è necessaria alcuna programmazione speciale. i dettagli della comunicazione con il dispositivo in modalità kernel vengono incapsulati all'interno del filtro.

**Video per i dispositivi Windows**

Il filtro di acquisizione VFW supporta le schede di acquisizione video for Windows (VfW) precedenti. Quando una scheda VfW è presente nel sistema di destinazione, può essere individuata e aggiunta al grafo del filtro usando l' [enumeratore del dispositivo di sistema](system-device-enumerator.md)DirectShow. Per informazioni dettagliate, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).

**Acquisizione e combinazione di dispositivi audio (schede audio)**

Le schede audio più recenti hanno Jack di input per i microfoni e altri tipi di dispositivi. In genere, queste schede dispongono anche di funzionalità di combinazione sul bordo per il controllo del volume, degli acuti e dei bassi di ogni singolo input. In DirectShow gli input e il mixer della scheda audio sono inclusi nel filtro di acquisizione audio. Ogni scheda audio può essere individuata con l'enumeratore di dispositivo di sistema. Per visualizzare le schede audio del sistema, eseguire GraphEdit e selezionare la categoria origini acquisizione audio. Ogni filtro in tale categoria è un'istanza separata del filtro di acquisizione audio. Vedere [uso di GraphEdit](using-graphedit.md).

**Dispositivi di streaming WDM**

I decodificatori hardware e le schede di acquisizione più recenti sono conformi alla specifica Windows Driver Model (WDM). Questi dispositivi hanno funzionalità maggiori rispetto ai dispositivi VfW. Le schede di acquisizione video WDM possono supportare funzionalità non disponibili in VfW, inclusa l'enumerazione dei formati di acquisizione, il controllo a livello di codice dei parametri video, ad esempio tonalità e luminosità, selezione input a livello di codice e supporto per sintonizzatori TV.

Per supportare i dispositivi di streaming WDM, DirectShow fornisce il filtro KsProxy (ksproxy.ax). KsProxy è stato chiamato "filtro coltelli svizzeri per l'esercito", perché esegue molte operazioni diverse. Il numero di pin sul filtro e il numero di interfacce COM esposte dal filtro dipendono dalle funzionalità del driver sottostante. KsProxy non viene visualizzato nel grafico del filtro sotto il nome "KsProxy". Accetta sempre il nome descrittivo del dispositivo, disponibile nel registro di sistema. Per visualizzare i dispositivi WDM nel sistema, eseguire GraphEdit e selezionare una delle categorie di streaming WDM. Anche se nel sistema è presente una sola scheda WDM, tale scheda potrebbe contenere più di un dispositivo. Ogni dispositivo è rappresentato come filtro separato e ognuno di questi filtri è effettivamente KsProxy.

Un'applicazione usa l'enumeratore di dispositivo di sistema per trovare i moniker del dispositivo WDM nel sistema. Viene creata un'istanza di KsProxy chiamando **BindToObject** sul moniker. Poiché KsProxy può rappresentare tutti i tipi di dispositivi WDM, deve eseguire una query sul driver per determinare quali proprietà sono supportate dal driver. I set di proprietà sono raccolte di strutture di dati utilizzate dai driver WDM e anche da alcuni filtri in modalità utente, ad esempio i decodificatori di software MPEG-2. KsProxy configura se stesso per esporre le interfacce COM che corrispondono a tali set di proprietà. KsProxy converte le chiamate al metodo COM in set di proprietà e le invia al driver. I fornitori di hardware possono estendere KsProxy fornendo plug-in, ovvero interfacce specifiche del fornitore che espongono le funzionalità speciali di un dispositivo. Tutti questi dettagli sono nascosti dall'applicazione. L'applicazione controlla il dispositivo tramite KsProxy, nello stesso modo di qualsiasi altro filtro DirectShow.

**Flusso del kernel**

I dispositivi WDM supportano lo streaming del kernel, in cui i dati vengono trasmessi interamente in modalità kernel senza mai passare alla modalità utente. Il cambio tra la modalità kernel e la modalità utente è costoso dal punto di vista del calcolo. il flusso del kernel consente velocità in bit elevate senza sovraccaricare la CPU dell'host. I filtri basati su WDM possono usare il flusso di kernel per passare i dati multimediali direttamente da un dispositivo hardware a un altro, sulla stessa scheda o su una scheda diversa, senza copiare i dati nella memoria principale del sistema.

Dal punto di vista di un'applicazione, viene visualizzato come se i dati fossero spostati da un filtro in modalità utente a quello successivo. In realtà, i dati potrebbero non passare mai alla modalità utente, ma possono essere trasmessi direttamente da un dispositivo in modalità kernel a un altro fino a quando non ne viene eseguito il rendering nella scheda video grafica. Alcuni scenari, ad esempio l'acquisizione in un file, richiedono che i dati vengano passati dalla modalità kernel alla modalità utente a un certo punto. Tuttavia, questa opzione non richiede necessariamente che i dati vengano copiati in una nuova posizione in memoria.

Gli sviluppatori di applicazioni in genere non devono preoccuparsi dei dettagli del flusso del kernel, ad eccezione delle informazioni complementari. Per informazioni più dettagliate su WDM, streaming kernel, KsProxy e argomenti correlati, vedere Microsoft DDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Il grafico del filtro e i relativi componenti](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



