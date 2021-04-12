---
description: Viene descritta la sintassi di base di un'istruzione SELECT per le query di eventi.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Istruzione SELECT per le query di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233460"
---
# <a name="select-statement-for-event-queries"></a><span data-ttu-id="25a26-103">Istruzione SELECT per le query di eventi</span><span class="sxs-lookup"><span data-stu-id="25a26-103">SELECT Statement for Event Queries</span></span>

<span data-ttu-id="25a26-104">È possibile utilizzare un'ampia gamma di istruzioni SELECT per eseguire una query per le informazioni sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="25a26-104">You can use a variety of SELECT statements to query for event information.</span></span> <span data-ttu-id="25a26-105">Le istruzioni possono essere istruzioni di base oppure possono essere più restrittive per limitare il set di risultati restituito dalla query.</span><span class="sxs-lookup"><span data-stu-id="25a26-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="25a26-106">L'esempio seguente è un'istruzione SELECT di base utilizzata per eseguire una query per ottenere informazioni sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="25a26-106">The following example is a basic SELECT statement that is used to query for event information.</span></span>


```sql
SELECT * FROM EventClass
```



<span data-ttu-id="25a26-107">Quando un consumer invia una query, si tratta di una richiesta di notifica di tutte le occorrenze dell'evento rappresentato da **EventClass**.</span><span class="sxs-lookup"><span data-stu-id="25a26-107">When a consumer submits a query, it is a request to be notified of all occurrences of the event represented by **EventClass**.</span></span> <span data-ttu-id="25a26-108">Questa richiesta include una richiesta di notifica relativa a tutte le proprietà del sistema di eventi e non di sistema.</span><span class="sxs-lookup"><span data-stu-id="25a26-108">This request includes a request for notification about all of the event system and nonsystem properties.</span></span> <span data-ttu-id="25a26-109">Quando un provider di eventi invia una query, registra il supporto per la generazione di notifiche quando si verifica un evento rappresentato da **EventClass** .</span><span class="sxs-lookup"><span data-stu-id="25a26-109">When an event provider submits a query, it registers support for generating notifications when an event represented by **EventClass** occurs.</span></span>

<span data-ttu-id="25a26-110">I consumer possono specificare singole proprietà anziché l'asterisco ( \* ) nell'istruzione SELECT.</span><span class="sxs-lookup"><span data-stu-id="25a26-110">Consumers can specify individual properties instead of the asterisk (\*) in the SELECT statement.</span></span>

<span data-ttu-id="25a26-111">Nell'esempio seguente viene illustrato come eseguire una query per proprietà specifiche.</span><span class="sxs-lookup"><span data-stu-id="25a26-111">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



<span data-ttu-id="25a26-112">Tuttavia, tutte le proprietà di un oggetto incorporato vengono restituite, anche se la query specifica le proprietà dell'oggetto incorporato.</span><span class="sxs-lookup"><span data-stu-id="25a26-112">However, all of the properties of an embedded object are returned, even if the query specifies embedded object properties.</span></span>

<span data-ttu-id="25a26-113">Nell'esempio seguente vengono illustrate due query che restituiscono gli stessi dati.</span><span class="sxs-lookup"><span data-stu-id="25a26-113">The following example shows two queries that return the same data.</span></span>


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



<span data-ttu-id="25a26-114">Se una proprietà di sistema non è pertinente per una query specifica, contiene **null**.</span><span class="sxs-lookup"><span data-stu-id="25a26-114">If a system property is not relevant for a specific query, it contains **NULL**.</span></span> <span data-ttu-id="25a26-115">Ad esempio, il valore della proprietà di sistema **\_ \_ RelPath** è **null** per tutte le query di eventi.</span><span class="sxs-lookup"><span data-stu-id="25a26-115">For example, the value of the **\_\_RELPATH** system property is **NULL** for all event queries.</span></span>

<span data-ttu-id="25a26-116">Le seguenti proprietà di sistema contengono **valori null** per le query di eventi:</span><span class="sxs-lookup"><span data-stu-id="25a26-116">The following system properties contain **NULL** for event queries:</span></span>

<dl> <span data-ttu-id="25a26-117">\_\_Namespace</span><span class="sxs-lookup"><span data-stu-id="25a26-117">\_\_Namespace</span></span>  
<span data-ttu-id="25a26-118">\_\_Percorso</span><span class="sxs-lookup"><span data-stu-id="25a26-118">\_\_Path</span></span>  
<span data-ttu-id="25a26-119">\_\_RelPath</span><span class="sxs-lookup"><span data-stu-id="25a26-119">\_\_RelPath</span></span>  
<span data-ttu-id="25a26-120">\_\_Server</span><span class="sxs-lookup"><span data-stu-id="25a26-120">\_\_Server</span></span>  
</dl>

<span data-ttu-id="25a26-121">Per ulteriori informazioni, vedere [riferimento alle proprietà di sistema WMI](wmi-system-properties.md).</span><span class="sxs-lookup"><span data-stu-id="25a26-121">For more information, see [WMI System Property Reference](wmi-system-properties.md).</span></span>

<span data-ttu-id="25a26-122">Tutte le query di evento possono includere una [clausola WHERE](where-clause.md)facoltativa, ma le clausole WHERE vengono utilizzate principalmente dai consumer per specificare filtri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="25a26-122">All event queries can include an optional [WHERE clause](where-clause.md), but WHERE clauses are primarily used by consumers to specify additional filtering.</span></span> <span data-ttu-id="25a26-123">È vivamente consigliabile che i consumer specifichino sempre una clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="25a26-123">It is strongly recommended that consumers always specify a WHERE clause.</span></span> <span data-ttu-id="25a26-124">Il costo di una query complessa è minimo rispetto al costo della distribuzione e dell'elaborazione delle notifiche non necessarie.</span><span class="sxs-lookup"><span data-stu-id="25a26-124">The cost of a complex query is minimal compared to the cost of delivering and processing unneeded notifications.</span></span>

<span data-ttu-id="25a26-125">Nell'esempio seguente viene illustrata una query che richiede notifiche di tutti gli eventi di modifica dell'istanza che interessano la classe ipotetica **EmailEvent**.</span><span class="sxs-lookup"><span data-stu-id="25a26-125">The following example shows a query that requests notifications of all instance modification events that affect the hypothetical class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent
```



<span data-ttu-id="25a26-126">Se gli eventi associati a **EmailEvent** si verificano di frequente, il consumer viene invaso da eventi.</span><span class="sxs-lookup"><span data-stu-id="25a26-126">If events associated with **EmailEvent** occur frequently, the consumer is flooded with events.</span></span> <span data-ttu-id="25a26-127">Una query migliore richiede gli eventi solo quando determinate condizioni utilizzano proprietà della classe specificata, ad esempio quando il livello di importanza è elevato.</span><span class="sxs-lookup"><span data-stu-id="25a26-127">A better query requests events only when specific conditions use properties of the class specified, such as when the importance level is high.</span></span>

<span data-ttu-id="25a26-128">Nell'esempio seguente viene illustrata la query che è possibile usare se **EmailImportance** è una proprietà della classe **EmailEvent**.</span><span class="sxs-lookup"><span data-stu-id="25a26-128">The following example shows the query you can use if **EmailImportance** is a property of the class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



<span data-ttu-id="25a26-129">Si noti che WMI può rifiutare una query per diversi motivi.</span><span class="sxs-lookup"><span data-stu-id="25a26-129">Note that WMI can reject a query for a number of reasons.</span></span> <span data-ttu-id="25a26-130">Ad esempio, la query può essere troppo complessa o con un utilizzo intensivo di risorse per la valutazione.</span><span class="sxs-lookup"><span data-stu-id="25a26-130">For example, the query can be too complex or resource-intensive for evaluation.</span></span> <span data-ttu-id="25a26-131">Quando si verifica questa situazione, WMI restituisce codici di errore specifici, ad esempio la **\_ query WBEM E \_ non valida \_**.</span><span class="sxs-lookup"><span data-stu-id="25a26-131">When this occurs, WMI returns specific error codes, such as **WBEM\_E\_INVALID\_QUERY**.</span></span>

<span data-ttu-id="25a26-132">È possibile utilizzare le proprietà degli oggetti incorporati nella clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="25a26-132">Properties of embedded objects can be used in the WHERE clause.</span></span>

<span data-ttu-id="25a26-133">Nell'esempio seguente viene illustrato come eseguire una query per gli oggetti in cui la proprietà **TargetInstance** della classe di sistema [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) è un oggetto [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) incorporato e **FreeSpace** è una proprietà di **Win32 \_ disco logico**.</span><span class="sxs-lookup"><span data-stu-id="25a26-133">The following example shows how to query for objects where the **TargetInstance** property of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system class is an embedded [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) object and **FreeSpace** is a property of **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a><span data-ttu-id="25a26-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="25a26-134">Examples</span></span>

<span data-ttu-id="25a26-135">L' [evento di creazione del monitoraggio per](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) un esempio di nome di processo specifico VBScript in TechNet utilizza l'istruzione SELECT per monitorare gli eventi di creazione dell'istanza WMI per \_ il processo Win32, filtrando il nome di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="25a26-135">The [Monitor creation event for specific process name](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript sample on TechNet uses the SELECT statement to monitor WMI instance creation events for Win32\_Process, filtering for a specific process name.</span></span>

 

 
