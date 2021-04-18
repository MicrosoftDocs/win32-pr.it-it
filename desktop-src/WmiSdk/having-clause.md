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
# <a name="having-clause"></a><span data-ttu-id="72274-103">Clausola HAVING</span><span class="sxs-lookup"><span data-stu-id="72274-103">HAVING Clause</span></span>

<span data-ttu-id="72274-104">La clausola HAVING viene utilizzata per filtrare gli eventi ricevuti durante l'intervallo di raggruppamento specificato nella [clausola all'interno](within-clause.md)di.</span><span class="sxs-lookup"><span data-stu-id="72274-104">The HAVING clause is used to filter the events that are received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="72274-105">È ad esempio possibile costruire un'istruzione SELECT in modo che non restituisca nulla a meno che non ci siano stati almeno 5 eventi negli ultimi 30 secondi di intervallo.</span><span class="sxs-lookup"><span data-stu-id="72274-105">For example, a SELECT statement could be constructed so that it returns nothing unless there HAVE been at least 5 events within the past 30 second INTERVAL.</span></span>

<span data-ttu-id="72274-106">La clausola all'interno di segue immediatamente nell' [istruzione SELECT](select-statement-for-event-queries.md) dopo la clausola [Group](group-clause.md) .</span><span class="sxs-lookup"><span data-stu-id="72274-106">The WITHIN clause follows immediately in the [SELECT statement](select-statement-for-event-queries.md) after the [GROUP](group-clause.md) clause.</span></span> <span data-ttu-id="72274-107">La clausola HAVING opera sulla proprietà **NumberOfEvents** della classe di sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) , di cui il gruppo creato dalla clausola Group è un membro.</span><span class="sxs-lookup"><span data-stu-id="72274-107">The HAVING clause operates on the **NumberOfEvents** property of the [**\_\_AggregateEvent**](--aggregateevent.md) system class, of which the group created by the GROUP clause is a member.</span></span> <span data-ttu-id="72274-108">La clausola HAVING può utilizzare tutti gli operatori relazionali standard.</span><span class="sxs-lookup"><span data-stu-id="72274-108">The HAVING clause can use all of the standard relational operators.</span></span>

<span data-ttu-id="72274-109">La sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="72274-109">The syntax is as follows:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

<span data-ttu-id="72274-110">Il valore *EventClass* è la classe di evento di cui l'evento è membro e *value* è il valore della proprietà in cui è richiesta la notifica.</span><span class="sxs-lookup"><span data-stu-id="72274-110">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="72274-111">L'intervallo è un Unsigned Integer che rappresenta l'intervallo di raggruppamento (in secondi) dopo la ricezione del primo evento.</span><span class="sxs-lookup"><span data-stu-id="72274-111">The interval is an unsigned integer that represents the grouping interval (in seconds) after receiving the first event.</span></span> <span data-ttu-id="72274-112">L'elenco di proprietà è un elenco delimitato da virgole di una o più proprietà incluse nella classe di evento.</span><span class="sxs-lookup"><span data-stu-id="72274-112">The property list is a comma-delimited list of one or more properties that are included in the event class.</span></span> <span data-ttu-id="72274-113">L'operatore è qualsiasi operatore relazionale.</span><span class="sxs-lookup"><span data-stu-id="72274-113">The operator is any relational operator.</span></span> <span data-ttu-id="72274-114">Il valore costante è qualsiasi intero senza segno a 32 bit che indica il numero di eventi utilizzati per il filtro.</span><span class="sxs-lookup"><span data-stu-id="72274-114">The constant value is any unsigned 32-bit integer indicating the number of events used for filtering.</span></span>

<span data-ttu-id="72274-115">Quando si utilizza la clausola HAVING, le clausole WHERE e BY sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="72274-115">When using the HAVING clause, the WHERE and BY clauses are optional.</span></span>

<span data-ttu-id="72274-116">La query di eventi seguente richiede che le notifiche della classe **EmailEvent** vengano raggruppate in un evento 300 secondi dopo il primo evento ricevuto da WMI.</span><span class="sxs-lookup"><span data-stu-id="72274-116">The following event query requests that notifications of the **EmailEvent** class be grouped into one event 300 seconds after the first event that WMI receives.</span></span> <span data-ttu-id="72274-117">Inoltre, la query richiede che l'istanza di [**\_ \_ AggregateEvent**](--aggregateevent.md) venga recapitata solo se WMI riceve più di cinque eventi di posta elettronica in 300 secondi.</span><span class="sxs-lookup"><span data-stu-id="72274-117">Also, the query requests the [**\_\_AggregateEvent**](--aggregateevent.md) instance should be delivered only if WMI receives more than five email events in that 300 seconds.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



<span data-ttu-id="72274-118">Nell'esempio seguente vengono raggruppati tutti gli eventi ricevuti in 600 secondi (ovvero 10 minuti) da **TargetInstance**. Proprietà **SourceName** .</span><span class="sxs-lookup"><span data-stu-id="72274-118">The following example groups all events received in 600 seconds (that is, 10 minutes) by the **TargetInstance**.**SourceName** property.</span></span> <span data-ttu-id="72274-119">In questo esempio gli eventi di aggregazione vengono recapitati solo se il numero di eventi [**\_ NTLogEvent Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) ricevuti dalla stessa origine supera 25.</span><span class="sxs-lookup"><span data-stu-id="72274-119">In this example, aggregate events are delivered only if the number of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) events received from the same source exceeds 25.</span></span> <span data-ttu-id="72274-120">Tenere presente che l'operatore ISA causa la rappresentazione di un'istanza della classe **\_ NTLogEvent Win32** da parte della proprietà **TargetInstance** della classe di sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) .</span><span class="sxs-lookup"><span data-stu-id="72274-120">Keep in mind that the ISA operator causes the **TargetInstance** property of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) system class to represent an instance of the **Win32\_NTLogEvent** class.</span></span>


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
