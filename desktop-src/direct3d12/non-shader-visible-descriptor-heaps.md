---
title: Heap descrittori non shader visibili
description: Per gli shader non è possibile fare riferimento ad alcuni heap del descrittore tramite le tabelle dei descrittori, ma esistono per supportare l'app nella gestione temporanea dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile dello shader.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894640cde142f1241b088518ba7140ffb9405152
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548809"
---
# <a name="non-shader-visible-descriptor-heaps"></a>Heap descrittori non shader visibili

Per gli shader non è possibile fare riferimento ad alcuni heap del descrittore tramite le tabelle dei descrittori, ma esistono per supportare l'app nella gestione temporanea dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile dello shader.

-   [Viste non visibili](#non-visible-views)
-   [Summary](#summary)
-   [Argomenti correlati](#related-topics)

## <a name="non-visible-views"></a>Viste non visibili

Tutti gli heap dei descrittori, inclusi gli heap dei descrittori accessibili dello shader descritti in precedenza, possono essere modificati dagli elenchi della CPU e/o dei comandi a seconda del pool di memoria e delle proprietà di accesso alla CPU che l'applicazione seleziona per un heap del descrittore.

Per gli [heap del descrittore visibile dello shader](shader-visible-descriptor-heaps.md), il motivo più ovvio per negare l'accesso dello shader a questi heap di descrittori è mentre sono in fase di gestione temporanea. Questi heap, quindi, vengono resi visibili allo shader e sono accessibili tramite tabelle descrittore nell'esecuzione dell'elenco dei comandi. Tuttavia, non esiste alcun requisito per gestire gli heap visibili dello shader, che possono essere popolati direttamente.

Gli altri descrittori vengono associati alla pipeline con il relativo contenuto registrato direttamente nell'elenco dei comandi. Questi descrittori servono solo per tradurre i parametri di visualizzazione in fase di record dell'elenco dei comandi. Questi heap sono sempre visibili senza shader e contengono quanto segue.

-   Visualizzazioni destinazione rendering (RTVs)
-   Visualizzazioni stencil Depth (viste origine dati)

Le viste del buffer di indice (IBVs), le viste del buffer dei vertici (VBVs) e le viste di output del flusso (sovietici) vengono passate direttamente ai metodi API, non dispongono di tipi di heap specifici.

Dopo la registrazione nell'elenco dei comandi (ad esempio, con una chiamata come [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)), la memoria usata per conservare i descrittori per questa chiamata è immediatamente disponibile per essere riutilizzata dopo la chiamata.

Anche le tabelle dei descrittori includono opzioni in cui un'app può consentire all'implementazione di scegliere di registrare il contenuto della tabella nella registrazione dell'elenco di comandi, anziché dereferenziare il puntatore della tabella in fase di esecuzione.

## <a name="summary"></a>Riepilogo



|                   |                                    |                                        |
|-------------------|------------------------------------|----------------------------------------|
|                   | **shader visibile, solo scrittura CPU** | **non shader visibile, lettura/scrittura CPU** |
| **CBV, SRV, UAV** | sì                                | sì                                    |
| **CAMPIONATORE**       | sì                                | sì                                    |
| **RTV**           | no                                 | sì                                    |
| **DSV**           | no                                 | sì                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap descrittore](descriptor-heaps.md)
</dt> </dl>

 

 




