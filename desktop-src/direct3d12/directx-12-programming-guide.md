---
title: Guida alla programmazione per Direct3D 12
description: Direct3D 12 offre un'API e una piattaforma che consentono alle app di sfruttare le funzionalità grafiche e di calcolo dei PC dotati di una o più GPU compatibili con Direct3D 12.
ms.assetid: 16F78A6B-74C4-4ED1-809F-FE6DE157F368
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: c7dfaf55b44da4a05616db7b7f64c262a3c5b6920ab2c0665e1196d70b539215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045489"
---
# <a name="direct3d-12-programming-guide"></a>Guida alla programmazione per Direct3D 12

Direct3D 12 offre un'API e una piattaforma che consentono alle app di sfruttare le funzionalità grafiche e di calcolo dei PC dotati di una o più GPU compatibili con Direct3D 12.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Cos'è Direct3D 12?](what-is-directx-12-.md) | DirectX 12 introduce la prossima versione di Direct3D, l'API grafica 3D alla base di DirectX. Questa versione di Direct3D è più veloce ed efficiente rispetto a qualsiasi versione precedente. Direct3D 12 consente scene più complete, più oggetti, effetti più complessi e utilizzo completo dell'hardware GPU moderno.  |
| [Novità di Direct3D 12](new-releases.md) | Descrive la nuova documentazione più significativa disponibile con la versione più recente dell'SDK. |
| [Informazioni su Direct3D 12](directx-12-getting-started.md) | Per scrivere giochi e app 3D per Windows 10 e Windows 10 Mobile, è necessario comprendere le nozioni di base della tecnologia Direct3D 12 e come prepararsi per l'uso nei giochi e nelle app. |
| [Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md) | Per migliorare l'efficienza della CPU delle app Direct3D, Direct3D 12 non supporta più un contesto immediato associato a un dispositivo. Al contrario, le app registrano e inviano *elenchi di comandi* che contengono chiamate di disegno e gestione delle risorse. Questi elenchi di comandi possono essere inviati da più thread a una o più code di comandi, che gestiscono l'esecuzione dei comandi. Questa modifica fondamentale aumenta l'efficienza a thread singolo consentendo alle app di pre-calcolare il lavoro di rendering per un uso successivo e sfrutta i vantaggi dei sistemi multi-core spreading del lavoro di rendering tra più thread.  |
| [Binding delle risorse in Direct3D 12](resource-binding.md) | Il binding è il processo di collegamento di oggetti risorsa agli shader della pipeline grafica.  |
| [Gestione della memoria in Direct3D 12](memory-management.md) | Il passaggio a D3D12 comporta la sincronizzazione e la gestione corrette della residenza della memoria. La gestione della residenza della memoria significa che è necessario eseguire una sincronizzazione ancora maggiore. Questa sezione illustra le strategie di gestione della memoria e la sottoallocazione all'interno di heap e buffer.  |
| [Sistemi con più schede](multi-engine.md) | Descrive il supporto in Direct3D 12 per i sistemi in cui sono installate più schede, descrive gli scenari in cui l'applicazione è destinata in modo esplicito a più schede GPU e gli scenari in cui i driver usano implicitamente più schede GPU per conto dell'applicazione. |
| [Sincronizzazione di più motori](user-mode-heap-synchronization.md) | In questo argomento viene illustrata la sincronizzazione dell'accesso ai più motori indipendenti disponibili nelle GPU più moderne. |
| [Rendering](rendering.md) | Questa sezione contiene informazioni sulle funzionalità di rendering nuove di Direct3D 12 (e Direct3D 11.3). |
| [Contatori, query e misurazione delle prestazioni](performance-measurement.md) | Nelle sezioni seguenti vengono descritte le funzionalità da utilizzare per il test delle prestazioni e il miglioramento, ad esempio query, contatori, tempistica e predicazione. |
| [Uso di Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md) | Questa sezione illustra le tecniche di interoperabilità con le versioni precedenti di Direct3D e Direct2D, l'API Direct3D 11on12 e le linee guida per la portabilità da Direct3D 11 a Direct3D 12. |
| [Esempi funzionanti](working-samples.md) | Sono disponibili esempi funzionanti per il download, che mostrano l'utilizzo di alcune funzionalità di Direct3D 12. |
| [Procedura per il codice D3D12](d3d12-code-walk-throughs.md) | In questa sezione viene fornito il codice per gli scenari di esempio. Molte delle operazioni dettagliate forniscono informazioni dettagliate sul codice da aggiungere a un esempio di base, per evitare di ripetere il codice del componente di base per ogni scenario. |
| [Debug e diagnostica con Direct3D 12](understanding-the-d3d12-debug-layer.md) | Include argomenti che descrivono come usare al meglio il livello di debug Direct3D 12 con la convalida basata su GPU e come usare drED (Device Removed Extended Data). |

## <a name="related-topics"></a>Argomenti correlati

* [Grafica Direct3D 12](direct3d-12-graphics.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
* [Esercitazioni video di apprendimento avanzato DirectX](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
