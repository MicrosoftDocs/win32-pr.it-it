---
description: Una risorsa è un'area della memoria accessibile tramite la pipeline Direct3D.
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: Risorse (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bb064bc771e36335527d68891bc76a1ce4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483589"
---
# <a name="resources-direct3d-10"></a>Risorse (Direct3D 10)

Una risorsa è un'area della memoria accessibile tramite la pipeline Direct3D. Per consentire alla pipeline di accedere in modo efficiente alla memoria, i dati forniti alla pipeline, ad esempio la geometria di input, le risorse dello shader, le trame e così via, devono essere archiviati in una risorsa. Esistono due tipi di risorse da cui derivano tutte le risorse Direct3D: buffer e trama. Per ogni fase della pipeline possono essere attive fino a 128 risorse.

In ogni applicazione vengono in genere create molte risorse. Esempi di risorse includono: buffer di vertici, buffer di indice, buffer costante, trame e risorse dello shader. Sono disponibili diverse opzioni che determinano il modo in cui è possibile usare le risorse. È possibile creare risorse fortemente tipizzate o di tipo less; è possibile controllare se le risorse hanno accesso sia in lettura che in scrittura; è possibile rendere le risorse accessibili solo alla CPU, alla GPU o a entrambe. Naturalmente, ci sarà un compromesso tra velocità e funzionalità. maggiore è il numero di funzionalità consentite per una risorsa, minore sarà la prestazione prevista.

Poiché un'applicazione spesso usa molte trame, Direct3D introduce anche il concetto di una matrice di trame per semplificare la gestione delle trame. Una matrice di trame contiene una o più trame (tutte dello stesso tipo e dimensioni) che possono essere indicizzate dall'interno di un'applicazione o da shader. Le matrici di trame consentono di usare una singola interfaccia con più indici per accedere a molte trame. È possibile creare un numero così elevato di matrici di trame per gestire i diversi tipi di trama necessari.

Dopo aver creato le risorse che l'applicazione userà, è possibile connettere o associare ogni risorsa alle fasi della pipeline che li useranno. Questa operazione viene eseguita chiamando un'API bind, che accetta un puntatore alla risorsa. Poiché è possibile che più fasi della pipeline debbano accedere alla stessa risorsa, Direct3D 10 introduce il concetto di visualizzazione delle risorse. Una visualizzazione identifica la parte di una risorsa a cui è possibile accedere. È possibile creare visualizzazioni m o una risorsa e associarle a n fasi della pipeline, presupponendo che si seguano le regole di binding per la risorsa condivisa (il runtime genererà errori in fase di compilazione se non lo è).

Una visualizzazione risorse fornisce un modello generale per l'accesso a una risorsa (trame, buffer e così via). Poiché è possibile usare una visualizzazione per indicare al runtime i dati a cui accedere e come accedervi, le visualizzazioni delle risorse consentono di creare meno risorse del tipo. Ovvero, è possibile creare risorse per una determinata dimensione in fase di compilazione e quindi dichiarare il tipo di dati all'interno della risorsa quando la risorsa viene associata alla pipeline. Le visualizzazioni espongono numerose nuove funzionalità per l'utilizzo delle risorse, ad esempio la possibilità di leggere le superfici dello shader nello shader, di generare CubeMaps dinamici in un singolo passaggio e di eseguire il rendering simultaneo in più sezioni di un volume.

Per altre informazioni sui tipi di risorse di base, sulle matrici di trama e su come creare e usare le risorse, vedere gli argomenti seguenti:

-   [Tipi di risorse](d3d10-graphics-programming-guide-resources-types.md)
-   [Scelta di una risorsa](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [Creazione di risorse buffer](d3d10-graphics-programming-guide-resources-creating.md)
-   [Creazione di risorse di trama](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [Copia e accesso ai dati delle risorse](d3d10-graphics-programming-guide-resources-mapping.md)
-   [Struttura e visualizzazioni della memoria](d3d10-graphics-programming-guide-resources-access-views.md)
-   [Compressione dei blocchi](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [Tabella dei limiti delle risorse](d3d10-graphics-programming-guide-resources-limits.md)
-   [Sistemi di coordinate](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [Regole a virgola mobile](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [Regole di conversione del tipo di dati](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [Mapping di formati legacy](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



