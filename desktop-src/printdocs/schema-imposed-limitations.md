---
description: Informazioni sulle limitazioni imposte dallo schema PrintCapabilities. Il provider PrintCapabilities deve rilevare le configurazioni non valide e risolverle.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Schema-Imposed limitazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404924"
---
# <a name="schema-imposed-limitations"></a>Schema-Imposed limitazioni

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema PrintCapabilities offre agli autori PrintCapabilities una notevole quantità di flessibilità ed espressività che possono essere utilizzate nelle descrizioni dei dispositivi. Tuttavia, le dipendenze di configurazione impongono una limitazione a questa flessibilità ed espressività. Le istanze ParameterDef, l'elenco di elementi Feature, l'elenco di istanze Option all'interno di ogni feature e le istanze ScoredProperty all'interno di ogni opzione non devono contenere dipendenze di configurazione. Il provider di documenti PrintCapabilities deve rilevare combinazioni di configurazioni non valide e risolverle.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



