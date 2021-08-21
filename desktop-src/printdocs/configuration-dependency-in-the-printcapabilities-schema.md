---
title: Dipendenza di configurazione PrintCapabilities
description: Le dipendenze di configurazione si riferiscono al fatto che alcuni elementi possono essere modificati o addirittura eliminati da un documento PrintCapabilities a quello successivo.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56e05e7b41ecfacf26556cdc7c38fa00087b440e92b476b2d6121f7ee082574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950461"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Dipendenza di configurazione nello schema PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema PrintCapabilities è strettamente parallelo a Print Schema Framework, in termini di elementi usati e della struttura generale espressa dagli elementi padre e figlio. Le dipendenze di configurazione, che riguardano in modo specifico PrintCapabilities, sono elencate di seguito come estensione del framework generale. Le dipendenze di configurazione si riferiscono al fatto che alcuni elementi, incluso il relativo contenuto, possono essere modificati o addirittura eliminati da un documento PrintCapabilities al successivo, come risultato delle dipendenze dalla configurazione. Anche se è necessario che un elemento padre sia indipendente dalla configurazione, gli elementi figlio potrebbero avere dipendenze. Tali dipendenze vengono espresse usando \* costrutti \* Switch/Case nei file GPD.

Come esempio di dipendenza di configurazione, prendere in considerazione i valori associati a ogni proprietà nel documento PrintCapabilities. Ogni documento PrintCapabilities può differire nelle istanze Property definite e nelle istanze Value assegnate a tali istanze property.



| Tipo di elemento                                                                                                                                                                             | Dipendenza di configurazione                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funzionalità <br/> Opzione<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Proprietà<br/> ScoredProperty<br/> | Questi elementi non devono avere dipendenze di configurazione.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | Gli elementi ParameterDef e gli elementi contenuti in essi in qualsiasi livello di annidamento non devono avere dipendenze di configurazione.<br/>                                                                                        |
| Proprietà <br/>                                                                                                                                                                     | Gli elementi proprietà possono avere dipendenze di configurazione, tranne quando vengono visualizzati all'interno di elementi ParameterDef.<br/>                                                                                                       |
| Valore <br/>                                                                                                                                                                        | Gli elementi value visualizzati all'interno degli elementi ScoredProperty non devono avere dipendenze di configurazione. Gli elementi valore visualizzati all'interno di un elemento Property possono avere dipendenze arbitrarie dalla configurazione.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




