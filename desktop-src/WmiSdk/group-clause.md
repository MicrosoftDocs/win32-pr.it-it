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
# <a name="group-clause"></a><span data-ttu-id="82832-103">Clausola GROUP</span><span class="sxs-lookup"><span data-stu-id="82832-103">GROUP Clause</span></span>

<span data-ttu-id="82832-104">La clausola GROUP determina la generazione di una singola notifica da parte di WMI per rappresentare un gruppo di eventi.</span><span class="sxs-lookup"><span data-stu-id="82832-104">The GROUP clause causes WMI to generate a single notification to represent a group of events.</span></span> <span data-ttu-id="82832-105">La notifica rappresentativa è un'istanza della classe di sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="82832-105">The representative notification is an instance of the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span> <span data-ttu-id="82832-106">La classe di sistema **\_ \_ AggregateEvent** contiene due proprietà, **rappresentative** e **NumberOfEvents**.</span><span class="sxs-lookup"><span data-stu-id="82832-106">The **\_\_AggregateEvent** system class contains two properties: **Representative** and **NumberOfEvents**.</span></span> <span data-ttu-id="82832-107">La proprietà **rappresentativa** è un oggetto incorporato che contiene una delle istanze ricevute durante l'intervallo di raggruppamento specificato nella [clausola all'interno](within-clause.md)di.</span><span class="sxs-lookup"><span data-stu-id="82832-107">The **Representative** property is an embedded object that contains one of the instances received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="82832-108">Se, ad esempio, viene generato un evento di aggregazione per notificare gli eventi di modifica dell'istanza, **rappresentativo** contiene un'istanza della classe [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) .</span><span class="sxs-lookup"><span data-stu-id="82832-108">For example, if an aggregate event is generated to notify of instance modification events, **Representative** contains one instance of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) class.</span></span> <span data-ttu-id="82832-109">La proprietà **NumberOfEvents** contiene il numero di eventi ricevuti durante l'intervallo di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="82832-109">The **NumberOfEvents** property contains the number of events received during the grouping interval.</span></span> <span data-ttu-id="82832-110">L'intervallo di raggruppamento specifica il periodo di tempo, dopo la ricezione di un evento iniziale durante il quale WMI deve raccogliere eventi simili.</span><span class="sxs-lookup"><span data-stu-id="82832-110">The grouping interval specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span>

<span data-ttu-id="82832-111">La clausola GROUP deve contenere una clausola WITHin per specificare l'intervallo di raggruppamento e può contenere la parola chiave BY o HAVING oppure entrambe.</span><span class="sxs-lookup"><span data-stu-id="82832-111">The GROUP clause must contain a WITHIN clause to specify the grouping interval and can contain the BY or HAVING keyword, or both.</span></span> <span data-ttu-id="82832-112">La clausola GROUP viene posizionata dopo la clausola WHERE, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="82832-112">The GROUP clause is placed after the WHERE clause, as shown following:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

<span data-ttu-id="82832-113">Il valore *EventClass* è la classe di evento di cui l'evento è membro e *value* è il valore della proprietà in cui è richiesta la notifica.</span><span class="sxs-lookup"><span data-stu-id="82832-113">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="82832-114">L'intervallo è un Unsigned Integer che rappresenta l'intervallo di raggruppamento dopo la ricezione del primo evento.</span><span class="sxs-lookup"><span data-stu-id="82832-114">The interval is an unsigned integer that represents the grouping interval after receiving the first event.</span></span> <span data-ttu-id="82832-115">Il Unsigned Integer è costituito da un numero di secondi.</span><span class="sxs-lookup"><span data-stu-id="82832-115">The unsigned integer is a number of seconds.</span></span> <span data-ttu-id="82832-116">L'elenco di proprietà è un elenco delimitato da virgole di una o più proprietà incluse nella classe di evento; *operator* è qualsiasi operatore relazionale. e *Integer* è un intero senza segno a 32 bit che indica una serie di eventi.</span><span class="sxs-lookup"><span data-stu-id="82832-116">The property list is a comma-delimited list of one or more properties that are included in the event class; *operator* is any relational operator; and *integer* is an unsigned 32-bit integer indicating a number of events.</span></span>

<span data-ttu-id="82832-117">Quando si utilizza la clausola GROUP, le clausole WHERE, BY e HAVING sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="82832-117">When using the GROUP clause, the WHERE, BY, and HAVING clauses are optional.</span></span>

<span data-ttu-id="82832-118">Un uso di base della clausola GROUP potrebbe richiedere un raggruppamento di eventi all'interno di un intervallo di tempo che inizia quando viene ricevuto il primo evento.</span><span class="sxs-lookup"><span data-stu-id="82832-118">A basic use of the GROUP clause might request a grouping of events within a time interval that starts when the first event is received.</span></span> <span data-ttu-id="82832-119">Ad esempio, la query seguente consente di raggruppare tutti gli eventi di posta elettronica inviati entro 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="82832-119">For example, the following query groups all of the email events sent within 5 minutes.</span></span> <span data-ttu-id="82832-120">Anziché eseguire il paging di un utente ogni volta che viene ricevuto un nuovo messaggio di posta elettronica, il consumer permanente può usare questa query per informare l'utente solo se è stato ricevuto un nuovo messaggio di posta elettronica negli ultimi 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="82832-120">Instead of paging a user every time a piece of new email is received, the permanent consumer might use this query to inform the user only if new email has been received within the last 5 minutes.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



<span data-ttu-id="82832-121">Se sono necessarie informazioni più dettagliate, gli eventi possono essere raggruppati in base a una o più proprietà della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="82832-121">If more detailed information is required, events can be grouped by one or more properties of the event class.</span></span> <span data-ttu-id="82832-122">La query seguente richiede che gli eventi di posta elettronica vengano combinati con altri eventi che hanno lo stesso valore nella proprietà **sender** :</span><span class="sxs-lookup"><span data-stu-id="82832-122">The following query requests that email events be combined with other events that have the same value in the **Sender** property:</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



<span data-ttu-id="82832-123">È possibile ottenere un livello di dettaglio ancora maggiore aggiungendo una clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="82832-123">A still greater level of detail can be achieved by adding a WHERE clause.</span></span> <span data-ttu-id="82832-124">Ad esempio, la query seguente informa un utente del nuovo messaggio di posta elettronica di un mittente specifico che è arrivato negli ultimi 10 minuti, combinato con altri eventi con lo stesso valore nella proprietà **priorità** :</span><span class="sxs-lookup"><span data-stu-id="82832-124">For example, the following query notifies a user of new email from a particular sender that has arrived within the last 10 minutes, combined with other events that have the same value in the **Importance** property:</span></span>


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



