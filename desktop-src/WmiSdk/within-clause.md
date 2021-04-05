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
# <a name="within-clause"></a><span data-ttu-id="b4dde-103">Clausola WITHin</span><span class="sxs-lookup"><span data-stu-id="b4dde-103">WITHIN Clause</span></span>

<span data-ttu-id="b4dde-104">I consumer di eventi utilizzano la clausola all nelle query di eventi per specificare un *intervallo di polling* o un *intervallo di raggruppamento*.</span><span class="sxs-lookup"><span data-stu-id="b4dde-104">Event consumers use the WITHIN clause in event queries to specify a *polling interval* or a *grouping interval*.</span></span>

<span data-ttu-id="b4dde-105">Un intervallo di polling è l'intervallo usato da Strumentazione gestione Windows (WMI) per eseguire il polling del provider di dati responsabile della classe per [gli eventi intrinseci](determining-the-type-of-event-to-receive.md), di cui l'evento sottoposto a query è un membro.</span><span class="sxs-lookup"><span data-stu-id="b4dde-105">A polling interval is the interval that Windows Management Instrumentation (WMI) uses to poll the data provider responsible for the class for [intrinsic events](determining-the-type-of-event-to-receive.md), of which the event queried is a member.</span></span> <span data-ttu-id="b4dde-106">Questo intervallo rappresenta il tempo massimo che può trascorrere prima della consegna della notifica di un evento.</span><span class="sxs-lookup"><span data-stu-id="b4dde-106">This interval is the maximum amount of time that can pass before notification of an event must be delivered.</span></span> <span data-ttu-id="b4dde-107">Un consumer utilizza un intervallo di polling in una clausola WITHin quando il consumer richiede la notifica delle modifiche a una classe e non è disponibile un provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="b4dde-107">A consumer uses a polling interval in a WITHIN clause when the consumer requires notification of changes to a class, and an event provider is unavailable.</span></span> <span data-ttu-id="b4dde-108">Il consumer registra per un evento intrinseco e include l'intervallo di polling.</span><span class="sxs-lookup"><span data-stu-id="b4dde-108">The consumer registers for an intrinsic event and includes the polling interval.</span></span>

<span data-ttu-id="b4dde-109">Per specificare un intervallo di polling, inserire la clausola all'interno immediatamente prima della clausola WHERE, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b4dde-109">To specify a polling interval, place the WITHIN clause immediately before the WHERE clause, as shown following:</span></span>


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



<span data-ttu-id="b4dde-110">IntrinsicEventClass è la classe di evento intrinseca di cui l'evento è membro, Interval è l'intervallo di polling e value è il valore della proprietà in cui il consumer richiede la notifica.</span><span class="sxs-lookup"><span data-stu-id="b4dde-110">IntrinsicEventClass is the intrinsic event class of which the event is a member, interval is the polling interval, and value is the value for the property on which the consumer requires notification.</span></span>

<span data-ttu-id="b4dde-111">L'intervallo di polling è un numero a virgola mobile e può essere frazionario per accettare valori inferiori a 1 secondo.</span><span class="sxs-lookup"><span data-stu-id="b4dde-111">The polling interval is a floating-point number, and can be fractional to accept values smaller than 1 second.</span></span> <span data-ttu-id="b4dde-112">Tuttavia, l'intervallo deve rappresentare un numero di secondi anziché un valore estremamente ridotto, ad esempio 0,001, perché la specifica di un valore troppo piccolo può causare il rifiuto dell'istruzione non valida da parte di WMI, a causa della natura a elevato utilizzo di risorse del polling.</span><span class="sxs-lookup"><span data-stu-id="b4dde-112">However, the interval should represent a number of seconds rather than an extremely small value such as 0.001, because specifying a value that is too small can cause WMI to reject the statement as not valid—due to the resource-intensive nature of polling.</span></span> <span data-ttu-id="b4dde-113">Poiché la maggior parte dei consumer di eventi non richiede notifiche immediate, è consigliabile usare un intervallo maggiore di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="b4dde-113">Because most event consumers do not require immediate notification, it is recommended that they use an interval that is greater than 5 minutes.</span></span>

<span data-ttu-id="b4dde-114">Nell'esempio di query seguente viene richiesto che WMI verifichi ogni 10 secondi le modifiche apportate alle istanze della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="b4dde-114">The following query example requests that WMI check every 10 seconds for changes that occur to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="b4dde-115">Se un'istanza della classe viene modificata entro l'intervallo di polling specificato, viene inviato un evento di notifica per ogni modifica.</span><span class="sxs-lookup"><span data-stu-id="b4dde-115">If an instance of the class is modified within the specified polling interval, a notification event is sent for each modification.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="b4dde-116">A seconda della query, un provider di eventi e WMI possono condividere l'attività di invio di eventi.</span><span class="sxs-lookup"><span data-stu-id="b4dde-116">Depending on the query, an event provider and WMI can share the task of providing events.</span></span> <span data-ttu-id="b4dde-117">Ad esempio, un provider di eventi che supporta gli eventi delle classi di sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) e [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) e non gli eventi della classe di sistema [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) .</span><span class="sxs-lookup"><span data-stu-id="b4dde-117">For example, an event provider that supports events of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) and [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system classes, and not events of the [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) system class.</span></span> <span data-ttu-id="b4dde-118">La query seguente consente al provider di eventi di generare gli eventi di creazione e modifica quando si verificano e di recapitarli al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="b4dde-118">The following query enables the event provider to generate the creation and modification events as they occur and have them delivered when they are created.</span></span> <span data-ttu-id="b4dde-119">La query consente inoltre a WMI di generare eventi **\_ \_ InstanceDeletionEvent** ogni 10 (dieci) secondi utilizzando il meccanismo di polling.</span><span class="sxs-lookup"><span data-stu-id="b4dde-119">The query also allows WMI to generate **\_\_InstanceDeletionEvent** events every 10 (ten) seconds using the polling mechanism.</span></span>


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



<span data-ttu-id="b4dde-120">È inoltre possibile utilizzare la clausola with per specificare un intervallo di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="b4dde-120">You can also use the WITHIN clause to specify a grouping interval.</span></span> <span data-ttu-id="b4dde-121">Un intervallo di raggruppamento è un intero senza segno a 32 bit che specifica il periodo di tempo, dopo la ricezione di un evento iniziale, durante il quale WMI deve raccogliere eventi simili.</span><span class="sxs-lookup"><span data-stu-id="b4dde-121">A grouping interval is an unsigned 32-bit integer that specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span> <span data-ttu-id="b4dde-122">Quando questo periodo di tempo scade, WMI recapita l'evento di aggregazione, composto da tutti gli eventi simili.</span><span class="sxs-lookup"><span data-stu-id="b4dde-122">When this time period expires, WMI delivers the aggregate event, made up of all the similar events.</span></span> <span data-ttu-id="b4dde-123">Per ulteriori informazioni, vedere [clausola Group](group-clause.md).</span><span class="sxs-lookup"><span data-stu-id="b4dde-123">For more information, see [GROUP Clause](group-clause.md).</span></span>

<span data-ttu-id="b4dde-124">I consumer di eventi che si registrano per gli eventi che si verificano frequentemente utilizzano un intervallo di raggruppamento con la clausola WITHin.</span><span class="sxs-lookup"><span data-stu-id="b4dde-124">Event consumers that register for frequently occurring events use a grouping interval with the WITHIN clause.</span></span> <span data-ttu-id="b4dde-125">L'aggiunta di un gruppo all'interno della clausola WHERE in una query di evento comporta l'invio di un evento di aggregazione anziché di molti eventi da parte di WMI.</span><span class="sxs-lookup"><span data-stu-id="b4dde-125">Adding GROUP WITHIN to the WHERE clause in an event query results in WMI sending one aggregate event rather than many events.</span></span> <span data-ttu-id="b4dde-126">L'evento di aggregazione è rappresentato dalla classe di sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="b4dde-126">The aggregate event is represented by the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span>

<span data-ttu-id="b4dde-127">Per specificare un intervallo di raggruppamento, inserire la clausola all'interno immediatamente dopo la clausola GROUP.</span><span class="sxs-lookup"><span data-stu-id="b4dde-127">To specify a grouping interval, place the WITHIN clause immediately after the GROUP clause.</span></span>


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



<span data-ttu-id="b4dde-128">EventClass è la classe di evento di cui l'evento è membro, value è il valore della proprietà in cui il consumer richiede la notifica e Interval è l'intervallo di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="b4dde-128">EventClass is the event class of which the event is a member, value is the value for the property on which the consumer requires notification, and Interval is the grouping interval.</span></span>

<span data-ttu-id="b4dde-129">Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="b4dde-129">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="b4dde-130">I consumer di eventi permanenti possono essere creati con query di polling solo se si dispone di privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="b4dde-130">Permanent event consumers can be created with polling queries only if you have administrator privileges.</span></span>

 

 
