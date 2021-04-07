---
description: Copia e accesso ai dati delle risorse (Direct3D 10)
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: Copia e accesso ai dati delle risorse (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bd075585ee3123e163075a50b06b53a77a214c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748519"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>Copia e accesso ai dati delle risorse (Direct3D 10)

Non è più necessario considerare le risorse come create nella memoria del video o nella memoria di sistema. O se il runtime deve gestire la memoria. Grazie all'architettura del nuovo WDDM (Windows Display Driver Model), le applicazioni creano ora risorse Direct3D 10 con flag di [**utilizzo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) diversi per indicare in che modo l'applicazione intende usare i dati delle risorse. Il nuovo modello di driver virtualizza la memoria usata dalle risorse; quindi diventa la responsabilità del sistema operativo/driver/Memory Manager di posizionare le risorse nell'area di memoria più efficiente possibile in base all'utilizzo previsto.

Il caso predefinito è che le risorse siano disponibili per la GPU. Ovviamente, in alcuni casi è necessario che i dati delle risorse siano disponibili per la CPU. La copia dei dati delle risorse in modo che il processore appropriato possa accedervi senza conseguenze sulle prestazioni richiede una certa conoscenza del funzionamento dei metodi API.

-   [Copia dei dati delle risorse](#copying-and-accessing-resource-data-direct3d-10)
-   [Accesso ai dati delle risorse](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>Copia dei dati delle risorse

Le risorse vengono create in memoria quando Direct3D esegue una chiamata di creazione. Possono essere creati in memoria video, memoria di sistema o qualsiasi altro tipo di memoria. Poiché il modello di driver WDDM virtualizza questa memoria, le applicazioni non devono più tenere traccia del tipo di risorse di memoria creato in.

Idealmente, tutte le risorse si trovano nella memoria video, in modo che la GPU possa avere accesso immediato. Tuttavia, è talvolta necessario che la CPU legga i dati delle risorse o che la GPU acceda ai dati delle risorse in cui la CPU ha scritto. Direct3D 10 gestisce questi diversi scenari richiedendo all'applicazione di specificare un utilizzo e quindi offre diversi metodi per la copia dei dati delle risorse, quando necessario.

A seconda di come è stata creata la risorsa, non è sempre possibile accedere direttamente ai dati sottostanti. Questo può significare che i dati della risorsa devono essere copiati dalla risorsa di origine a un'altra risorsa accessibile dal processore appropriato. In termini di Direct3D 10, è possibile accedere alle risorse predefinite direttamente dalla GPU, le risorse dinamiche e di staging possono accedere direttamente alla CPU.

Una volta creata una risorsa, non è possibile modificarne l' [**utilizzo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) . Copiare invece il contenuto di una risorsa in un'altra risorsa creata con un utilizzo diverso. Direct3D 10 offre questa funzionalità con tre metodi diversi. I primi due metodi ( [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) sono progettati per copiare i dati delle risorse da una risorsa a un'altra. Il terzo metodo ([**ID3D10Device:: UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) è progettato per copiare i dati dalla memoria a una risorsa.

Esistono due tipi principali di risorse: mappabili e non mappabili. Le risorse create con gli utilizzi dinamici o di gestione temporanea sono mappabili, mentre le risorse create con utilizzi predefiniti o non modificabili non sono mappabili.

La copia dei dati tra le risorse non mappabili è molto rapida perché questo è il caso più comune ed è stato ottimizzato per prestazioni ottimali. Poiché queste risorse non sono direttamente accessibili dalla CPU, sono ottimizzate in modo che la GPU possa manipolarle rapidamente.

La copia dei dati tra le risorse di mappabili è più problematica, perché le prestazioni variano a seconda dell'utilizzo con cui è stata creata la risorsa. La GPU, ad esempio, è in grado di leggere una risorsa dinamica abbastanza rapidamente, ma non di scrivervi, e la GPU non è in grado di leggere o scrivere direttamente nelle risorse di staging.

Le applicazioni che desiderano copiare i dati da una risorsa con utilizzo predefinito a una risorsa con utilizzo di gestione temporanea (per consentire alla CPU di leggere i dati, ad esempio il problema readback GPU), devono eseguire questa operazione con cautela. Per ulteriori informazioni sull'ultimo caso, vedere [accesso ai dati delle risorse](#copying-and-accessing-resource-data-direct3d-10) .

## <a name="accessing-resource-data"></a>Accesso ai dati delle risorse

Per accedere a una risorsa, è necessario mappare la risorsa; il mapping significa essenzialmente che l'applicazione sta tentando di concedere alla CPU l'accesso alla memoria. Il processo di mapping di una risorsa in modo che la CPU possa accedere alla memoria sottostante può causare alcuni colli di bottiglia delle prestazioni e per questo motivo è necessario prestare attenzione a come e quando eseguire questa attività.

Se l'applicazione tenta di eseguire il mapping di una risorsa in un momento errato, le prestazioni possono essere interrotte. Se l'applicazione tenta di accedere ai risultati di un'operazione prima del completamento dell'operazione, si verificherà un blocco della pipeline.

L'esecuzione di un'operazione di mapping in un momento errato potrebbe causare un calo grave delle prestazioni forzando la sincronizzazione della GPU e della CPU. Questa sincronizzazione si verificherà se l'applicazione vuole accedere a una risorsa prima che la GPU venga completata la copia in una risorsa di cui è possibile eseguire il mapping della CPU.

La CPU può leggere solo da risorse create con il \_ flag di gestione temporanea dell'utilizzo di D3D10 \_ . Poiché le risorse create con questo flag non possono essere impostate come output della pipeline, se la CPU vuole leggere i dati in una risorsa generata dalla GPU, i dati devono essere copiati in una risorsa creata con il flag di gestione temporanea. L'applicazione può eseguire questa operazione usando i metodi [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) per copiare il contenuto di una risorsa in un'altra. L'applicazione può quindi ottenere l'accesso a questa risorsa chiamando il metodo map appropriato. Quando l'accesso alla risorsa non è più necessario, l'applicazione deve chiamare il metodo annullare corrispondente. Ad esempio, [**ID3D10Texture2D:: Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) e [**ID3D10Texture2D:: annullare**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap). I diversi metodi della mappa restituiscono alcuni valori specifici a seconda dei flag di input. Per informazioni dettagliate, vedere la [**sezione Note sulla mappa**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map) .

> [!Note]  
> Quando l'applicazione chiama il metodo map, riceve un puntatore ai dati della risorsa a cui accedere. Il runtime garantisce che il puntatore abbia un allineamento specifico, a seconda del [livello di funzionalità](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md). Per [**il \_ livello di funzionalità D3D \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) e superiore, il puntatore è allineato a 16 byte. Per un livello di funzionalità inferiore a quello di [**D3D \_ \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level), il puntatore è allineato a 4 byte. L'allineamento a 16 byte consente all'applicazione di eseguire operazioni ottimizzate per [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))sui dati in modo nativo, senza riallineamento o copia.

 

### <a name="performance-considerations"></a>Considerazioni sulle prestazioni

È consigliabile considerare un PC come un computer in esecuzione come un'architettura parallela con due tipi principali di processori: uno o più CPU e una o più GPU. Come in qualsiasi architettura parallela, si ottengono le migliori prestazioni quando ogni processore è pianificato con un numero sufficiente di attività per impedirne l'inattività e quando il lavoro di un processore non è in attesa di un altro processore.

Lo scenario peggiore per il parallelismo GPU/CPU è la necessità di forzare un processore ad attendere i risultati del lavoro eseguito da un altro. Direct3D 10 tenta di rimuovere questo costo rendendo asincrono i metodi [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) ; la copia non è stata necessariamente eseguita nel momento in cui il metodo restituisce. Il vantaggio è che l'applicazione non paga il costo delle prestazioni di copia effettiva dei dati fino a quando la CPU non accede ai dati, ovvero quando viene chiamata la mappa. Se il metodo map viene chiamato dopo che i dati sono stati effettivamente copiati, non si verificherà alcuna perdita di prestazioni. D'altra parte, se viene chiamato il metodo map prima che i dati vengano copiati, si verificherà uno stallo della pipeline.

Le chiamate asincrone in Direct3D 10, ovvero la maggior parte dei metodi e in particolare le chiamate di rendering, vengono archiviate in ciò che viene definito buffer dei comandi. Questo buffer è interno al driver della grafica e viene usato per eseguire il batch delle chiamate all'hardware sottostante, in modo che il costo del passaggio dalla modalità utente alla modalità kernel in Microsoft Windows avvenga il più raramente possibile.

Il buffer dei comandi viene scaricato, causando un cambio di modalità utente/kernel, in una delle quattro situazioni seguenti.

1.  [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) viene chiamato.
2.  Viene chiamato [**ID3D10Device:: Flush**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush) .
3.  Il buffer dei comandi è pieno. le sue dimensioni sono dinamiche e sono controllate dal sistema operativo e dal driver della grafica.
4.  La CPU richiede l'accesso ai risultati di un comando in attesa di esecuzione nel buffer dei comandi.

Tra le quattro situazioni precedenti, il numero quattro è la più critica per le prestazioni. Se l'applicazione rilascia una chiamata [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) , questa chiamata viene accodata nel buffer dei comandi. Se l'applicazione tenta quindi di eseguire il mapping della risorsa di gestione temporanea che era la destinazione della chiamata di copia prima che il buffer del comando venisse scaricato, si verificherà uno stallo della pipeline perché non solo la chiamata al metodo di copia deve essere eseguita, ma anche tutti gli altri comandi memorizzati nel buffer nel buffer dei comandi. Questa operazione causerà la sincronizzazione della GPU e della CPU, perché la CPU sarà in attesa di accedere alla risorsa di staging mentre la GPU svuoterà il buffer dei comandi e riempirà infine la risorsa necessaria per la CPU. Al termine della copia, la CPU inizierà ad accedere alla risorsa di staging, ma durante questo periodo la GPU resterà inattiva.

Questa operazione di frequente in fase di esecuzione provocherà un grave peggioramento delle prestazioni. Per questo motivo, il mapping delle risorse create con l'utilizzo predefinito dovrebbe essere eseguito con cautela. L'applicazione deve attendere il tempo sufficiente per il svuotamento del buffer dei comandi e quindi completare l'esecuzione di tutti i comandi prima di provare a eseguire il mapping della risorsa di gestione temporanea corrispondente. Per quanto tempo l'applicazione deve attendere? Almeno due frame, in quanto ciò consentirà di sfruttare al massimo il parallelismo tra CPU e GPU. Il funzionamento della GPU è che, mentre l'applicazione elabora il frame N inviando chiamate al buffer dei comandi, la GPU è occupata nell'esecuzione delle chiamate dal frame precedente, N-1.

Quindi, se un'applicazione vuole eseguire il mapping di una risorsa che ha origine nella memoria video e chiama [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) al frame n, questa chiamata inizierà a essere eseguita al frame n + 1, quando l'applicazione invia chiamate per il frame successivo. La copia deve essere completata quando l'applicazione sta elaborando il frame N + 2.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Frame</th>
<th>Stato GPU/CPU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>N</td>
<td><ul>
<li>I problemi di CPU eseguono il rendering delle chiamate per il frame corrente.</li>
</ul></td>
</tr>
<tr class="even">
<td>N + 1</td>
<td><ul>
<li>GPU che eseguono chiamate inviate dalla CPU durante il frame N.</li>
<li>I problemi di CPU eseguono il rendering delle chiamate per il frame corrente.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N + 2</td>
<td><ul>
<li>La GPU ha terminato l'esecuzione delle chiamate inviate dalla CPU durante il frame N. risultati pronti.</li>
<li>Esecuzione di chiamate GPU inviate dalla CPU durante il frame N + 1.</li>
<li>I problemi di CPU eseguono il rendering delle chiamate per il frame corrente.</li>
</ul></td>
</tr>
<tr class="even">
<td>N + 3</td>
<td><ul>
<li>La GPU ha terminato l'esecuzione delle chiamate inviate dalla CPU durante il frame N + 1. Risultati pronti.</li>
<li>GPU che eseguono chiamate inviate dalla CPU durante il frame N + 2.</li>
<li>I problemi di CPU eseguono il rendering delle chiamate per il frame corrente.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N + 4</td>
<td>...</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
