---
description: La clausola HAVING viene usata per filtrare gli eventi ricevuti durante l'intervallo di raggruppamento specificato nella clausola WITHIN.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: Clausola HAVING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2662ea337c5664130eb9973c049431daedefe3c947c45eb397a950522fea6bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993161"
---
# <a name="having-clause"></a>Clausola HAVING

La clausola HAVING viene usata per filtrare gli eventi ricevuti durante l'intervallo di raggruppamento specificato nella clausola [WITHIN](within-clause.md). Ad esempio, un'istruzione SELECT può essere costruita in modo che non restituisca nulla a meno che non siano stati generati almeno 5 eventi negli ultimi 30 secondi INTERVAL.

La clausola WITHIN segue immediatamente [nell'istruzione SELECT dopo](select-statement-for-event-queries.md) la [clausola GROUP.](group-clause.md) La clausola HAVING opera sulla **proprietà NumberOfEvents** della classe di sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) di cui è membro il gruppo creato dalla clausola GROUP. La clausola HAVING può usare tutti gli operatori relazionali standard.

La sintassi è la seguente:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

Il *valore EventClass* è la classe di evento di cui l'evento è membro e *value* è il valore per la proprietà in cui è richiesta la notifica. L'intervallo è un intero senza segno che rappresenta l'intervallo di raggruppamento (in secondi) dopo la ricezione del primo evento. L'elenco di proprietà è un elenco delimitato da virgole di una o più proprietà incluse nella classe di evento . L'operatore è qualsiasi operatore relazionale. Il valore costante è qualsiasi intero senza segno a 32 bit che indica il numero di eventi usati per il filtro.

Quando si usa la clausola HAVING, le clausole WHERE e BY sono facoltative.

La query di evento seguente richiede che le notifiche della classe **EmailEvent** siano raggruppate in un evento 300 secondi dopo il primo evento ricevuto da WMI. Inoltre, la query richiede che l'istanza [**\_ \_ AggregateEvent**](--aggregateevent.md) venga recapitata solo se WMI riceve più di cinque eventi di posta elettronica in 300 secondi.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



L'esempio seguente raggruppa tutti gli eventi ricevuti in 600 secondi (ovvero 10 minuti) da **TargetInstance**. **Proprietà SourceName.** In questo esempio gli eventi aggregati vengono recapitati solo se il numero di eventi [**\_ NTLogEvent Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) ricevuti dalla stessa origine supera 25. Tenere presente che l'operatore ISA fa sì che la proprietà **TargetInstance** della classe di sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) rappresenti un'istanza della **classe \_ NTLogEvent Win32.**


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
