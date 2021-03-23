---
title: Cenni preliminari sulle firme radice
description: Una firma radice viene configurata tramite l'app e collega gli elenchi di comandi alle risorse necessarie per gli shader.
ms.assetid: 2E649DA2-6CAC-4C2A-A420-D4EC0DD6EA73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85eb5882e4a893c2933c55281f21c49f2d7d50d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548851"
---
# <a name="root-signatures-overview"></a>Cenni preliminari sulle firme radice

Una firma radice viene configurata tramite l'app e collega gli elenchi di comandi alle risorse necessarie per gli shader. L'elenco dei comandi di grafica include una firma della radice di calcolo e grafica. Un elenco di comandi di calcolo avrà semplicemente una firma radice di calcolo. Queste firme radice sono indipendenti l'una dall'altra.

-   [Parametri e argomenti radice](#root-parameters-and-arguments)
-   [Costanti radice, descrittori e tabelle](#root-constants-descriptors-and-tables)
-   [Argomenti correlati](#related-topics)

## <a name="root-parameters-and-arguments"></a>Parametri e argomenti radice

Una **firma radice** è simile a una firma della funzione API, che determina i tipi di dati che gli shader dovrebbero aspettarsi, ma non definisce la memoria o i dati effettivi. Un **parametro radice** è una voce nella firma radice. I valori effettivi dei parametri radice impostati e modificati in fase di esecuzione sono detti **argomenti radice**. La modifica degli argomenti radice modifica i dati letti dagli shader.

## <a name="root-constants-descriptors-and-tables"></a>Costanti radice, descrittori e tabelle

La firma radice può contenere tre tipi di parametri. costanti radice (costanti inline negli argomenti radice), descrittori radice (descrittori inline negli argomenti radice) e tabelle dei descrittori (puntatori a un intervallo di descrittori nell'heap del descrittore).

Le costanti radice sono valori inline a 32 bit che vengono visualizzati nello shader come buffer costante.

I descrittori radice resi inline devono contenere descrittori a cui si accede più spesso, sebbene sia limitato a CBVs e a buffer UAV o SRV non elaborati o strutturati. Un tipo più complesso, ad esempio una trama 2D SRV, non può essere utilizzato come descrittore radice. I descrittori radice non includono un limite di dimensioni, pertanto non è possibile eseguire il controllo out-of-Bounds, a differenza dei descrittori negli heap dei descrittori, che includono una dimensione.

Le voci della tabella descrittore nelle firme radice contengono il descrittore, il nome di associazione dello shader HLSL e il flag di visibilità. Per informazioni dettagliate sui nomi degli shader, vedere il [modello di shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1) . In alcuni componenti hardware è possibile che si verifichi un miglioramento delle prestazioni limitando la visibilità dei descrittori alle fasi dello shader che le richiedono (vedere la [**\_ \_ visibilità dello shader D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)).

![voce della tabella descrittore radice](images/root-descriptor-table.png)

Il layout della firma radice è piuttosto flessibile, con alcuni vincoli imposti su hardware meno idoneo. Indipendentemente dal livello di hardware, le applicazioni devono sempre provare a rendere la firma radice di dimensioni ridotte, in base alle esigenze, per la massima efficienza. Le applicazioni possono comportare la disattivazione della presenza di più tabelle dei descrittori nella firma radice, ma meno spazio per le costanti radice o viceversa.

Il contenuto della firma radice (le tabelle dei descrittori, le costanti radice e i descrittori radice) a cui l'applicazione è associata automaticamente viene sottoposta a controllo delle versioni dal driver D3D12 ogni volta che una parte del contenuto cambia tra le chiamate di/dispatch (Compute). Ogni operazione di estrazione/invio ottiene quindi un set univoco completo dello stato della firma radice.

Idealmente, esistono gruppi di oggetti di stato della pipeline (PSO) che condividono la stessa firma radice. Dopo aver impostato una firma radice sulla pipeline, tutte le associazioni che definisce (tabelle descrittori, descrittori, costanti) possono essere impostate o modificate singolarmente, inclusa l'ereditarietà in bundle.

Un'app può comportare un proprio compromesso tra il numero di tabelle di descrittori che desiderano i descrittori inline (che prevedono una maggiore quantità di spazio, ma la rimozione di un riferimento indiretto), che desiderano nella firma radice. Le applicazioni devono utilizzare la firma radice nel modo più sporadico possibile, basandosi sulla memoria controllata dall'applicazione, ad esempio heap e heap di descrittori che puntano a tali elementi per rappresentare i dati in blocco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Firme radice](root-signatures.md)
</dt> </dl>

 

 