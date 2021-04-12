---
description: Le enumerazioni tendono a usare una quantità significativa di risorse di sistema.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Miglioramento delle prestazioni di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232627"
---
# <a name="improving-enumeration-performance"></a><span data-ttu-id="61e02-103">Miglioramento delle prestazioni di enumerazione</span><span class="sxs-lookup"><span data-stu-id="61e02-103">Improving Enumeration Performance</span></span>

<span data-ttu-id="61e02-104">Le enumerazioni tendono a usare una quantità significativa di risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="61e02-104">Enumerations tend to use a significant amount of system resources.</span></span> <span data-ttu-id="61e02-105">Pertanto, è consigliabile tentare di ottimizzare il processo di enumerazione WMI se si prevede di eseguire enumerazioni in un gruppo di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="61e02-105">Therefore, you should try to optimize the WMI enumeration process if you plan on performing enumerations on a large group.</span></span> <span data-ttu-id="61e02-106">Gli script possono inoltre utilizzare una query per evitare un calo delle prestazioni nelle operazioni "for each... Next" con un set di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="61e02-106">Scripts can also use a query to avoid performance degradation in "For each….Next" operations with a large set.</span></span> <span data-ttu-id="61e02-107">Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="61e02-107">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="61e02-108">Nella procedura seguente viene descritto come migliorare le prestazioni di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="61e02-108">The following procedure describes how to improve enumeration performance.</span></span>

<span data-ttu-id="61e02-109">**Per migliorare le prestazioni di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="61e02-109">**To improve enumeration performance**</span></span>

1.  <span data-ttu-id="61e02-110">Impostare il parametro *è* per consentire a semisincrono di restituire i dati con un enumeratore che ignora ogni elemento da WMI mentre viene recapitato.</span><span class="sxs-lookup"><span data-stu-id="61e02-110">Set the *lFlags* parameter to allow semisynchronous return of the data with an enumerator that discards each item from WMI as it is delivered.</span></span> <span data-ttu-id="61e02-111">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="61e02-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="61e02-112">Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare i flag **WBEM \_ \_ return \_ immediate** e **WBEM \_ flag di \_ \_ sola trasmissione** .</span><span class="sxs-lookup"><span data-stu-id="61e02-112">The following C++ code example shows how to use the **WBEM\_FLAG\_RETURN\_IMMEDIATE** and **WBEM\_FLAG\_FORWARD\_ONLY** flags.</span></span>

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    <span data-ttu-id="61e02-113">In VBScript o Visual Basic usare i flag di scripting **WbemFlagReturnImmediately** e **WbemFlagForwardOnly** di [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="61e02-113">In VBScript or Visual Basic, use the scripting flags **WbemFlagReturnImmediately** and **WbemFlagForwardOnly** from [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span> <span data-ttu-id="61e02-114">Il valore combinato di questi flag è decimale 48.</span><span class="sxs-lookup"><span data-stu-id="61e02-114">The combined value of these flags is decimal 48.</span></span>

    <span data-ttu-id="61e02-115">I flag di scripting e di parametro generano il comportamento seguente:</span><span class="sxs-lookup"><span data-stu-id="61e02-115">The scripting and parameter flags cause the following behavior:</span></span>

    -   <span data-ttu-id="61e02-116">Il **\_ flag WBEM \_ restituisce \_** il flag **wbemFlagReturnImmediately** o immediate per la richiesta del comportamento semisincrono.</span><span class="sxs-lookup"><span data-stu-id="61e02-116">The **WBEM\_FLAG\_RETURN\_IMMEDIATE** or **wbemFlagReturnImmediately** flag requests semisynchronous behavior.</span></span> <span data-ttu-id="61e02-117">La chiamata per creare l'enumeratore restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="61e02-117">The call to create the enumerator returns immediately.</span></span> <span data-ttu-id="61e02-118">È quindi possibile iniziare a attraversare il set di oggetti che si riceve.</span><span class="sxs-lookup"><span data-stu-id="61e02-118">You can then begin to traverse the object set that you receive.</span></span>
    -   <span data-ttu-id="61e02-119">Il flag WBEM con flag di **\_ \_ \_ sola trasmissione** o flag **wbemFlagForwardOnly** richiede un enumeratore che non è possibile riavvolgere.</span><span class="sxs-lookup"><span data-stu-id="61e02-119">The **WBEM\_FLAG\_FORWARD\_ONLY** flag or **wbemFlagForwardOnly** flag requests an enumerator that you cannot rewind.</span></span> <span data-ttu-id="61e02-120">Ovvero WMI può rilasciare un oggetto dopo la visualizzazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61e02-120">That is, WMI can release an object after you view the object.</span></span>

    <span data-ttu-id="61e02-121">Nelle situazioni in cui l'enumerazione è di grandi dimensioni e l'applicazione è molto veloce, l'uso di enumeratori di sola trasmissione con l'elaborazione semisincrono consente a WMI di mantenere un numero molto inferiore di oggetti, aumentando in modo significativo il tempo di risposta e le prestazioni di memoria.</span><span class="sxs-lookup"><span data-stu-id="61e02-121">In situations where the enumeration is large and the application is very fast, using forward-only enumerators with semisynchronous processing allows WMI to hold on to far fewer objects, thereby increasing response time and memory performance significantly.</span></span>

    <span data-ttu-id="61e02-122">Nell'esempio di codice VBScript riportato di seguito viene illustrato come effettuare una chiamata utilizzando i flag **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** combinati per ottenere una raccolta di eventi da un log eventi.</span><span class="sxs-lookup"><span data-stu-id="61e02-122">The following VBScript code example shows how to make a call using the combined **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** flags to obtain a collection of events from an event log.</span></span>

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  <span data-ttu-id="61e02-123">Quando possibile, evitare di utilizzare [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) in C++ o [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)e utilizzare invece **ExecQuery**.</span><span class="sxs-lookup"><span data-stu-id="61e02-123">Whenever possible, avoid using [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) in C++ or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), and instead use **ExecQuery**.</span></span>

    <span data-ttu-id="61e02-124">Il metodo **ExecQuery** esegue una query su WMI utilizzando le tecnologie di database, mentre [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) o [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) enumera gli oggetti WMI.</span><span class="sxs-lookup"><span data-stu-id="61e02-124">The **ExecQuery** method queries WMI using database technologies, while [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) enumerates WMI objects.</span></span> <span data-ttu-id="61e02-125">In particolare, **ExecQuery** può richiedere subset specifici di dati che i metodi di enumerazione non possono.</span><span class="sxs-lookup"><span data-stu-id="61e02-125">Specifically, **ExecQuery** can request specific subsets of data that the enumerating methods cannot.</span></span>

    <span data-ttu-id="61e02-126">Poiché alcuni provider non dispongono di funzionalità di query, WMI fornisce una funzionalità di post-filtro che consente a WMI di annullare le istanze che non soddisfano le specifiche di una query.</span><span class="sxs-lookup"><span data-stu-id="61e02-126">Because some providers do not have querying capabilities, WMI provides a "post filter" feature that allows WMI to discard instances that do not fulfill a query's specifications.</span></span> <span data-ttu-id="61e02-127">Il fatto che un particolare provider sfrutti questa funzionalità spetta all'autore del provider.</span><span class="sxs-lookup"><span data-stu-id="61e02-127">Whether a particular provider takes advantage of this feature is up to the provider author.</span></span>

3.  <span data-ttu-id="61e02-128">Provare con diverse query per determinare ciò che offre le prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="61e02-128">Experiment with different queries to determine what gives you the best performance.</span></span>

    <span data-ttu-id="61e02-129">WMI, ad esempio, elabora raramente in modo efficiente le query con clausole **where** nel formato Prop1 < "x".</span><span class="sxs-lookup"><span data-stu-id="61e02-129">For example, WMI seldom efficiently processes queries with **WHERE** clauses of the form Prop1 < "x".</span></span> <span data-ttu-id="61e02-130">Al contrario, WMI elabora in genere le query nel formato KeyProp1 = "x" in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="61e02-130">In contrast, WMI normally processes queries of the form KeyProp1 = "x" efficiently.</span></span>

<span data-ttu-id="61e02-131">Per ulteriori informazioni, vedere [enumerazione di WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="61e02-131">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

 

 



