---
description: Il metodo QueryStations fornisce un elenco di tutti i computer che attualmente utilizzano Network Monitor per acquisire i dati di rete.
ms.assetid: 5ad99810-e463-4477-a542-cf4dfa6967a4
title: 'Metodo IESP:: QueryStations (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5287f472b2a0641eb29e4f1b37b6fe4e089dfa86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305874"
---
# <a name="iespquerystations-method"></a><span data-ttu-id="5cf18-103">Metodo IESP:: QueryStations</span><span class="sxs-lookup"><span data-stu-id="5cf18-103">IESP::QueryStations method</span></span>

<span data-ttu-id="5cf18-104">Il metodo **QueryStations** fornisce un elenco di tutti i computer che attualmente utilizzano Network Monitor per acquisire i dati di rete.</span><span class="sxs-lookup"><span data-stu-id="5cf18-104">The **QueryStations** method provides a list of all computers that currently use Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf18-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cf18-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="5cf18-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cf18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cf18-107">*lpQueryTable* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5cf18-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cf18-108">Puntatore a una struttura [QUERYTABLE](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf18-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="5cf18-109">In input questa struttura deve contenere il numero massimo di computer che si desidera vengano restituiti Network Monitor e una matrice di strutture [STATIONQUERY](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf18-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="5cf18-110">Nell'output, questa struttura restituisce il numero di computer che acquisiscono i dati e una struttura [STATIONQUERY](stationquery.md) per ogni computer rilevato.</span><span class="sxs-lookup"><span data-stu-id="5cf18-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="5cf18-111">Si noti che il totale può includere computer che usano versioni di Network Monitor la versione precedenti 2,0.</span><span class="sxs-lookup"><span data-stu-id="5cf18-111">Note that this total may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cf18-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cf18-112">Return value</span></span>

<span data-ttu-id="5cf18-113">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5cf18-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5cf18-114">Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="5cf18-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="5cf18-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5cf18-115">Return code</span></span>                                                                                           | <span data-ttu-id="5cf18-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cf18-116">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="5cf18-117"><dt>**\_ \_ \_ memoria insufficiente NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="5cf18-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="5cf18-118">La memoria necessaria per elaborare la query non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="5cf18-118">The memory needed to process this query was unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5cf18-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cf18-119">Remarks</span></span>

<span data-ttu-id="5cf18-120">Questo metodo può essere chiamato in qualsiasi momento dopo la chiamata del metodo [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf18-120">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="5cf18-121">Una chiamata a questo metodo è una chiamata sincrona, che può richiedere alcuni secondi per il completamento come Network Monitor attende che i computer remoti rispondano alla query.</span><span class="sxs-lookup"><span data-stu-id="5cf18-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="5cf18-122">È possibile eseguire query solo sui computer della subnet locale.</span><span class="sxs-lookup"><span data-stu-id="5cf18-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="5cf18-123">È responsabilità dell'utente allocare la memoria per la struttura [QUERYTABLE](querytable.md) e liberarla dopo che la tabella non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="5cf18-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="5cf18-124">Questo requisito include la memoria necessaria per la matrice [STATIONQUERY](stationquery.md) usata in QUERYTABLE.</span><span class="sxs-lookup"><span data-stu-id="5cf18-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf18-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cf18-125">Requirements</span></span>



| <span data-ttu-id="5cf18-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cf18-126">Requirement</span></span> | <span data-ttu-id="5cf18-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5cf18-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf18-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cf18-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf18-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5cf18-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5cf18-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cf18-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf18-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5cf18-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5cf18-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cf18-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cf18-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cf18-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5cf18-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5cf18-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cf18-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cf18-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cf18-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cf18-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf18-137">IESP</span><span class="sxs-lookup"><span data-stu-id="5cf18-137">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="5cf18-138">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="5cf18-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="5cf18-139">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="5cf18-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




