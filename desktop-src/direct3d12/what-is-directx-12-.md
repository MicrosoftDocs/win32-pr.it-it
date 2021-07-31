---
title: Che cos'è Direct3D 12
description: DirectX 12 introduce la versione successiva di Direct3D; l'API grafica 3D alla base di DirectX.
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: f82b01ba33cfa6660f266a481b2eaaab20ade236
ms.sourcegitcommit: 60ff57d8cf94ae7a47c6046ad49f7c7256a7edb6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/31/2021
ms.locfileid: "115006796"
---
# <a name="what-is-direct3d-12"></a>Cos'è Direct3D 12?

DirectX 12 introduce la versione successiva di Direct3D &mdash; dell'API grafica 3D alla base di DirectX. Direct3D 12 è più veloce ed efficiente di qualsiasi versione precedente. Direct3D 12 consente scene più complete, più oggetti, effetti più complessi e utilizzo completo dell'hardware GPU moderno.

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>In che modo Direct3D 12 può essere molto più veloce ed efficiente?

Direct3D 12 è univoco in quanto fornisce un livello inferiore di astrazione hardware rispetto alle versioni precedenti, che consente di migliorare in modo significativo il ridimensionamento della CPU multi-core del titolo (o di un'altra applicazione). Per prima cosa, con Direct3D 12, il titolo è responsabile della gestione [della memoria.](memory-management.md) Inoltre, usando Direct3D 12, i titoli e le applicazioni traggono vantaggio dal sovraccarico ridotto della GPU tramite funzionalità quali code di comandi ed [elenchi,](command-queues-and-command-lists.md)tabelle descrittori e oggetti di stato della [](descriptor-tables.md) [pipeline](managing-graphics-pipeline-state-in-direct3d-12.md)concisi.

Direct3D 12 e Direct3D 11.3 introducono un set di nuove funzionalità per la pipeline di rendering.

- [Rasterizzazione conservativa per](../direct3d11/conservative-rasterization.md) abilitare il rilevamento affidabile degli hit.
- [Volume delle risorse affiancate](../direct3d11/volume-tiled-resources.md) per consentire alle risorse tridimensionali trasmesse in streaming di essere considerate come se fossero tutte nella memoria video.
- [Visualizzazioni ordinate dal rasterizzatore](../direct3d11/rasterizer-order-views.md) per abilitare il rendering affidabile della trasparenza.
- Impostazione del riferimento dello stencil all'interno di uno shader per abilitare lo shadowing speciale e altri effetti.
- Mapping delle trame migliorato e caricamento della visualizzazione di accesso non ordinato (UAV, Unordered Access View) tipied.

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>Quanto è necessario investire in Direct3D 12?

Direct3D 12 offre quattro vantaggi principali agli sviluppatori di grafica (rispetto a Direct3D 11).

- Sovraccarico della CPU notevolmente ridotto.
- Consumo di energia significativamente ridotto.
- Fino al (circa) 20% di miglioramento dell'efficienza della GPU.
- Sviluppo multipiattaforma per un Windows 10 (PC, tablet, console, dispositivi mobili).

Direct3D 12 è progettato per i programmatori di grafica avanzati da usare. Richiede un'esperienza grafica significativa e un alto livello di ottimizzazione. Direct3D 12 è progettato per usare completamente multithreading, un'attenta sincronizzazione CPU/GPU e la transizione e il nuovo uso delle risorse da uno scopo a un altro. Si tratta di tecniche che richiedono una notevole quantità di competenze di programmazione a livello di memoria.

Un altro vantaggio di Direct3D 12 è il footprint di API ridotto. Sono disponibili circa 200 funzioni. e circa un terzo di questi fa tutto il lavoro pesante. Ciò significa che gli sviluppatori di grafica dovrebbero essere in grado di istruire e usare il set completo di API senza dover memorizzare troppi nomi &mdash; &mdash; di API.

Direct3D 11 continua a essere un'opzione praticabile insieme a Direct3D 12. Molte delle nuove funzionalità di rendering di Direct3D 12 sono disponibili in [Direct3D 11.3.](../direct3d11/direct3d-11-3-features.md) Direct3D 11.3 è un'API del motore di grafica di basso livello. e Direct3D 12 è ancora più profondo.

Esistono almeno due modi in cui il team di sviluppo può approcciarsi a un titolo Direct3D 12.

### <a name="use-direct3d-12-exclusively"></a>Usare Direct3D 12 in modo esclusivo

Per un progetto che sfrutta tutti i vantaggi di Direct3D 12, è consigliabile sviluppare un motore Direct3D 12 altamente personalizzato da zero.

Se uno sviluppatore di grafica comprende l'uso e il nuovo uso delle risorse all'interno dei titoli e può sfruttare questo vantaggio riducendo al minimo il caricamento e la copia, è possibile sviluppare e personalizzare un motore altamente efficiente per tali titoli. I miglioramenti delle prestazioni potrebbero essere considerevoli, liberando tempo di CPU per aumentare il numero di chiamate di disegno e quindi aggiungendo maggiore lucenteria alla grafica.

L'investimento di programmazione è significativo ed è consigliabile prendere in considerazione il debug e la strumentazione del progetto fin dall'inizio. Threading, sincronizzazione e altri bug di temporizzazione possono essere complessi.

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>Usare Direct3D 12 insieme a Direct3D 11

Un approccio a breve termine consiste nell'affrontare i colli di bottiglia noti nel titolo Direct3D 11. È possibile risolvere questi casi usando le tecniche di interoperabilità [Direct3D 12 e/o D3D11On12,](direct3d-12-interop.md) che consentono di usare insieme le due versioni dell'API. Questo approccio riduce al minimo le modifiche necessarie a un motore di grafica Direct3D 11 esistente. Tuttavia, i miglioramenti delle prestazioni saranno limitati alla riduzione del collo di bottiglia che il codice Direct3D 12 risolve.

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Video di Microsoft DirectX 12 (e formazione grafica)

[Formazione migliorata per gli sviluppatori di grafica.](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA) Questi video trattano argomenti come le modalità di presentazione, il porting a DirectX 12, la rasterizzazione conservativa, gli strumenti di grafica, Angle, Win2D ed eventi come GDC, Build e altro ancora. Il contenuto tecnico di DirectX 12 è preceduto *da DirectX 12.* È possibile ottenere suggerimenti e consigli direttamente dal team delle funzionalità di Direct3D 12. Microsoft vuole aiutare l'utente a usare le versioni e gli strumenti più recenti per rendere il gioco il migliore possibile.

## <a name="conclusion"></a>Conclusione

Direct3D 12 è tutto sulle prestazioni del motore di grafica. La facilità di sviluppo, i costrutti di alto livello e il supporto del compilatore sono stati ridimensionati per consentire questa operazione. Il supporto dei driver e la facilità di debug rimangono alla pari con Direct3D 11.

Direct3D 12 è un nuovo territorio. Territorio in attesa che l'esperto esperto venga a esplorare.
