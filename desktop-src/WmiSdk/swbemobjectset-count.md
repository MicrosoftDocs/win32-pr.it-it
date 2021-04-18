---
description: Usare la proprietà Count dell'oggetto SWbemObjectSet per determinare il numero di elementi presenti in una raccolta SWbemObjectSet. Questa proprietà è di sola lettura.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Proprietà SWbemObjectSet. Count (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318508"
---
# <a name="swbemobjectsetcount-property"></a><span data-ttu-id="9103f-104">Proprietà SWbemObjectSet. Count</span><span class="sxs-lookup"><span data-stu-id="9103f-104">SWbemObjectSet.Count property</span></span>

<span data-ttu-id="9103f-105">Usare la proprietà **count** dell'oggetto [**SWbemObjectSet**](swbemobjectset.md) per determinare il numero di elementi presenti in una raccolta **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="9103f-105">Use the **Count** property of the [**SWbemObjectSet**](swbemobjectset.md) object to determine how many items are in an **SWbemObjectSet** collection.</span></span> <span data-ttu-id="9103f-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9103f-106">This property is read-only.</span></span>

<span data-ttu-id="9103f-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9103f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="9103f-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9103f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9103f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9103f-109">Syntax</span></span>


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a><span data-ttu-id="9103f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9103f-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="9103f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9103f-111">Remarks</span></span>

<span data-ttu-id="9103f-112">Una cosa da fare quando si usa count è che WMI non mantiene un conteggio parziale del numero di elementi in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="9103f-112">One thing to be careful of when using Count is that WMI does not keep a running tally of the number of items in a collection.</span></span> <span data-ttu-id="9103f-113">Se si richiede il conteggio per una raccolta, WMI non può rispondere immediatamente con un numero; al contrario, deve contare letteralmente gli elementi, enumerando l'intero insieme.</span><span class="sxs-lookup"><span data-stu-id="9103f-113">If you request Count for a collection, WMI cannot instantly respond with a number; instead, it must literally count the items, enumerating the entire collection.</span></span> <span data-ttu-id="9103f-114">Per una raccolta con un numero relativamente basso di elementi, ad esempio servizi, questa enumerazione richiede probabilmente meno di un secondo.</span><span class="sxs-lookup"><span data-stu-id="9103f-114">For a collection that has relatively few items, such as services, this enumeration likely takes less than a second.</span></span> <span data-ttu-id="9103f-115">Il conteggio del numero di eventi in una raccolta di log eventi, tuttavia, può richiedere molto più tempo.</span><span class="sxs-lookup"><span data-stu-id="9103f-115">Counting the number of events in an event log collection, however, can take considerably longer.</span></span>

<span data-ttu-id="9103f-116">Si supponga quindi di voler visualizzare i valori delle proprietà per ogni evento nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="9103f-116">And then suppose you want to display the property values for every event in the collection.</span></span> <span data-ttu-id="9103f-117">In tal caso, WMI dovrà enumerare l'intera raccolta una seconda volta.</span><span class="sxs-lookup"><span data-stu-id="9103f-117">If so, WMI will have to enumerate the entire collection a second time.</span></span>

> [!Note]  
> <span data-ttu-id="9103f-118">Se si tenta di ottenere questa proprietà da un oggetto [**SWbemObjectSet**](swbemobjectset.md) restituito da un metodo in cui i flag specificati sono inclusi il flag wbemFlagForwardOnly, verrà visualizzato un errore wbemErrFailed.</span><span class="sxs-lookup"><span data-stu-id="9103f-118">If you attempt to get this property from an [**SWbemObjectSet**](swbemobjectset.md) object that is returned from a method where the specified flags are included the wbemFlagForwardOnly flag, you will get an wbemErrFailed error.</span></span>

 

## <a name="examples"></a><span data-ttu-id="9103f-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="9103f-119">Examples</span></span>

<span data-ttu-id="9103f-120">Nella maggior parte dei casi, l'unica cosa che si può fare con un SWbemObjectSet è enumerare tutti gli oggetti contenuti nella raccolta stessa.</span><span class="sxs-lookup"><span data-stu-id="9103f-120">For the most part, the only thing you will ever do with an SWbemObjectSet is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="9103f-121">Il conteggio dei conteggi, tuttavia, può essere utile nell'esecuzione di script per l'amministrazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="9103f-121">However, the Count Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="9103f-122">Come suggerisce il nome, Count indica il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="9103f-122">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="9103f-123">Questo script, ad esempio, recupera una raccolta di tutti i servizi installati in un computer e quindi restituisce il numero totale di servizi trovati:</span><span class="sxs-lookup"><span data-stu-id="9103f-123">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



<span data-ttu-id="9103f-124">Ciò che rende utile count è la possibilità di indicare se un'istanza specifica è disponibile in un computer.</span><span class="sxs-lookup"><span data-stu-id="9103f-124">What makes Count useful is that it can tell you whether a specific instance is available on a computer.</span></span> <span data-ttu-id="9103f-125">Questo script, ad esempio, recupera una raccolta di tutti i servizi in un computer con il nome W3SVC.</span><span class="sxs-lookup"><span data-stu-id="9103f-125">For example, this script retrieves a collection of all the services on a computer that have the Name W3SVC.</span></span> <span data-ttu-id="9103f-126">Se il conteggio è 0 (ed è valido per le raccolte senza istanze), significa che il servizio W3SVC non è installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="9103f-126">If the Count is 0 (and it is valid for collections to have no instances), that means the W3SVC service is not installed on the computer.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a><span data-ttu-id="9103f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9103f-127">Requirements</span></span>



| <span data-ttu-id="9103f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9103f-128">Requirement</span></span> | <span data-ttu-id="9103f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="9103f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9103f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9103f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9103f-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9103f-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9103f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9103f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9103f-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9103f-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9103f-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9103f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9103f-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9103f-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9103f-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9103f-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="9103f-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9103f-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9103f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9103f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9103f-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9103f-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9103f-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="9103f-140">CLSID</span></span><br/>                    | <span data-ttu-id="9103f-141">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="9103f-141">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="9103f-142">IID</span><span class="sxs-lookup"><span data-stu-id="9103f-142">IID</span></span><br/>                      | <span data-ttu-id="9103f-143">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="9103f-143">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




