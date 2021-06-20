---
title: Dipendenza di configurazione PrintCapabilities
description: Le dipendenze di configurazione si riferiscono al fatto che alcuni elementi possono essere modificati o persino eliminati da un documento PrintCapabilities a quello successivo.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20f01c8e7bd9a036a53048996ec5a38246471f67
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409664"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Dipendenza di configurazione nello schema PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema PrintCapabilities è strettamente parallelo a Print Schema Framework, in termini di elementi usati e della struttura generale espressa dagli elementi padre e figlio. Le dipendenze di configurazione, che riguardano in modo specifico PrintCapabilities, sono elencate qui come estensione del framework generale. Le dipendenze di configurazione si riferiscono al fatto che alcuni elementi, incluso il relativo contenuto, possono essere modificati o persino eliminati da un documento PrintCapabilities a quello successivo, a causa delle dipendenze dalla configurazione. Anche se un elemento padre deve essere indipendente dalla configurazione, gli elementi figlio potrebbero avere dipendenze. Tali dipendenze vengono espresse usando \* costrutti \* Switch/Case nei file GPD.

Come esempio di dipendenza di configurazione, prendere in considerazione i valori associati a ogni proprietà nel documento PrintCapabilities. Ogni documento PrintCapabilities può differire nelle istanze Property definite e nelle istanze Value assegnate a tali istanze Property.



| Tipo di elemento                                                                                                                                                                             | Dipendenza di configurazione                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funzionalità <br/> Opzione<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Proprietà<br/> ScoredProperty<br/> | Questi elementi non devono avere dipendenze di configurazione.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | Gli elementi ParameterDef e gli elementi contenuti al loro interno a qualsiasi livello di annidamento non devono avere dipendenze di configurazione.<br/>                                                                                        |
| Proprietà <br/>                                                                                                                                                                     | Gli elementi proprietà possono avere dipendenze di configurazione, tranne quando vengono visualizzati all'interno di elementi ParameterDef.<br/>                                                                                                       |
| Valore <br/>                                                                                                                                                                        | Gli elementi value visualizzati all'interno degli elementi ScoredProperty non devono avere dipendenze di configurazione. Gli elementi valore visualizzati all'interno di un elemento Property possono avere dipendenze arbitrarie nella configurazione.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




