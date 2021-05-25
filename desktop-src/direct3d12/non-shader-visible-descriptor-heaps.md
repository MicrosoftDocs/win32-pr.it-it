---
title: Heap dei descrittori non visibili allo shader
description: Gli shader non possono fare riferimento ad alcuni heap dei descrittori tramite tabelle di descrittori, ma esistono per aiutare l'app a eseguire lo staging dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile allo shader.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343456"
---
# <a name="non-shader-visible-descriptor-heaps"></a>Heap dei descrittori non visibili allo shader

Gli shader non possono fare riferimento ad alcuni heap dei descrittori tramite tabelle di descrittori, ma esistono per aiutare l'app a eseguire lo staging dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile allo shader.

-   [Visualizzazioni non visibili](#non-visible-views)
-   [Summary](#summary)
-   [Argomenti correlati](#related-topics)

## <a name="non-visible-views"></a>Visualizzazioni non visibili

Tutti gli heap dei descrittori, inclusi gli heap dei descrittori accessibili allo shader descritti in precedenza, possono essere manipolati dagli elenchi di CPU e/o comandi a seconda del pool di memoria e delle proprietà di accesso alla CPU selezionate dall'applicazione per un heap descrittore.

Per [gli heap dei descrittori](shader-visible-descriptor-heaps.md)visibili allo shader, l'ovvio motivo per negare l'accesso dello shader a questi heap dei descrittori è durante la fase di stage. Questi heap vengono quindi resi visibili allo shader e vi si accede tramite tabelle di descrittori durante l'esecuzione dell'elenco dei comandi. Tuttavia, non è necessario eseguire lo stage degli heap visibili allo shader, che possono essere popolati direttamente.

Altri descrittori vengono associati alla pipeline registrando il relativo contenuto direttamente nell'elenco dei comandi. Questi descrittori servono solo per convertire i parametri di visualizzazione al momento del record dell'elenco dei comandi. Questi heap sono sempre non visibili per lo shader e contengono quanto segue.

-   Rendering delle visualizzazioni di destinazione (RTV)
-   Visualizzazioni degli stencil di profondità (DSV)

Le viste IBV (Index Buffer Views), le viste vertex buffer (VBV) e le viste di output di flusso (SOV) vengono passate direttamente ai metodi API e non hanno tipi di heap specifici.

Dopo la registrazione nell'elenco dei comandi ,ad esempio con una chiamata come [**OMSetRenderTargets,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)la memoria usata per contenere i descrittori per questa chiamata è immediatamente disponibile per il nuovo uso dopo la chiamata.

Anche le tabelle descrittore hanno opzioni in cui un'app può consentire all'implementazione di scegliere di registrare il contenuto della tabella durante la registrazione dell'elenco dei comandi (anziché dereferenziare il puntatore di tabella in fase di esecuzione).

## <a name="summary"></a>Riepilogo



|                   | Shader visibile, solo scrittura CPU                                   | Non-shader visibile, lettura/scrittura della CPU                                       |
|-------------------|------------------------------------|----------------------------------------|
| **CBV, SRV, UAV** | Sì                                | Sì                                    |
| **Campionatore**       | Sì                                | Sì                                    |
| **RTV**           | No                                 | sì                                    |
| **Dsv**           | No                                 | sì                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap dei descrittori](descriptor-heaps.md)
</dt> </dl>

 

 




