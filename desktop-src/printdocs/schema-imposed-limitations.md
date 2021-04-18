---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Limitazioni Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc283704ea96e3303de6755a217e454b506bdc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321060"
---
# <a name="schema-imposed-limitations"></a>Limitazioni Schema-Imposed

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema PrintCapabilities fornisce agli autori PrintCapabilities un notevole livello di flessibilità ed espressività che possono essere utilizzati nelle descrizioni dei dispositivi. Tuttavia, le dipendenze di configurazione impongono una limitazione sulla flessibilità e sull'espressività. Le istanze di ParameterDef, l'elenco di elementi Feature, l'elenco delle istanze di opzioni all'interno di ogni funzionalità e le istanze di ScoredProperty all'interno di ogni opzione non devono contenere dipendenze di configurazione. Il provider di documenti PrintCapabilities deve rilevare combinazioni di configurazioni non valide e deve risolverle.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



