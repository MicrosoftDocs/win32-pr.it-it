---
title: Che cos'è Direct3D 12
description: In DirectX 12 è stata introdotta la versione successiva di Direct3D; API grafica 3D al centro di DirectX.
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: b3ff1896372719b011b283e3ff1f5426db9e13d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103819"
---
# <a name="what-is-direct3d-12"></a>Cos'è Direct3D 12?

In DirectX 12 è stata introdotta la prossima versione di Direct3D &mdash; , l'API grafica 3D, alla base di DirectX. Direct3D 12 è più veloce ed efficiente rispetto a qualsiasi versione precedente. Direct3D 12 offre scenari più completi, più oggetti, effetti più complessi e un utilizzo completo di hardware GPU moderno.

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>In che modo Direct3D 12 può essere molto più veloce ed efficiente?

Direct3D 12 è univoco in quanto fornisce un livello di astrazione hardware inferiore rispetto alle versioni precedenti, che consente di migliorare significativamente il ridimensionamento della CPU multicore del titolo o di un'altra applicazione. Per una cosa, con Direct3D 12, il titolo è responsabile della gestione della [memoria](memory-management.md). Inoltre, utilizzando Direct3D 12, i titoli e le applicazioni traggono vantaggio dalla riduzione del sovraccarico della GPU tramite funzionalità come le [code di comando e gli elenchi](command-queues-and-command-lists.md), le [tabelle di descrittori](descriptor-tables.md)e [gli oggetti di stato della pipeline](managing-graphics-pipeline-state-in-direct3d-12.md)concisi.

Direct3D 12 e Direct3D 11,3 introducono un set di nuove funzionalità per la pipeline di rendering.

- [Rasterizzazione conservativa](../direct3d11/conservative-rasterization.md) per abilitare il rilevamento di hit affidabili.
- [Risorse affiancate al volume](../direct3d11/volume-tiled-resources.md) per consentire l'invio di risorse tridimensionali con flusso come se fossero tutte nella memoria video.
- [Rasterizzazione: visualizzazioni ordinate](../direct3d11/volume-tiled-resources.md) per abilitare il rendering affidabile della trasparenza.
- Impostazione del riferimento stencil all'interno di uno shader per consentire lo shadowing speciale e altri effetti.
- È stato migliorato il mapping di trama e i carichi UAV (unordered Access View) tipizzati.

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>Con quale profondità devo investire in Direct3D 12?

Direct3D 12 offre quattro vantaggi principali agli sviluppatori grafici (rispetto a Direct3D 11).

- Notevole riduzione del sovraccarico della CPU.
- Il consumo di energia è notevolmente ridotto.
- Fino a (approssimativamente) miglioramento del 20% nell'efficienza della GPU.
- Sviluppo multipiattaforma per un dispositivo Windows 10 (PC, tablet, console, dispositivi mobili).

Direct3D 12 è progettato per i programmatori grafici avanzati da usare. Richiede una notevole esperienza grafica e un elevato livello di ottimizzazione. Direct3D 12 è progettato per sfruttare al meglio il multithreading, una sincronizzazione attenta della CPU/GPU e la transizione e il riutilizzo delle risorse da uno scopo a un altro. Si tratta di tecniche che richiedono una notevole quantità di competenze di programmazione a livello di memoria.

Un altro vantaggio offerto da Direct3D 12 è la piccola impronta API. Sono disponibili circa 200 funzioni; e circa un terzo di questi sono tutti i pesanti. Questo significa che, in qualità di sviluppatore di grafica, dovrebbe essere in grado di istruirsi &mdash; e padroneggiare &mdash; il set completo di API senza dover memorizzare troppi nomi di API.

Direct3D 11 continua a essere un'opzione valida insieme a Direct3D 12. Molte delle nuove funzionalità di rendering di Direct3D 12 sono disponibili in [direct3d 11,3](../direct3d11/direct3d-11-3-features.md). Direct3D 11,3 è un'API del motore di grafica di basso livello. e Direct3D 12 risulta ancora più approfondito.

Il team di sviluppo può accedere a un titolo Direct3D 12 in almeno due modi.

### <a name="use-direct3d-12-exclusively"></a>Usare esclusivamente Direct3D 12

Per un progetto che si avvale di tutti i vantaggi di Direct3D 12, è consigliabile sviluppare un motore Direct3D 12 altamente personalizzato da zero.

Gli sviluppatori grafici possono comprendere l'uso e il riutilizzo delle risorse all'interno dei propri titoli, sfruttando al minimo il caricamento e la copia, quindi è possibile sviluppare e personalizzare un motore altamente efficiente per questi titoli. I miglioramenti apportati alle prestazioni potrebbero essere molto significativi, liberando il tempo della CPU per aumentare il numero di chiamate di progetto e quindi aggiungendo più Luster alla grafica.

L'investimento di programmazione è significativo ed è opportuno prendere in considerazione il debug e la strumentazione del progetto fin dall'inizio. Il threading, la sincronizzazione e altri bug temporali possono essere complessi.

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>Usare Direct3D 12 in concerto con Direct3D 11

Un approccio a breve termine è quello di risolvere i colli di bottiglia noti nel titolo di Direct3D 11. È possibile risolverli usando le tecniche di [interoperabilità di Direct3D 12 e/o D3D11On12](direct3d-12-interop.md) , che consentono di interagire con le due versioni dell'API. Questo approccio riduce al minimo le modifiche necessarie a un motore di grafica Direct3D 11 esistente. Tuttavia, il miglioramento delle prestazioni sarà limitato al sollievo del collo di bottiglia che il codice Direct3D 12 indirizza.

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Video su Microsoft DirectX 12 (e formazione grafica)

[Formazione migliorata per gli sviluppatori di grafica](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA). Questi video illustrano argomenti come le modalità di presentazione, il porting a DirectX 12, la rasterizzazione conservativa, strumenti di grafica, angolo, Win2D ed eventi come GDC, Build e altro ancora. Il contenuto tecnico di DirectX 12 è preceduto da *DirectX 12*. Per apprendere suggerimenti e consigli direttamente dal team di funzionalità di Direct3D 12, Microsoft vuole aiutarti a usare le versioni e gli strumenti più recenti per sfruttare al meglio il tuo gioco.

## <a name="conclusion"></a>Conclusione

Direct3D 12 riguarda le prestazioni del motore grafico più drammatiche. La facilità di sviluppo, i costrutti di alto livello e il supporto del compilatore sono stati ridimensionati per abilitare questa operazione. Il supporto dei driver e la facilità di debug rimangono in una coppia con Direct3D 11.

Direct3D 12 è un nuovo territorio. Territorio che è in attesa di essere esplorato dall'esperto curioso.
