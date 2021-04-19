---
description: Uno degli strumenti principali di Strumentazione gestione Windows (WMI) è la possibilità di eseguire query sul repository WMI per informazioni sulle classi e sulle istanze.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Esecuzione di query su WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309921"
---
# <a name="querying-wmi"></a><span data-ttu-id="70a1e-103">Esecuzione di query su WMI</span><span class="sxs-lookup"><span data-stu-id="70a1e-103">Querying WMI</span></span>

<span data-ttu-id="70a1e-104">Uno degli strumenti principali di Strumentazione gestione Windows (WMI) è la possibilità di eseguire query sul repository WMI per informazioni sulle classi e sulle istanze.</span><span class="sxs-lookup"><span data-stu-id="70a1e-104">One of the main tools of Windows Management Instrumentation (WMI) is the ability to query the WMI repository for class and instance information.</span></span> <span data-ttu-id="70a1e-105">È ad esempio possibile richiedere che WMI restituisca tutti gli oggetti che rappresentano gli eventi di chiusura dal sistema desktop.</span><span class="sxs-lookup"><span data-stu-id="70a1e-105">For example, you can request that WMI return all the objects representing shut-down events from your desktop system.</span></span> <span data-ttu-id="70a1e-106">È inoltre possibile recuperare i dati della classe, dell'istanza o dello schema.</span><span class="sxs-lookup"><span data-stu-id="70a1e-106">You can also retrieve class, instance, or schema data.</span></span> <span data-ttu-id="70a1e-107">Nella tabella seguente sono elencati i diversi tipi di query che è possibile eseguire.</span><span class="sxs-lookup"><span data-stu-id="70a1e-107">The following table lists the different types of queries you can make.</span></span>



| <span data-ttu-id="70a1e-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="70a1e-108">Topic</span></span>                                                                | <span data-ttu-id="70a1e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70a1e-109">Description</span></span>                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70a1e-110">Richiamo di una query sincrona</span><span class="sxs-lookup"><span data-stu-id="70a1e-110">Invoking a Synchronous Query</span></span>](invoking-a-synchronous-query.md)     | <span data-ttu-id="70a1e-111">Viene descritto come gestire un collegamento con WMI durante il processo di query.</span><span class="sxs-lookup"><span data-stu-id="70a1e-111">Describes how to maintain a link with WMI throughout the query process.</span></span> <span data-ttu-id="70a1e-112">Le query sincrone sono valide per query o query di piccole dimensioni in un sistema locale.</span><span class="sxs-lookup"><span data-stu-id="70a1e-112">Synchronous queries are good for small queries or queries to a local system.</span></span><br/>                                  |
| [<span data-ttu-id="70a1e-113">Richiamo di una query asincrona</span><span class="sxs-lookup"><span data-stu-id="70a1e-113">Invoking an Asynchronous Query</span></span>](invoking-an-asynchronous-query.md) | <span data-ttu-id="70a1e-114">Viene descritto come configurare un processo separato per la ricezione di query.</span><span class="sxs-lookup"><span data-stu-id="70a1e-114">Describes how to set up a separate process to receive queries.</span></span> <span data-ttu-id="70a1e-115">Le query asincrone sono più complesse e forniscono un livello di sicurezza inferiore, ma in genere migliorano le prestazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="70a1e-115">Asynchronous queries are more complex and provide a lower level of security, but generally improve system performance.</span></span><br/> |



 

<span data-ttu-id="70a1e-116">Oltre a eseguire query sul repository WMI, è inoltre possibile utilizzare il [*WMI Query Language (WQL)*](gloss-w.md) per indirizzare gli eventi di notifica all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="70a1e-116">In addition to querying the WMI repository, you can also use the [*WMI Query Language (WQL)*](gloss-w.md) to route notification events to your application.</span></span> <span data-ttu-id="70a1e-117">Per ulteriori informazioni, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="70a1e-117">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

> [!Note]
>
> <span data-ttu-id="70a1e-118">Per eseguire correttamente una query su WMI, è necessario avere una conoscenza corretta di WQL.</span><span class="sxs-lookup"><span data-stu-id="70a1e-118">To properly query WMI, you must have a good understanding of WQL.</span></span> <span data-ttu-id="70a1e-119">Una query non corretta, troppo complessa o inappropriata può causare la restituzione di un errore o di risultati imprevisti da parte di query processor.</span><span class="sxs-lookup"><span data-stu-id="70a1e-119">A query that is incorrect, too complex, or inappropriate can cause the query processor to return an error or unexpected results.</span></span> <span data-ttu-id="70a1e-120">Per una guida completa a WQL, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="70a1e-120">For a comprehensive guide to WQL, see [Querying with WQL](querying-with-wql.md).</span></span>
>
> <span data-ttu-id="70a1e-121">Esistono limiti al numero di parole chiave **and** e **or** che possono essere utilizzate nelle query WQL.</span><span class="sxs-lookup"><span data-stu-id="70a1e-121">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="70a1e-122">Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione del codice di errore di **\_ \_ \_ violazione della quota E di WBEM** come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70a1e-122">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="70a1e-123">Il limite di parole chiave WQL dipende dalla complessità della query.</span><span class="sxs-lookup"><span data-stu-id="70a1e-123">The limit of WQL keywords depends on how complex the query is.</span></span>
>
> <span data-ttu-id="70a1e-124">Quando si esegue una query per i valori delle proprietà con un tipo di dati **UInt64** o **sint64** in un linguaggio di scripting come VBScript, WMI restituisce i valori stringa.</span><span class="sxs-lookup"><span data-stu-id="70a1e-124">When querying for property values with a **uint64** or **sint64** data type in a scripting language like VBScript, WMI returns string values.</span></span> <span data-ttu-id="70a1e-125">Quando si confrontano questi valori, possono verificarsi risultati imprevisti, perché il confronto di stringhe restituisce risultati diversi rispetto al confronto dei numeri.</span><span class="sxs-lookup"><span data-stu-id="70a1e-125">Unexpected results can occur when comparing these values, because comparing strings returns different results than comparing numbers.</span></span> <span data-ttu-id="70a1e-126">Ad esempio, "10 miliardi" è minore di "9" durante il confronto di stringhe e 9 è minore di 10 miliardi durante il confronto dei numeri.</span><span class="sxs-lookup"><span data-stu-id="70a1e-126">For example, "10000000000" is less than "9" when comparing strings, and 9 is less than 10000000000 when comparing numbers.</span></span> <span data-ttu-id="70a1e-127">Per evitare confusione, è consigliabile usare il metodo [CDbl](/previous-versions//ftekwwt0(v=vs.85)) in VBScript quando le proprietà di tipo **UInt64** o **SINT64** vengono recuperate da WMI.</span><span class="sxs-lookup"><span data-stu-id="70a1e-127">To avoid confusion you should use the [CDbl](/previous-versions//ftekwwt0(v=vs.85)) method in VBScript when properties of type **uint64** or **sint64** are retrieved from WMI.</span></span>

 

> [!Note]  

 

<span data-ttu-id="70a1e-128">Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="70a1e-128">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

