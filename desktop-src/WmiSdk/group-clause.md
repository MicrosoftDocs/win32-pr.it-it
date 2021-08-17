---
description: La clausola GROUP fa in modo che WMI generi una singola notifica per rappresentare un gruppo di eventi.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: Clausola GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4f5f796c563376853896213c5418039ac0104d04437ec7c9e0b444db6692e60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993181"
---
# <a name="group-clause"></a>Clausola GROUP

La clausola GROUP fa in modo che WMI generi una singola notifica per rappresentare un gruppo di eventi. La notifica rappresentativa è un'istanza della [**\_ \_ classe di sistema AggregateEvent.**](--aggregateevent.md) La **\_ \_ classe di sistema AggregateEvent** contiene due proprietà: **Representative** e **NumberOfEvents**. La **proprietà Representative** è un oggetto incorporato che contiene una delle istanze ricevute durante l'intervallo di raggruppamento specificato nella clausola [WITHIN.](within-clause.md) Ad esempio, se viene generato un evento di aggregazione per notificare gli eventi di modifica dell'istanza, **Representative** contiene un'istanza della [**\_ \_ classe InstanceModificationEvent.**](--instancemodificationevent.md) La **proprietà NumberOfEvents** contiene il numero di eventi ricevuti durante l'intervallo di raggruppamento. L'intervallo di raggruppamento specifica il periodo di tempo, dopo la ricezione di un evento iniziale, durante il quale WMI deve raccogliere eventi simili.

La clausola GROUP deve contenere una clausola WITHIN per specificare l'intervallo di raggruppamento e può contenere la parola chiave BY o HAVING o entrambe. La clausola GROUP viene inserita dopo la clausola WHERE, come illustrato di seguito:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

Il *valore EventClass* è la classe di evento di cui l'evento è membro e *value* è il valore per la proprietà in cui è richiesta la notifica. L'intervallo è un intero senza segno che rappresenta l'intervallo di raggruppamento dopo la ricezione del primo evento. L'intero senza segno è un numero di secondi. L'elenco di proprietà è un elenco delimitato da virgole di una o più proprietà incluse nella classe di evento . *operator* è qualsiasi operatore relazionale. e *integer* è un intero senza segno a 32 bit che indica un numero di eventi.

Quando si usa la clausola GROUP, le clausole WHERE, BY e HAVING sono facoltative.

Un uso di base della clausola GROUP potrebbe richiedere un raggruppamento di eventi all'interno di un intervallo di tempo che inizia quando viene ricevuto il primo evento. Ad esempio, la query seguente raggruppa tutti gli eventi di posta elettronica inviati entro 5 minuti. Invece di eseguire il paging di un utente ogni volta che viene ricevuto un nuovo messaggio di posta elettronica, il consumer permanente potrebbe usare questa query per informare l'utente solo se è stato ricevuto un nuovo messaggio di posta elettronica negli ultimi 5 minuti.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



Se sono necessarie informazioni più dettagliate, gli eventi possono essere raggruppati in base a una o più proprietà della classe di evento. La query seguente richiede che gli eventi di posta elettronica siano combinati con altri eventi con lo stesso valore nella **proprietà Sender:**


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



È possibile ottenere un livello di dettaglio ancora maggiore aggiungendo una clausola WHERE. Ad esempio, la query seguente notifica a un utente un nuovo messaggio di posta elettronica da un determinato mittente che è arrivato negli ultimi 10 minuti, in combinazione con altri eventi che hanno lo stesso valore nella proprietà **Importance:**


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



