---
description: Copia e accesso ai dati delle risorse (Direct3D 10)
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: Copia e accesso ai dati delle risorse (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbe3ec1dc970635a08cea455927f21d8928f48d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466838"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>Copia e accesso ai dati delle risorse (Direct3D 10)

Non è più necessario pensare alle risorse create nella memoria video o nella memoria di sistema. O se il runtime deve gestire o meno la memoria. Grazie all'architettura del nuovo modello wddm (Windows Display Driver), le applicazioni creano [](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) ora risorse Direct3D 10 con flag di utilizzo diversi per indicare come l'applicazione intende usare i dati delle risorse. Il nuovo modello di driver virtualizza la memoria usata dalle risorse. diventa quindi responsabilità del sistema operativo/driver/gestione della memoria posizionare le risorse nell'area di memoria più performante possibile in base all'utilizzo previsto.

Il caso predefinito è che le risorse siano disponibili per la GPU. Naturalmente, detto questo, in alcuni casi i dati delle risorse devono essere disponibili per la CPU. La copia dei dati delle risorse in modo che il processore appropriato possa accedervi senza influire sulle prestazioni richiede una certa conoscenza del funzionamento dei metodi API.

-   [Copia dei dati delle risorse](#copying-and-accessing-resource-data-direct3d-10)
-   [Accesso ai dati delle risorse](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>Copia dei dati delle risorse

Le risorse vengono create in memoria quando Direct3D esegue una chiamata Create. Possono essere creati nella memoria video, nella memoria di sistema o in qualsiasi altro tipo di memoria. Poiché il modello di driver WDDM virtualizza questa memoria, le applicazioni non devono più tenere traccia del tipo di risorse di memoria in cui vengono create.

Idealmente, tutte le risorse si trovano nella memoria video in modo che la GPU possa accedervi immediatamente. Tuttavia, talvolta è necessario che la CPU letta i dati delle risorse o che la GPU accedono ai dati delle risorse in cui la CPU ha scritto. Direct3D 10 gestisce questi diversi scenari richiedendo all'applicazione di specificare un utilizzo e quindi offre diversi metodi per copiare i dati delle risorse quando necessario.

A seconda della modalità di creazione della risorsa, non è sempre possibile accedere direttamente ai dati sottostanti. Ciò può significare che i dati delle risorse devono essere copiati dalla risorsa di origine a un'altra risorsa accessibile dal processore appropriato. In termini di Direct3D 10, le risorse predefinite sono accessibili direttamente dalla GPU, le risorse dinamiche e di staging sono accessibili direttamente dalla CPU.

Dopo aver creato una risorsa, non [**è**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) possibile modificarne l'utilizzo. Copiare invece il contenuto di una risorsa in un'altra risorsa creata con un utilizzo diverso. Direct3D 10 offre questa funzionalità con tre metodi diversi. I primi due metodi( [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) sono progettati per copiare i dati delle risorse da una risorsa a un'altra. Il terzo metodo ([**ID3D10Device::UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) è progettato per copiare dati dalla memoria a una risorsa.

Esistono due tipi principali di risorse: mappabile e non mappabile. Le risorse create con utilizzi dinamici o di staging sono mappabili, mentre le risorse create con utilizzi predefiniti o non modificabili non sono mappabili.

La copia di dati tra risorse non mappabili è molto veloce perché questo è il caso più comune ed è stato ottimizzato per prestazioni ottimizzate. Poiché queste risorse non sono direttamente accessibili dalla CPU, sono ottimizzate in modo che la GPU possa modificarle rapidamente.

La copia di dati tra risorse mappabili è più problematica perché le prestazioni dipendono dall'utilizzo con cui è stata creata la risorsa. Ad esempio, la GPU può leggere una risorsa dinamica abbastanza rapidamente, ma non può scrivervi e la GPU non può leggere o scrivere direttamente nelle risorse di staging.

Le applicazioni che vogliono copiare dati da una risorsa con utilizzo predefinito a una risorsa con utilizzo di staging (per consentire alla CPU di leggere i dati, ad esempio il problema di readback della GPU), devono eseguire questa operazione con cautela. Per altre informazioni su questo ultimo [caso,](#copying-and-accessing-resource-data-direct3d-10) vedere Accesso ai dati delle risorse.

## <a name="accessing-resource-data"></a>Accesso ai dati delle risorse

Per accedere a una risorsa è necessario eseguire il mapping della risorsa. mapping significa essenzialmente che l'applicazione sta tentando di concedere alla CPU l'accesso alla memoria. Il processo di mapping di una risorsa in modo che la CPU possa accedere alla memoria sottostante può causare alcuni colli di bottiglia delle prestazioni e per questo motivo è necessario fare attenzione a come e quando eseguire questa attività.

Le prestazioni possono arrestarsi se l'applicazione tenta di eseguire il mapping di una risorsa nel momento errato. Se l'applicazione tenta di accedere ai risultati di un'operazione prima del termine dell'operazione, si verificherà uno stallo della pipeline.

L'esecuzione di un'operazione di mapping nel momento errato potrebbe causare un calo grave delle prestazioni forzando la sincronizzazione tra GPU e CPU. Questa sincronizzazione si verifica se l'applicazione vuole accedere a una risorsa prima che la GPU finirà di copiarla in una risorsa che può essere mappata dalla CPU.

La CPU può leggere solo dalle risorse create con il flag D3D10 \_ USAGE \_ STAGING. Poiché le risorse create con questo flag non possono essere impostate come output della pipeline, se la CPU vuole leggere i dati in una risorsa generata dalla GPU, i dati devono essere copiati in una risorsa creata con il flag di staging. L'applicazione può eseguire questa operazione usando i metodi [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) per copiare il contenuto di una risorsa in un'altra. L'applicazione può quindi ottenere l'accesso a questa risorsa chiamando il metodo Map appropriato. Quando l'accesso alla risorsa non è più necessario, l'applicazione deve chiamare il metodo Unmap corrispondente. Ad esempio, [**ID3D10Texture2D::Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) e [**ID3D10Texture2D::Unmap**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap). I diversi metodi Map restituiscono alcuni valori specifici a seconda dei flag di input. Per [**informazioni dettagliate, vedere la sezione Note**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map) sulla mappa.

> [!Note]  
> Quando l'applicazione chiama il metodo Map, riceve un puntatore ai dati della risorsa a cui accedere. Il runtime garantisce che il puntatore abbia un allineamento specifico, a seconda del [livello di funzionalità](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md). Per [**D3D \_ FEATURE LEVEL \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) e versioni successive, il puntatore è allineato a 16 byte. Per un valore inferiore a [**D3D \_ FEATURE \_ LEVEL \_ 10 \_ 0,**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level)il puntatore è allineato a 4 byte. L'allineamento a 16 byte consente all'applicazione di eseguire operazioni ottimizzate [per SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))sui dati in modo nativo, senza riallineamento o copia.

 

### <a name="performance-considerations"></a>Considerazioni sulle prestazioni

È meglio pensare a un PC come a un computer in esecuzione come un'architettura parallela con due tipi principali di processori: uno o più CPU e uno o più GPU. Come in qualsiasi architettura parallela, le prestazioni migliori si ottiene quando ogni processore è pianificato con attività sufficienti per impedirne l'inattività e quando il lavoro di un processore non è in attesa sul lavoro di un altro.

Lo scenario peggiore per il parallelismo GPU/CPU è la necessità di forzare un processore ad attendere i risultati del lavoro eseguito da un altro. Direct3D 10 prova a rimuovere questo costo rendendo asincroni i metodi [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**ID3D10Device::CopySubresourceRegion.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) la copia non è necessariamente stata eseguita nel momento in cui il metodo viene restituito. Il vantaggio di questo è che l'applicazione non paga il costo delle prestazioni della copia dei dati fino a quando la CPU non accede ai dati, ovvero quando viene chiamato Map. Se il metodo Map viene chiamato dopo la copia dei dati, non si verifica alcuna perdita di prestazioni. D'altra parte, se il metodo Map viene chiamato prima che i dati siano stati copiati, si verificherà uno stallo della pipeline.

Le chiamate asincrone in Direct3D 10 (che sono la maggior parte dei metodi e in particolare le chiamate di rendering) vengono archiviate in quello che viene chiamato buffer dei comandi. Questo buffer è interno al driver di grafica e viene usato per eseguire chiamate in batch all'hardware sottostante in modo che il passaggio dis costoso dalla modalità utente alla modalità kernel in Microsoft Windows si verifichi il più raramente possibile.

Il buffer dei comandi viene scaricato, causando un'opzione in modalità utente/kernel, in una delle quattro situazioni seguenti.

1.  [**Viene chiamato**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) Present.
2.  [**Viene chiamato ID3D10Device::Flush.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush)
3.  Il buffer dei comandi è pieno. le dimensioni sono dinamiche ed è controllata dal sistema operativo e dal driver di grafica.
4.  La CPU richiede l'accesso ai risultati di un comando in attesa di essere eseguito nel buffer dei comandi.

Delle quattro situazioni precedenti, il numero quattro è il più critico per le prestazioni. Se l'applicazione invia una chiamata [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device::CopySubresourceRegion,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) questa chiamata viene accodata nel buffer dei comandi. Se l'applicazione prova quindi a eseguire il mapping della risorsa di staging che era la destinazione della chiamata di copia prima che il buffer dei comandi sia stato scaricato, si verificherà un blocco della pipeline perché non solo deve essere eseguita la chiamata al metodo Copy, ma anche tutti gli altri comandi memorizzati nel buffer dei comandi. In questo modo la GPU e la CPU verranno sincronizzate perché la CPU sarà in attesa di accedere alla risorsa di staging mentre la GPU svuota il buffer dei comandi e infine riempie la risorsa richiesta dalla CPU. Al termine della copia, la CPU inizierà ad accedere alla risorsa di staging, ma durante questo periodo la GPU sarà inattiva.

Questa operazione spesso in fase di esecuzione riduce gravemente le prestazioni. Per questo motivo, il mapping delle risorse create con l'utilizzo predefinito deve essere eseguito con cautela. L'applicazione deve attendere un tempo sufficiente per svuotare il buffer dei comandi e quindi completare l'esecuzione di tutti questi comandi prima di tentare di eseguire il mapping della risorsa di staging corrispondente. Per quanto tempo l'applicazione deve attendere? Almeno due frame perché ciò consentirà di sfruttare al massimo il parallelismo tra le CPU e la GPU. Il funzionamento della GPU è che mentre l'applicazione elabora il frame N inviando chiamate al buffer dei comandi, la GPU è occupata nell'esecuzione delle chiamate dal frame precedente, N-1.

Pertanto, se un'applicazione vuole eseguire il mapping di una risorsa che ha origine nella memoria video e chiama [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) nel frame N, questa chiamata inizierà effettivamente a essere eseguita nel frame N+1, quando l'applicazione invia chiamate per il fotogramma successivo. La copia deve essere completata quando l'applicazione elabora il frame N+2.




| Frame | Stato GPU/CPU | 
|-------|----------------|
| N | <ul><li>La CPU esegue il rendering delle chiamate per il frame corrente.</li></ul> | 
| N+1 | <ul><li>GPU che esegue le chiamate inviate dalla CPU durante il frame N.</li><li>La CPU esegue il rendering delle chiamate per il frame corrente.</li></ul> | 
| N+2 | <ul><li>GPU ha terminato l'esecuzione delle chiamate inviate dalla CPU durante il frame N. Risultati pronti.</li><li>GPU che esegue le chiamate inviate dalla CPU durante il frame N+1.</li><li>La CPU esegue il rendering delle chiamate per il frame corrente.</li></ul> | 
| N+3 | <ul><li>GPU ha terminato l'esecuzione delle chiamate inviate dalla CPU durante il frame N+1. Risultati pronti.</li><li>GPU che esegue chiamate inviate dalla CPU durante il frame N+2.</li><li>La CPU esegue il rendering delle chiamate per il frame corrente.</li></ul> | 
| N+4 | ... | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
