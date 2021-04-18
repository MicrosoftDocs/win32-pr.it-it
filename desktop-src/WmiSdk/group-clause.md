---
description: La clausola GROUP determina la generazione di una singola notifica da parte di WMI per rappresentare un gruppo di eventi.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: Clausola GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032a8e86c84c0b317b3739c0e203a249b432b0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318191"
---
# <a name="group-clause"></a>Clausola GROUP

La clausola GROUP determina la generazione di una singola notifica da parte di WMI per rappresentare un gruppo di eventi. La notifica rappresentativa è un'istanza della classe di sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) . La classe di sistema **\_ \_ AggregateEvent** contiene due proprietà, **rappresentative** e **NumberOfEvents**. La proprietà **rappresentativa** è un oggetto incorporato che contiene una delle istanze ricevute durante l'intervallo di raggruppamento specificato nella [clausola all'interno](within-clause.md)di. Se, ad esempio, viene generato un evento di aggregazione per notificare gli eventi di modifica dell'istanza, **rappresentativo** contiene un'istanza della classe [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) . La proprietà **NumberOfEvents** contiene il numero di eventi ricevuti durante l'intervallo di raggruppamento. L'intervallo di raggruppamento specifica il periodo di tempo, dopo la ricezione di un evento iniziale durante il quale WMI deve raccogliere eventi simili.

La clausola GROUP deve contenere una clausola WITHin per specificare l'intervallo di raggruppamento e può contenere la parola chiave BY o HAVING oppure entrambe. La clausola GROUP viene posizionata dopo la clausola WHERE, come illustrato di seguito:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

Il valore *EventClass* è la classe di evento di cui l'evento è membro e *value* è il valore della proprietà in cui è richiesta la notifica. L'intervallo è un Unsigned Integer che rappresenta l'intervallo di raggruppamento dopo la ricezione del primo evento. Il Unsigned Integer è costituito da un numero di secondi. L'elenco di proprietà è un elenco delimitato da virgole di una o più proprietà incluse nella classe di evento; *operator* è qualsiasi operatore relazionale. e *Integer* è un intero senza segno a 32 bit che indica una serie di eventi.

Quando si utilizza la clausola GROUP, le clausole WHERE, BY e HAVING sono facoltative.

Un uso di base della clausola GROUP potrebbe richiedere un raggruppamento di eventi all'interno di un intervallo di tempo che inizia quando viene ricevuto il primo evento. Ad esempio, la query seguente consente di raggruppare tutti gli eventi di posta elettronica inviati entro 5 minuti. Anziché eseguire il paging di un utente ogni volta che viene ricevuto un nuovo messaggio di posta elettronica, il consumer permanente può usare questa query per informare l'utente solo se è stato ricevuto un nuovo messaggio di posta elettronica negli ultimi 5 minuti.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



Se sono necessarie informazioni più dettagliate, gli eventi possono essere raggruppati in base a una o più proprietà della classe di evento. La query seguente richiede che gli eventi di posta elettronica vengano combinati con altri eventi che hanno lo stesso valore nella proprietà **sender** :


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



È possibile ottenere un livello di dettaglio ancora maggiore aggiungendo una clausola WHERE. Ad esempio, la query seguente informa un utente del nuovo messaggio di posta elettronica di un mittente specifico che è arrivato negli ultimi 10 minuti, combinato con altri eventi con lo stesso valore nella proprietà **priorità** :


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



