---
title: Utilizzo di tabelle descrittore
description: Le tabelle dei descrittori, ciascuna delle quali identifica un intervallo in un heap descrittore, vengono associate agli slot definiti dalla firma radice corrente in un elenco di comandi.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104062"
---
# <a name="using-descriptor-tables"></a>Utilizzo di tabelle descrittore

Le tabelle dei descrittori, ciascuna delle quali identifica un intervallo in un heap descrittore, vengono associate agli slot definiti dalla firma radice corrente in un elenco di comandi.

-   [Indicizzazione di tabelle descrittore](#indexing-descriptor-tables)
-   [Argomenti correlati](#related-topics)

Gli shader possono individuare le risorse a cui fanno riferimento i descrittori che compongono la tabella del descrittore. Altre associazioni di risorse: i buffer di indice, il buffer di vertex, i buffer di output del flusso, le destinazioni di rendering e lo stencil di profondità vengono eseguiti direttamente in un elenco di comandi anziché tramite descrittori. Per concludere:

I riferimenti alle risorse seguenti possono condividere la stessa tabella e l'heap del descrittore:

-   Viste delle risorse shader
-   Viste di accesso non ordinate
-   Viste del buffer costante

I riferimenti alle risorse seguenti devono trovarsi nel proprio heap dei descrittori:

-   Campionatori

Le risorse seguenti non vengono inserite nelle tabelle o negli heap del descrittore, ma vengono associate direttamente tramite gli elenchi di comandi:

-   Index buffer
-   Buffer vertici
-   Buffer di output di flusso
-   Destinazioni di rendering
-   Visualizzazioni stencil profondità

## <a name="indexing-descriptor-tables"></a>Indicizzazione di tabelle descrittore

Gli shader non possono eseguire l'indicizzazione dinamica tra i limiti della tabella descrittore da un determinato sito di chiamata nello shader. Tuttavia, la selezione di un descrittore all'interno di una tabella descrittore può essere indicizzata dinamicamente nel codice dello shader all'interno di intervalli dello stesso tipo di descrittore, ad esempio l'indicizzazione in un'area contigua di SRVs.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabelle descrittore](descriptor-tables.md)
</dt> </dl>

 

 




