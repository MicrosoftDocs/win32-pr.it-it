---
title: Livelli hardware
description: I livelli di hardware dal livello 1 al livello 3 hanno risorse crescenti disponibili per la pipeline.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/15/2020
ms.locfileid: "104548782"
---
# <a name="hardware-tiers"></a>Livelli hardware

I livelli di hardware dal livello 1 al livello 3 hanno risorse crescenti disponibili per la pipeline.

-   [Limiti dipendenti dall'hardware](#limits-dependant-on-hardware)
-   [Limiti invariabili](#invariable-limits)
-   [Argomenti correlati](#related-topics)

## <a name="limits-dependant-on-hardware"></a>Limiti dipendenti dall'hardware



| Risorse disponibili per la pipeline                                                                                                              | Livello 1                                                                   | Livello 2        | Livello 3        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| Livelli di funzionalità                                                                                                                                   | 11.0 +                                                                    | 11.0 +         | 11.1 +         |
| Numero massimo di descrittori in un heap Constant Buffer View (CBV), Shader Resource View (SRV) o Unordered Access View (UAV) usato per il rendering | 1\.000.000                                                                | 1\.000.000     | 1.000.000 +    |
| Numero massimo di visualizzazioni del buffer costante in tutte le tabelle dei descrittori per fase shader                                                                | 14                                                                       | 14            | **heap completo** |
| Numero massimo di visualizzazioni delle risorse dello shader in tutte le tabelle dei descrittori per fase shader                                                                | 128                                                                      | **heap completo** | heap completo     |
| Numero massimo di viste di accesso non ordinate in tutte le tabelle dei descrittori in tutte le fasi                                                              | 64 per i livelli di funzionalità 11.1 +<br/> 8 per il livello di funzionalità 11<br/> | 64            | **heap completo** |
| Numero massimo di campioni in tutte le tabelle dei descrittori per fase shader                                                                             | 16                                                                       | **2048** | 2048     |



 

Le voci in **grassetto** evidenziano miglioramenti significativi rispetto al livello precedente.

Esiste una restrizione aggiuntiva per l'hardware di livello 1 che si applica a tutti gli heap e all'hardware di livello 2 che si applica agli heap CBV e UAV, che tutte le voci dell'heap dei descrittori incluse nelle tabelle dei descrittori nella firma radice *devono* essere popolate con i descrittori durante l'esecuzione dello shader, anche se lo shader (probabilmente a causa della dirama Non esiste alcuna restrizione per l'hardware di livello 3. Una mitigazione per questa restrizione è l'uso diligente dei [descrittori null](descriptors.md).

## <a name="invariable-limits"></a>Limiti invariabili

Il numero massimo di campioni in un heap del descrittore visibile dello shader è 2048.

Il numero massimo di campioni statici univoci tra le firme radice attive è 2032, che lascia 16 per i driver che necessitano dei propri Sampler.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap descrittore](descriptor-heaps.md)
</dt> <dt>

[Livelli di funzionalità hardware](hardware-feature-levels.md)
</dt> </dl>

 

 





