---
description: Usare la clausola WITHIN nelle query di evento per specificare un intervallo di polling o un intervallo di raggruppamento.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: Clausola WITHIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee35350a52ef6af1aa22aacf775d22b3c7629fb479967a74aed1408aa5e1f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757601"
---
# <a name="within-clause"></a>Clausola WITHIN

I consumer di eventi usano la clausola WITHIN nelle query di eventi per specificare un intervallo *di polling* o *un intervallo di raggruppamento.*

Un intervallo di polling è l'intervallo utilizzato da Windows Management Instrumentation (WMI) per eseguire il polling del provider di dati responsabile della classe per gli eventi intrinseci [,](determining-the-type-of-event-to-receive.md)di cui l'evento sottoposto a query è un membro. Questo intervallo rappresenta il tempo massimo che può trascorrere prima della consegna della notifica di un evento. Un consumer utilizza un intervallo di polling in una clausola WITHIN quando il consumer richiede la notifica delle modifiche a una classe e un provider di eventi non è disponibile. Il consumer esegue la registrazione per un evento intrinseco e include l'intervallo di polling.

Per specificare un intervallo di polling, inserire la clausola WITHIN immediatamente prima della clausola WHERE, come illustrato di seguito:


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



IntrinsicEventClass è la classe di evento intrinseca di cui l'evento è membro, interval è l'intervallo di polling e value è il valore per la proprietà in cui il consumer richiede la notifica.

L'intervallo di polling è un numero a virgola mobile e può essere frazionario per accettare valori inferiori a 1 secondo. Tuttavia, l'intervallo deve rappresentare un numero di secondi anziché un valore estremamente ridotto, ad esempio 0,001, perché se si specifica un valore troppo piccolo, WMI può rifiutare l'istruzione come non valida, a causa della natura a elevato utilizzo di risorse del polling. Poiché la maggior parte dei consumer di eventi non richiede una notifica immediata, è consigliabile usare un intervallo maggiore di 5 minuti.

L'esempio di query seguente richiede a WMI di controllare ogni 10 secondi le modifiche apportate alle istanze della [**classe \_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) Se un'istanza della classe viene modificata entro l'intervallo di polling specificato, viene inviato un evento di notifica per ogni modifica.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



A seconda della query, un provider di eventi e WMI possono condividere l'attività di fornire eventi. Ad esempio, un provider di eventi che supporta gli eventi delle classi di sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) e [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) e non gli eventi della classe di sistema [**\_ \_ InstanceDeletionEvent.**](--instancedeletionevent.md) La query seguente consente al provider di eventi di generare gli eventi di creazione e modifica non appena si verificano e di recapitarli al momento della creazione. La query consente inoltre a WMI di generare eventi **\_ \_ InstanceDeletionEvent** ogni 10 (dieci) secondi usando il meccanismo di polling.


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



È anche possibile usare la clausola WITHIN per specificare un intervallo di raggruppamento. Un intervallo di raggruppamento è un intero senza segno a 32 bit che specifica il periodo di tempo, dopo la ricezione di un evento iniziale, durante il quale WMI deve raccogliere eventi simili. Alla scadenza di questo periodo di tempo, WMI recapita l'evento aggregato, costituito da tutti gli eventi simili. Per altre informazioni, vedere [Clausola GROUP.](group-clause.md)

I consumer di eventi registrati per gli eventi che si verificano di frequente usano un intervallo di raggruppamento con la clausola WITHIN. L'aggiunta di GROUP WITHIN alla clausola WHERE in una query di eventi comporta l'invio da WMI di un evento aggregato anziché di molti eventi. L'evento di aggregazione è rappresentato dalla classe di sistema [**\_ \_ AggregateEvent.**](--aggregateevent.md)

Per specificare un intervallo di raggruppamento, inserire la clausola WITHIN immediatamente dopo la clausola GROUP.


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



EventClass è la classe di evento di cui l'evento è membro, value è il valore per la proprietà in cui il consumer richiede la notifica e Interval è l'intervallo di raggruppamento.

Per altre informazioni, vedere [Determinazione del tipo di evento da ricevere.](determining-the-type-of-event-to-receive.md)

I consumer di eventi permanenti possono essere creati con query di polling solo se si hanno privilegi di amministratore.

 

 
