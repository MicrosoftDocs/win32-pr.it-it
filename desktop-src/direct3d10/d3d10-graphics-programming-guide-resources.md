---
description: Una risorsa è un'area della memoria accessibile tramite la pipeline Direct3D.
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: Risorse (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93448fadd14d1a0849c9b730d34030b70d42a8cbc0926743e7059e222a6ea9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567051"
---
# <a name="resources-direct3d-10"></a>Risorse (Direct3D 10)

Una risorsa è un'area della memoria accessibile tramite la pipeline Direct3D. Per consentire alla pipeline di accedere in modo efficiente alla memoria, i dati forniti alla pipeline (ad esempio geometria di input, risorse shader, trame e così via) devono essere archiviati in una risorsa. Esistono due tipi di risorse da cui derivano tutte le risorse Direct3D: buffer e trama. Per ogni fase della pipeline possono essere attive fino a 128 risorse.

Ogni applicazione crea in genere molte risorse. Esempi di risorse includono: buffer dei vertici, index buffer, buffer costante, trame e risorse shader. Sono disponibili diverse opzioni che determinano come è possibile usare le risorse. È possibile creare risorse fortemente tip tip o meno di tipo. è possibile controllare se le risorse hanno accesso sia in lettura che in scrittura. È possibile rendere le risorse accessibili solo alla CPU, alla GPU o a entrambi. Naturalmente, ci sarà un compromesso tra velocità e funzionalità: maggiore sarà la funzionalità che si consente a una risorsa, minore sarà il livello di prestazioni previsto.

Poiché un'applicazione usa spesso molte trame, Direct3D introduce anche il concetto di matrice di trame per semplificare la gestione delle trame. Una matrice di trame contiene una o più trame (tutte dello stesso tipo e dimensioni) che possono essere indicizzate dall'interno di un'applicazione o dagli shader. Le matrici di trame consentono di usare una singola interfaccia con più indici per accedere a più trame. È possibile creare tutte le matrici di trame per gestire i diversi tipi di trama necessari.

Dopo aver creato le risorse che verranno usate dall'applicazione, connettere o associare ogni risorsa alle fasi della pipeline che le useranno. Questa operazione viene eseguita chiamando un'API di associazione, che accetta un puntatore alla risorsa. Poiché più fasi della pipeline possono richiedere l'accesso alla stessa risorsa, Direct3D 10 introduce il concetto di visualizzazione delle risorse. Una vista identifica la parte di una risorsa a cui è possibile accedere. È possibile creare visualizzazioni m o una risorsa e associarle a n fasi della pipeline, presupponendo di seguire le regole di associazione per la risorsa condivisa (il runtime genererà errori in fase di compilazione se non lo si fa).

Una visualizzazione risorse fornisce un modello generale per l'accesso a una risorsa (trame, buffer e così via). Poiché è possibile usare una visualizzazione per indicare al runtime i dati a cui accedere e come accedervi, le visualizzazioni delle risorse consentono di creare meno risorse di tipo. Ciò significa che è possibile creare risorse per una determinata dimensione in fase di compilazione e quindi dichiarare il tipo di dati all'interno della risorsa quando la risorsa viene associata alla pipeline. Le visualizzazioni espongono molte nuove funzionalità per l'uso delle risorse, ad esempio la possibilità di leggere le superfici di profondità/stencil nello shader, la generazione di mappe cubi dinamiche in un unico passaggio e il rendering simultaneo in più sezioni di un volume.

Per altre informazioni sui tipi di risorse di base, sulle matrici di trame e su come creare e usare le risorse, vedere gli altri argomenti seguenti:

-   [Tipi di risorse](d3d10-graphics-programming-guide-resources-types.md)
-   [Scelta di una risorsa](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [Creazione di risorse buffer](d3d10-graphics-programming-guide-resources-creating.md)
-   [Creazione di risorse di trama](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [Copia e accesso ai dati delle risorse](d3d10-graphics-programming-guide-resources-mapping.md)
-   [Struttura della memoria e visualizzazioni](d3d10-graphics-programming-guide-resources-access-views.md)
-   [Compressione a blocchi](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [Tabella dei limiti delle risorse](d3d10-graphics-programming-guide-resources-limits.md)
-   [Sistemi di coordinate](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [Regole a virgola mobile](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [Regole di conversione dei tipi di dati](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [Mapping di formati legacy](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



