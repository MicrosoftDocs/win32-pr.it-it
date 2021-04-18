---
description: Il WMI Query Language (WQL) è un subset di standard American National Standards Institute Structured Query Language (ANSI SQL) con modifiche semantiche secondarie per il supporto di WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Esecuzione di query con WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309924"
---
# <a name="querying-with-wql"></a><span data-ttu-id="2bbde-103">Esecuzione di query con WQL</span><span class="sxs-lookup"><span data-stu-id="2bbde-103">Querying with WQL</span></span>

<span data-ttu-id="2bbde-104">Il WMI Query Language (WQL) è un subset di standard American National Standards Institute Structured Query Language (ANSI SQL) con modifiche semantiche secondarie per il supporto di WMI.</span><span class="sxs-lookup"><span data-stu-id="2bbde-104">The WMI Query Language (WQL) is a subset of standard American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes to support WMI.</span></span>

<span data-ttu-id="2bbde-105">Per un elenco completo delle parole chiave WQL supportate, vedere [WQL (SQL per WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2bbde-105">For a complete list of supported WQL keywords, see [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span> <span data-ttu-id="2bbde-106">L'utilizzo di parole chiave SQL per i nomi di oggetti o proprietà può impedire l'analisi di una query.</span><span class="sxs-lookup"><span data-stu-id="2bbde-106">Using SQL keywords for object or property names may restrict a query from being parsed.</span></span> <span data-ttu-id="2bbde-107">Le seguenti parole chiave SQL sono limitate: **null**, **true** e **false**.</span><span class="sxs-lookup"><span data-stu-id="2bbde-107">The following SQL keywords are restricted: **NULL**, **TRUE**, and **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="2bbde-108">Esistono limiti al numero di parole chiave AND e OR che possono essere utilizzate nelle query WQL.</span><span class="sxs-lookup"><span data-stu-id="2bbde-108">There are limits to the number of AND and OR keywords that can be used in WQL queries.</span></span> <span data-ttu-id="2bbde-109">Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione del codice di errore di **\_ \_ \_ violazione della quota E di WBEM** come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2bbde-109">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="2bbde-110">Il limite di parole chiave WQL dipende dalla complessità della query.</span><span class="sxs-lookup"><span data-stu-id="2bbde-110">The limit of WQL keywords depends on how complex the query is.</span></span>

 

<span data-ttu-id="2bbde-111">Le query possono utilizzare la clausola **where** per l'estensione e la personalizzazione, sebbene non sia obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="2bbde-111">Queries can use the **WHERE** clause for extension and customization, although it is not required.</span></span> <span data-ttu-id="2bbde-112">La clausola **where** è costituita da una proprietà o una parola chiave, da un operatore e da una costante.</span><span class="sxs-lookup"><span data-stu-id="2bbde-112">The **WHERE** clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="2bbde-113">Tutte le clausole **where** devono specificare uno degli operatori predefiniti inclusi in WQL.</span><span class="sxs-lookup"><span data-stu-id="2bbde-113">All **WHERE** clauses must specify one of the predefined operators that are included in WQL.</span></span> <span data-ttu-id="2bbde-114">Per ulteriori informazioni sulla sintassi, vedere [clausola WHERE](where-clause.md).</span><span class="sxs-lookup"><span data-stu-id="2bbde-114">For more information about syntax, see [WHERE Clause](where-clause.md).</span></span> <span data-ttu-id="2bbde-115">Per ulteriori informazioni sugli operatori WQL validi, vedere [operatori WQL](wql-operators.md).</span><span class="sxs-lookup"><span data-stu-id="2bbde-115">For more information about valid WQL operators, see [WQL Operators](wql-operators.md).</span></span>

<span data-ttu-id="2bbde-116">Come per le altre stringhe di query SQL, è possibile usare caratteri di escape per le query.</span><span class="sxs-lookup"><span data-stu-id="2bbde-116">As with other SQL query strings, you can escape your queries.</span></span>

> [!Note]  
> <span data-ttu-id="2bbde-117">WQL non supporta le query o le associazioni tra gli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="2bbde-117">WQL does not support cross-namespace queries or associations.</span></span> <span data-ttu-id="2bbde-118">Non è possibile eseguire una query per tutte le istanze di una classe specificata che risiede in tutti gli spazi dei nomi nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2bbde-118">You cannot query for all instances of a specified class residing in all of the namespaces on the target computer.</span></span>

 

<span data-ttu-id="2bbde-119">WQL supporta i tipi di query seguenti:</span><span class="sxs-lookup"><span data-stu-id="2bbde-119">WQL supports the following types of queries:</span></span>

-   <span data-ttu-id="2bbde-120">Query di dati</span><span class="sxs-lookup"><span data-stu-id="2bbde-120">Data queries</span></span>

    <span data-ttu-id="2bbde-121">Le query sui dati vengono utilizzate per recuperare le istanze di classe e le associazioni dati.</span><span class="sxs-lookup"><span data-stu-id="2bbde-121">Data queries are used to retrieve class instances and data associations.</span></span> <span data-ttu-id="2bbde-122">Si tratta del tipo di query usato più di frequente in applicazioni e script WMI.</span><span class="sxs-lookup"><span data-stu-id="2bbde-122">They are the most commonly used type of query in WMI scripts and applications.</span></span> <span data-ttu-id="2bbde-123">Per ulteriori informazioni sulla sintassi delle query di dati, vedere [richiesta di dati dell'istanza di classe](requesting-class-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="2bbde-123">For more information about the syntax of data queries, see [Requesting Class Instance Data](requesting-class-instance-data.md).</span></span> <span data-ttu-id="2bbde-124">Per ulteriori informazioni sulle associazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="2bbde-124">For more information about associations, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="2bbde-125">WQL non supporta query di tipi di oggetto di tipo matrice.</span><span class="sxs-lookup"><span data-stu-id="2bbde-125">WQL does not support queries of array datatypes.</span></span>

     

    <span data-ttu-id="2bbde-126">Nell'esempio di query dei dati seguente viene richiesto il file di registro eventi denominato "Application" da tutte le istanze di [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="2bbde-126">The following data query example requests the event log file named "Application" from all instances of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   <span data-ttu-id="2bbde-127">Query di eventi</span><span class="sxs-lookup"><span data-stu-id="2bbde-127">Event queries</span></span>

    <span data-ttu-id="2bbde-128">I consumer usano le query di eventi per eseguire la registrazione per ricevere la notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="2bbde-128">Consumers use event queries to register to receive notification of events.</span></span> <span data-ttu-id="2bbde-129">I provider di eventi utilizzano le query di eventi per eseguire la registrazione per supportare uno o più eventi.</span><span class="sxs-lookup"><span data-stu-id="2bbde-129">Event providers use event queries to register to support one or more events.</span></span> <span data-ttu-id="2bbde-130">Per ulteriori informazioni sulle query di eventi, vedere [ricezione di notifiche degli eventi](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="2bbde-130">For more information about event queries, see [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

    <span data-ttu-id="2bbde-131">La query di eventi di esempio seguente da parte di un consumer di eventi temporanei richiede una notifica quando viene creata una nuova istanza di una classe derivata da [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) .</span><span class="sxs-lookup"><span data-stu-id="2bbde-131">The following example event query by a temporary event consumer requests notification when a new instance of a class derived from [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) is created.</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   <span data-ttu-id="2bbde-132">Query dello schema</span><span class="sxs-lookup"><span data-stu-id="2bbde-132">Schema queries</span></span>

    <span data-ttu-id="2bbde-133">Le query di schema vengono utilizzate per recuperare le definizioni delle classi, anziché le istanze di classe, e le associazioni di schema.</span><span class="sxs-lookup"><span data-stu-id="2bbde-133">Schema queries are used to retrieve class definitions (rather than class instances) and schema associations.</span></span> <span data-ttu-id="2bbde-134">I provider di classi utilizzano query dello schema per specificare le classi supportate durante la registrazione.</span><span class="sxs-lookup"><span data-stu-id="2bbde-134">Class providers use schema queries to specify the classes that they support when they register.</span></span> <span data-ttu-id="2bbde-135">Per ulteriori informazioni sulle query dello schema, vedere [recupero di definizioni di classe](retrieving-class-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="2bbde-135">For more information about schema queries, see [Retrieving Class Definitions](retrieving-class-definitions.md).</span></span>

    <span data-ttu-id="2bbde-136">Nella query dello schema di esempio seguente viene illustrata la sintassi speciale.</span><span class="sxs-lookup"><span data-stu-id="2bbde-136">The following example schema query shows the special syntax.</span></span>

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="2bbde-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bbde-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bbde-138">Formato data e ora WMI</span><span class="sxs-lookup"><span data-stu-id="2bbde-138">WMI Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 
