---
title: Perché le risorse affiancate sono necessarie
description: Le risorse affiancate sono necessarie, in modo che la memoria dell'unità di elaborazione grafica (GPU) venga sprecata per l'archiviazione di aree di superfici che l'applicazione sa non sarà accessibile e l'hardware possa comprendere come filtrare tra i riquadri adiacenti.
ms.assetid: E2179D65-56D3-481F-A5F3-B9C45A11A179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42ccccf66a73d224d8bab9a9d10c87cc330be43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976655"
---
# <a name="why-are-tiled-resources-needed"></a>Perché sono necessarie risorse affiancate?

Le risorse affiancate sono necessarie, in modo che la memoria dell'unità di elaborazione grafica (GPU) venga sprecata per l'archiviazione di aree di superfici che l'applicazione sa non sarà accessibile e l'hardware possa comprendere come filtrare tra i riquadri adiacenti.

In un sistema grafico (ovvero il sistema operativo, il driver di visualizzazione e l'hardware grafico) senza supporto delle risorse affiancate, il sistema grafico gestisce tutte le allocazioni di memoria Direct3D a livello di granularità delle risorse. Per un [buffer](overviews-direct3d-11-resources-buffers.md), l'intero buffer è la sottorisorsa. Per una [trama](overviews-direct3d-11-resources-textures.md) , ad esempio [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d), ogni livello MIP è una sottorisorsa; per una matrice di trame (ad esempio, [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray)), ogni livello MIP in una determinata sezione della matrice è una sottorisorsa. Il sistema grafico espone solo la possibilità di gestire il mapping delle allocazioni in questa granularità delle sottorisorse. Nel contesto delle risorse affiancate, "mapping" si riferisce al fatto che i dati siano visibili alla GPU.

Si supponga che un'applicazione sappia che un'operazione di rendering specifica deve solo accedere a una piccola parte di una catena di mipmap di immagini (probabilmente non anche all'area completa di un determinato mipmap). Idealmente, l'app potrebbe informare il sistema grafico in merito a questa esigenza. Il sistema grafico dovrebbe quindi solo assicurarsi che la memoria necessaria sia mappata sulla GPU senza eseguire il paging in troppa memoria. In realtà, senza il supporto delle risorse affiancate, il sistema grafico può essere informato solo sulla memoria di cui è necessario eseguire il mapping sulla GPU a livello di granularità delle risorse (ad esempio, un intervallo di livelli di mipmap completi a cui è possibile accedere). Non vi è alcuna richiesta di errori nel sistema grafico, quindi è necessario usare potenzialmente una quantità eccessiva di memoria GPU per eseguire il mapping delle sottorisorse complete prima che venga eseguito un comando di rendering che fa riferimento a una parte della memoria. Questo è solo un problema che rende difficile l'uso di allocazioni di memoria di grandi dimensioni in Direct3D senza supporto delle risorse affiancate.

Direct3D 11 supporta le superfici [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) con un massimo di 16384 pixel su un lato specifico. Un'immagine di 16384 in larghezza per 16384 di altezza e 4 byte per pixel utilizzerebbe 1 GB di memoria video (e l'aggiunta di mipmap sarebbe raddoppiata). In pratica, è necessario fare riferimento a tutti i GB in un'unica operazione di rendering.

Alcuni sviluppatori di giochi modellano le superfici del terreno fino a 128 KB per 128 KB. Il modo in cui si ottiene questo lavoro sulle GPU esistenti è suddividere l'area in riquadri sufficientemente piccoli da poter gestire l'hardware. L'applicazione deve determinare quali riquadri potrebbero essere necessari e caricarli in una cache di trame nel sistema di paging GPU, un software. Uno svantaggio significativo di questo approccio deriva dall'hardware che non è in grado di conoscere il paging che sta succedendo: quando una parte di un'immagine deve essere mostrata sullo schermo che occupa i riquadri, l'hardware non è in grado di eseguire il filtraggio di una funzione fissa (ovvero efficiente) tra i riquadri. Ciò significa che l'applicazione che gestisce il proprio affiancamento software deve ricorrere al filtro di trama manuale nel codice dello shader (che diventa molto costosa se si desidera un filtro anisotropico di qualità elevata) e/o sprecare le grondature di creazione della memoria intorno ai riquadri contenenti dati provenienti da riquadri adiacenti, in modo che i filtri hardware per funzioni fisse possano continuare a fornire assistenza

Se una rappresentazione affiancata delle allocazioni di superficie può essere una funzionalità di prima classe nel sistema grafico, l'applicazione potrebbe indicare all'hardware quali riquadri rendere disponibili. In questo modo, una minore quantità di memoria GPU viene sprecata per archiviare le aree di superficie che l'applicazione sa non sarà accessibile e l'hardware è in grado di comprendere come filtrare tra i riquadri adiacenti, attenuando alcune delle problematiche riscontrate dagli sviluppatori che eseguono autonomamente l'affiancamento software.

Tuttavia, per fornire una soluzione completa, è necessario eseguire un'operazione per gestire il fatto che, indipendentemente dal fatto che l'affiancamento all'interno di una superficie sia supportata, la dimensione massima della superficie è attualmente 16384-Nowhere vicino al 128 KB + che le applicazioni desiderano già. È sufficiente che l'hardware per supportare dimensioni di trama più grandi sia un approccio, tuttavia ci sono costi e/o compromessi significativi per l'itinerario. Il percorso del filtro di trama e il percorso di rendering di Direct3D 11 sono già saturi in termini di precisione nel supporto delle trame 16K con gli altri requisiti, ad esempio il supporto degli extent del viewport che non rientrano nell'area durante il rendering o il wrapping del bordo della superficie durante il filtro. Una possibilità consiste nel definire un compromesso in modo tale che, quando le dimensioni della trama aumentano oltre 16K, le funzionalità e la precisione vengono fornite in qualche modo. Anche con questa concessione, tuttavia, potrebbero essere necessari costi hardware aggiuntivi in termini di funzionalità di indirizzamento nel sistema hardware per passare a dimensioni di trama maggiori.

Un problema che si verifica come una trama è molto grande è che le coordinate di trama a virgola mobile e precisione singola (e gli interpolatori associati per supportare la rasterizzazione) hanno esaurito la precisione per specificare accuratamente i percorsi sulla superficie. Si verificherà un filtro di trama di Jittery. Una delle opzioni più dispendiose è la necessità di supportare l'interpolazione a precisione doppia, sebbene questo possa essere eccessivo in base a una ragionevole alternativa.

Un nome alternativo per le risorse affiancate è "trama sparse". "Sparse" fornisce sia la natura affiancata delle risorse sia il motivo principale per affiancarli, che non tutti devono essere mappati in una sola volta. In realtà, un'applicazione potrebbe in teoria creare una risorsa affiancata in cui nessun dato venga creato per tutte le aree + MIPS della risorsa, intenzionalmente. Il contenuto stesso potrebbe pertanto essere di tipo sparse e il mapping del contenuto nella memoria GPU in un determinato momento sarà un subset di tale contenuto (anche più sparse).

Un altro scenario che può essere servito dalle risorse affiancate consiste nell'abilitare più risorse di dimensioni/formati diversi per la condivisione della stessa memoria. A volte le applicazioni hanno set esclusivi di risorse che non devono essere usate contemporaneamente o risorse create solo per un breve utilizzo e quindi distrutte, seguite dalla creazione di altre risorse. Una forma di generalizzazione che può rientrare nelle "risorse affiancate" è che è possibile consentire all'utente di puntare più risorse diverse alla stessa memoria (sovrapposta). In altre parole, la creazione e l'eliminazione di "risorse", che definiscono una dimensione/un formato e così via, possono essere separate dalla gestione della memoria sottostante le risorse dal punto di vista dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse affiancate](tiled-resources.md)
</dt> </dl>

 

 