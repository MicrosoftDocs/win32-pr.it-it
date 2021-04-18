---
description: La clausola HAVING viene utilizzata per filtrare gli eventi ricevuti durante l'intervallo di raggruppamento specificato nella clausola all'interno di.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: Clausola HAVING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f93fbe082fb2f655dfad59d7642e1d0ff9a33e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318187"
---
# <a name="having-clause"></a>Clausola HAVING

La clausola HAVING viene utilizzata per filtrare gli eventi ricevuti durante l'intervallo di raggruppamento specificato nella [clausola all'interno](within-clause.md)di. È ad esempio possibile costruire un'istruzione SELECT in modo che non restituisca nulla a meno che non ci siano stati almeno 5 eventi negli ultimi 30 secondi di intervallo.

La clausola all'interno di segue immediatamente nell' [istruzione SELECT](select-statement-for-event-queries.md) dopo la clausola [Group](group-clause.md) . La clausola HAVING opera sulla proprietà **NumberOfEvents** della classe di sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) , di cui il gruppo creato dalla clausola Group è un membro. La clausola HAVING può utilizzare tutti gli operatori relazionali standard.

La sintassi è la seguente:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

Il valore *EventClass* è la classe di evento di cui l'evento è membro e *value* è il valore della proprietà in cui è richiesta la notifica. L'intervallo è un Unsigned Integer che rappresenta l'intervallo di raggruppamento (in secondi) dopo la ricezione del primo evento. L'elenco di proprietà è un elenco delimitato da virgole di una o più proprietà incluse nella classe di evento. L'operatore è qualsiasi operatore relazionale. Il valore costante è qualsiasi intero senza segno a 32 bit che indica il numero di eventi utilizzati per il filtro.

Quando si utilizza la clausola HAVING, le clausole WHERE e BY sono facoltative.

La query di eventi seguente richiede che le notifiche della classe **EmailEvent** vengano raggruppate in un evento 300 secondi dopo il primo evento ricevuto da WMI. Inoltre, la query richiede che l'istanza di [**\_ \_ AggregateEvent**](--aggregateevent.md) venga recapitata solo se WMI riceve più di cinque eventi di posta elettronica in 300 secondi.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



Nell'esempio seguente vengono raggruppati tutti gli eventi ricevuti in 600 secondi (ovvero 10 minuti) da **TargetInstance**. Proprietà **SourceName** . In questo esempio gli eventi di aggregazione vengono recapitati solo se il numero di eventi [**\_ NTLogEvent Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) ricevuti dalla stessa origine supera 25. Tenere presente che l'operatore ISA causa la rappresentazione di un'istanza della classe **\_ NTLogEvent Win32** da parte della proprietà **TargetInstance** della classe di sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) .


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
