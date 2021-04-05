---
description: Utilizzare la clausola all nelle query di eventi per specificare un intervallo di polling o un intervallo di raggruppamento.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: Clausola WITHin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d863e2e71d52fe60aeed7697feeb1231164c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131151"
---
# <a name="within-clause"></a>Clausola WITHin

I consumer di eventi utilizzano la clausola all nelle query di eventi per specificare un *intervallo di polling* o un *intervallo di raggruppamento*.

Un intervallo di polling è l'intervallo usato da Strumentazione gestione Windows (WMI) per eseguire il polling del provider di dati responsabile della classe per [gli eventi intrinseci](determining-the-type-of-event-to-receive.md), di cui l'evento sottoposto a query è un membro. Questo intervallo rappresenta il tempo massimo che può trascorrere prima della consegna della notifica di un evento. Un consumer utilizza un intervallo di polling in una clausola WITHin quando il consumer richiede la notifica delle modifiche a una classe e non è disponibile un provider di eventi. Il consumer registra per un evento intrinseco e include l'intervallo di polling.

Per specificare un intervallo di polling, inserire la clausola all'interno immediatamente prima della clausola WHERE, come illustrato di seguito:


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



IntrinsicEventClass è la classe di evento intrinseca di cui l'evento è membro, Interval è l'intervallo di polling e value è il valore della proprietà in cui il consumer richiede la notifica.

L'intervallo di polling è un numero a virgola mobile e può essere frazionario per accettare valori inferiori a 1 secondo. Tuttavia, l'intervallo deve rappresentare un numero di secondi anziché un valore estremamente ridotto, ad esempio 0,001, perché la specifica di un valore troppo piccolo può causare il rifiuto dell'istruzione non valida da parte di WMI, a causa della natura a elevato utilizzo di risorse del polling. Poiché la maggior parte dei consumer di eventi non richiede notifiche immediate, è consigliabile usare un intervallo maggiore di 5 minuti.

Nell'esempio di query seguente viene richiesto che WMI verifichi ogni 10 secondi le modifiche apportate alle istanze della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) . Se un'istanza della classe viene modificata entro l'intervallo di polling specificato, viene inviato un evento di notifica per ogni modifica.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



A seconda della query, un provider di eventi e WMI possono condividere l'attività di invio di eventi. Ad esempio, un provider di eventi che supporta gli eventi delle classi di sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) e [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) e non gli eventi della classe di sistema [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) . La query seguente consente al provider di eventi di generare gli eventi di creazione e modifica quando si verificano e di recapitarli al momento della creazione. La query consente inoltre a WMI di generare eventi **\_ \_ InstanceDeletionEvent** ogni 10 (dieci) secondi utilizzando il meccanismo di polling.


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



È inoltre possibile utilizzare la clausola with per specificare un intervallo di raggruppamento. Un intervallo di raggruppamento è un intero senza segno a 32 bit che specifica il periodo di tempo, dopo la ricezione di un evento iniziale, durante il quale WMI deve raccogliere eventi simili. Quando questo periodo di tempo scade, WMI recapita l'evento di aggregazione, composto da tutti gli eventi simili. Per ulteriori informazioni, vedere [clausola Group](group-clause.md).

I consumer di eventi che si registrano per gli eventi che si verificano frequentemente utilizzano un intervallo di raggruppamento con la clausola WITHin. L'aggiunta di un gruppo all'interno della clausola WHERE in una query di evento comporta l'invio di un evento di aggregazione anziché di molti eventi da parte di WMI. L'evento di aggregazione è rappresentato dalla classe di sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) .

Per specificare un intervallo di raggruppamento, inserire la clausola all'interno immediatamente dopo la clausola GROUP.


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



EventClass è la classe di evento di cui l'evento è membro, value è il valore della proprietà in cui il consumer richiede la notifica e Interval è l'intervallo di raggruppamento.

Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).

I consumer di eventi permanenti possono essere creati con query di polling solo se si dispone di privilegi di amministratore.

 

 
