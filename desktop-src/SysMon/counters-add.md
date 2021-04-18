---
title: Metodo Counters. Add
description: Aggiunge un'istanza di CounterItem alla raccolta.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Aggiungere il metodo SysMon
- Add Method SysMon, classe Counters
- Classe contatori SysMon, Aggiungi metodo
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475827"
---
# <a name="countersadd-method"></a><span data-ttu-id="e3e36-106">Metodo Counters. Add</span><span class="sxs-lookup"><span data-stu-id="e3e36-106">Counters.Add method</span></span>

<span data-ttu-id="e3e36-107">Aggiunge un'istanza di [**CounterItem**](counteritem.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e3e36-107">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e36-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3e36-108">Syntax</span></span>


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a><span data-ttu-id="e3e36-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3e36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e36-110">*nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3e36-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e36-111">Percorso del contatore.</span><span class="sxs-lookup"><span data-stu-id="e3e36-111">Path to the counter.</span></span> <span data-ttu-id="e3e36-112">Il percorso può includere un nome di computer e deve includere il nome di un oggetto prestazione, il nome di un'istanza dell'oggetto se l'oggetto prestazione specificato supporta più istanze e il nome di un contatore.</span><span class="sxs-lookup"><span data-stu-id="e3e36-112">The path can include a machine name, and must include a performance object name, an object instance name if the specified performance object supports multiple instances, and a counter name.</span></span> <span data-ttu-id="e3e36-113">Questa specifica del percorso non distingue tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e3e36-113">This path specification is not case-sensitive.</span></span>

<span data-ttu-id="e3e36-114">Per informazioni dettagliate su come specificare un percorso del contatore, vedere [specifica di un percorso del contatore](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span><span class="sxs-lookup"><span data-stu-id="e3e36-114">For details on specifying a counter path, see [Specifying a Counter Path](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span></span>

</dd> </dl>

## <a name="exceptions"></a><span data-ttu-id="e3e36-115">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="e3e36-115">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3e36-116">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="e3e36-116">Exception type</span></span></th>
<th><span data-ttu-id="e3e36-117">Condizione</span><span class="sxs-lookup"><span data-stu-id="e3e36-117">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3e36-118"><strong>System. Runtime. InteropServices. COMException</strong></span><span class="sxs-lookup"><span data-stu-id="e3e36-118"><strong>System.Runtime.InteropServices.COMException</strong></span></span></td>
<td><span data-ttu-id="e3e36-119">È possibile ricevere questa eccezione per uno dei motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3e36-119">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="e3e36-120">L'oggetto prestazione specificato non è stato trovato nel computer.</span><span class="sxs-lookup"><span data-stu-id="e3e36-120">The specified performance object was not found on the computer.</span></span> <span data-ttu-id="e3e36-121">Il valore ERR. Number è 0xC0000BB8.</span><span class="sxs-lookup"><span data-stu-id="e3e36-121">The Err.Number value is 0xC0000BB8.</span></span></li>
<li><span data-ttu-id="e3e36-122">Impossibile trovare il contatore specificato.</span><span class="sxs-lookup"><span data-stu-id="e3e36-122">The specified counter could not be found.</span></span> <span data-ttu-id="e3e36-123">Il valore ERR. Number è 0xC0000BB9.</span><span class="sxs-lookup"><span data-stu-id="e3e36-123">The Err.Number value is 0xC0000BB9.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="e3e36-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3e36-124">Remarks</span></span>

<span data-ttu-id="e3e36-125">Se si specifica un contatore con caratteri jolly nel parametro *pathname* , il metodo **Add** crea un oggetto [**CounterItem**](counteritem.md) per ogni percorso espanso.</span><span class="sxs-lookup"><span data-stu-id="e3e36-125">If you specify a wildcard counter in the *pathname* parameter, the **Add** method creates one [**CounterItem**](counteritem.md) object for each expanded path.</span></span> <span data-ttu-id="e3e36-126">Il metodo **Add** restituisce quindi un puntatore al primo **CounterItem** aggiunto.</span><span class="sxs-lookup"><span data-stu-id="e3e36-126">The **Add** method then returns a pointer to the first added **CounterItem**.</span></span>

<span data-ttu-id="e3e36-127">Se il carattere jolly genera un contatore duplicato, l'errore non viene segnalato e non viene creato alcun duplicato.</span><span class="sxs-lookup"><span data-stu-id="e3e36-127">If the wildcard would result in a duplicate counter, the error is not reported and no duplicate is created.</span></span> <span data-ttu-id="e3e36-128">Se si verifica una condizione di errore prima della creazione di tutti i contatori, viene restituito l'errore e non vengono creati i restanti contatori.</span><span class="sxs-lookup"><span data-stu-id="e3e36-128">If an error condition occurs before all counters are created, the error is reported and the remaining counters are not created.</span></span>

<span data-ttu-id="e3e36-129">Non esiste alcun limite al numero di contatori che è possibile aggiungere; Tuttavia, SYSMON creerà solo i primi 1.024 contatori della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e3e36-129">There is no limit to the number of counters that you can add; however, SYSMON will graph only the first 1,024 counters in the collection.</span></span> <span data-ttu-id="e3e36-130">Non esiste alcun limite al numero di contatori che SYSMON visualizzerà in un report.</span><span class="sxs-lookup"><span data-stu-id="e3e36-130">There is no limit on the number of counters that SYSMON will display in a report.</span></span>

<span data-ttu-id="e3e36-131">Per ricevere una notifica quando viene aggiunto un contatore, implementare l'evento [OnCounterAdded](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="e3e36-131">To receive notification when a counter is added, implement the [OnCounterAdded](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3e36-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3e36-132">Requirements</span></span>



| <span data-ttu-id="e3e36-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3e36-133">Requirement</span></span> | <span data-ttu-id="e3e36-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e3e36-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e36-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3e36-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e3e36-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e3e36-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e3e36-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3e36-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e3e36-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e3e36-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3e36-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e3e36-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3e36-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e3e36-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3e36-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3e36-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e36-142">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="e3e36-142">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="e3e36-143">**Contatori**</span><span class="sxs-lookup"><span data-stu-id="e3e36-143">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="e3e36-144">**SystemMonitor. BrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="e3e36-144">**SystemMonitor.BrowseCounters**</span></span>](systemmonitor-browsecounters.md)
</dt> </dl>

 

