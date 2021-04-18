---
description: Uniscribe fornisce le API per il supporto della tipografia e per supportare la visualizzazione e la modifica del testo internazionale, incluse le complesse regole degli script Medio Oriente e asiatici.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Uso di Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319468"
---
# <a name="using-uniscribe"></a>Uso di Uniscribe

Uniscribe fornisce le API per il supporto della tipografia e per supportare la visualizzazione e la modifica del testo internazionale, incluse le complesse regole degli script Medio Oriente e asiatici. Uniscribe fornisce routine di basso livello per la gestione di testo completamente formattato e una semplice API ScriptString impostata per il testo non formattato.

Con Uniscribe, le applicazioni devono solo gestire un archivio di backup di codici carattere Unicode. Per tenere traccia dell'ordine dei caratteri, le applicazioni di layout del testo non devono gestire altri buffer o tabelle di mapping. Ogni applicazione deve solo archiviare e gestire l'ordine in cui i caratteri vengono immessi dall'utente, ovvero lo stesso ordine logico definito da Unicode. L'archivio di backup non viene mai modificato in seguito a operazioni di layout. Uniscribe mantiene un indice dai cluster riordinati ai limiti dei caratteri originali passati dall'applicazione.

In questa sezione vengono trattati gli argomenti seguenti.

**Shaping**

-   [Determinare se uno script richiede la definizione del glifo](determining-if-a-script-requires-glyph-shaping.md)
-   [Uso di shaping Engine](using-shaping-engines.md)

**Altre elaborazioni**

-   [Memorizzazione nella cache](caching.md)
-   [Visualizzazione di testo con Uniscribe](displaying-text-with-uniscribe.md)
-   [Elaborazione di script complessi](processing-complex-scripts.md)
-   [Uso del fallback dei tipi di carattere](using-font-fallback.md)
-   [Uso delle funzioni ScriptString](using-the-scriptstring-functions.md)

**Cursore**

-   [Visualizzazione del cursore nelle stringhe bidirezionali](displaying-the-caret-in-bidirectional-strings.md)
-   [Gestione della selezione host e hit testing del cursore](managing-caret-placement-and-hit-testing.md)
-   [Conversione dell'offset X del mouse nella posizione del punto di inserimento](translating-mouse-hit-x-offset-to-caret-position.md)

**Parole e cluster di caratteri**

-   [Uso di cluster di caratteri](using-character-clusters.md)
-   [Uso di punti di interruzioni di Word](using-word-break-points.md)
-   [Utilizzo delle relazioni tra le posizioni del punto di inserimento, i punti di giustificazione e i cluster](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



