---
title: Guida alla programmazione per Direct3D 12
description: Direct3D 12 fornisce un'API e una piattaforma che consente alle app di sfruttare le funzionalità di grafica e calcolo dei PC dotati di una o più GPU compatibili con Direct3D 12.
ms.assetid: 16F78A6B-74C4-4ED1-809F-FE6DE157F368
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 94afd9125a2e73665e3783419651f34fd72285ca
ms.sourcegitcommit: bf6a52b91604d8a9432bf646097e3f31e44967d7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/06/2019
ms.locfileid: "104548876"
---
# <a name="direct3d-12-programming-guide"></a>Guida alla programmazione per Direct3D 12

Direct3D 12 fornisce un'API e una piattaforma che consente alle app di sfruttare le funzionalità di grafica e calcolo dei PC dotati di una o più GPU compatibili con Direct3D 12.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Cos'è Direct3D 12?](what-is-directx-12-.md) | In DirectX 12 è stata introdotta la versione successiva di Direct3D, l'API grafica 3D alla base di DirectX. Questa versione di Direct3D è più veloce e più efficiente rispetto a qualsiasi versione precedente. Direct3D 12 offre scenari più completi, più oggetti, effetti più complessi e un utilizzo completo di hardware GPU moderno.  |
| [Novità di Direct3D 12](new-releases.md) | Viene descritta la nuova documentazione più significativa disponibile con la versione più recente dell'SDK. |
| [Informazioni su Direct3D 12](directx-12-getting-started.md) | Per scrivere giochi 3D e app per Windows 10 e Windows 10 Mobile, è necessario comprendere le nozioni di base della tecnologia Direct3D 12 e come prepararsi a usarla nei giochi e nelle app. |
| [Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md) | Per migliorare l'efficienza della CPU delle app Direct3D, Direct3D 12 non supporta più un contesto immediato associato a un dispositivo. Al contrario, le app registrano e quindi inviano *elenchi di comandi*, che contengono chiamate di gestione delle risorse e di disegno. Questi elenchi di comandi possono essere inviati da più thread a una o più code di comandi, che gestiscono l'esecuzione dei comandi. Questa modifica fondamentale aumenta l'efficienza a thread singolo consentendo alle app di pre-calcolare il lavoro di rendering per riutilizzarlo in un secondo momento, sfruttando i sistemi multicore distribuendo il lavoro di rendering tra più thread.  |
| [Binding delle risorse in Direct3D 12](resource-binding.md) | Binding è il processo di collegamento di oggetti risorsa agli shader della pipeline grafica.  |
| [Gestione della memoria in Direct3D 12](memory-management.md) | Il passaggio a D3D12 comporta una corretta sincronizzazione e gestione della residenza di memoria. La gestione della residenza della memoria significa che è necessario eseguire ancora più sincronizzazioni. In questa sezione vengono illustrate le strategie di gestione della memoria e le sottoallocazioni all'interno di heap e buffer.  |
| [Sistemi con più adapter](multi-engine.md) | Viene descritto il supporto in Direct3D 12 per i sistemi in cui sono installati più adapter, coprendo scenari in cui l'applicazione è destinata in modo esplicito a più adapter GPU e scenari in cui i driver utilizzano in modo implicito più schede GPU per conto dell'applicazione. |
| [Sincronizzazione multimotore](user-mode-heap-synchronization.md) | Questo argomento illustra la sincronizzazione dell'accesso a più motori indipendenti disponibili nella maggior parte delle GPU moderne. |
| [Rendering](rendering.md) | Questa sezione contiene informazioni sulle funzionalità di rendering nuove di Direct3D 12 (e Direct3D 11,3). |
| [Contatori, query e misurazione delle prestazioni](performance-measurement.md) | Le sezioni seguenti descrivono le funzionalità da usare per il test delle prestazioni e il miglioramento, ad esempio query, contatori, temporizzazione e predicazione. |
| [Uso di Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md) | Questa sezione illustra le tecniche di interoperabilità con le versioni precedenti di Direct3D e Direct2D, l'API Direct3D 11on12 e le linee guida per il porting da Direct3D 11 a Direct3D 12. |
| [Esempi di lavoro](working-samples.md) | Gli esempi operativi sono disponibili per il download, mostrando l'utilizzo di una serie di funzionalità di Direct3D 12. |
| [Procedure dettagliate per il codice D3D12](d3d12-code-walk-throughs.md) | In questa sezione viene fornito il codice per gli scenari di esempio. Molti dei passaggi forniscono informazioni dettagliate su quale codifica è necessario aggiungere a un esempio di base, per evitare di ripetere il codice componente di base per ogni scenario. |
| [Debug e diagnostica con Direct3D 12](understanding-the-d3d12-debug-layer.md) | Include argomenti che descrivono come usare al meglio il livello di debug Direct3D 12 con la convalida basata su GPU (GBV) e come usare i dati estesi rimossi del dispositivo (eseguire). |

## <a name="related-topics"></a>Argomenti correlati

* [Grafica Direct3D 12](direct3d-12-graphics.md)
* [Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
* [Esercitazioni video su DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
