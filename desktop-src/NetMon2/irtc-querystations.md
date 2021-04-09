---
description: Fornisce un elenco di tutti i computer che utilizzano attualmente Network Monitor per acquisire i dati di rete.
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: 'Metodo IRTC:: QueryStations (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a0cebd789284dd41c293424a70686f30eb4601d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967137"
---
# <a name="irtcquerystations-method"></a><span data-ttu-id="4b784-103">Metodo IRTC:: QueryStations</span><span class="sxs-lookup"><span data-stu-id="4b784-103">IRTC::QueryStations method</span></span>

<span data-ttu-id="4b784-104">Il metodo **QueryStations** fornisce un elenco di tutti i computer che utilizzano attualmente Network Monitor per acquisire i dati di rete.</span><span class="sxs-lookup"><span data-stu-id="4b784-104">The **QueryStations** method provides a list of all computers currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b784-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b784-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="4b784-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b784-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b784-107">*lpQueryTable* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4b784-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b784-108">Puntatore a una struttura [**QUERYTABLE**](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="4b784-108">A pointer to a [**QUERYTABLE**](querytable.md) structure.</span></span> <span data-ttu-id="4b784-109">In input questa struttura deve contenere il numero massimo di computer che si desidera vengano restituiti Network Monitor e una matrice di strutture [**STATIONQUERY**](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="4b784-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [**STATIONQUERY**](stationquery.md) structures.</span></span>

<span data-ttu-id="4b784-110">Nell'output questa struttura restituisce il numero di computer che acquisiscono i dati e una struttura [**STATIONQUERY**](stationquery.md) per ogni computer trovato.</span><span class="sxs-lookup"><span data-stu-id="4b784-110">On output, this structure returns the number of computers capturing data and a [**STATIONQUERY**](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="4b784-111">Tenere presente che potrebbero essere inclusi computer che usano versioni di Network Monitor la versione preesistente 2,0.</span><span class="sxs-lookup"><span data-stu-id="4b784-111">Be aware that this may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b784-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b784-112">Return value</span></span>

<span data-ttu-id="4b784-113">Se il metodo ha esito positivo, il valore restituito è **NMERR \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="4b784-113">If the method is successful, the return value is **NMERR\_SUCCESS**.</span></span>

<span data-ttu-id="4b784-114">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b784-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="4b784-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4b784-115">Return code</span></span>                                                                                           | <span data-ttu-id="4b784-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b784-116">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b784-117"><dt>**\_ \_ \_ memoria insufficiente NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="4b784-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="4b784-118">La memoria necessaria per elaborare la query non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="4b784-118">The memory required to process this query is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b784-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b784-119">Remarks</span></span>

<span data-ttu-id="4b784-120">Questo metodo può essere chiamato in qualsiasi momento dopo la chiamata del metodo [**CreateNPPInterface**](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="4b784-120">This method can be called at any time after the [**CreateNPPInterface**](createnppinterface.md) method is called.</span></span> <span data-ttu-id="4b784-121">Una chiamata a questo metodo è una chiamata sincrona, che può richiedere alcuni secondi per il completamento mentre Network Monitor attende che i computer remoti rispondano alla query.</span><span class="sxs-lookup"><span data-stu-id="4b784-121">A call to this method is a synchronous call, which may take several seconds to complete while Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="4b784-122">È possibile eseguire query solo sui computer della subnet locale.</span><span class="sxs-lookup"><span data-stu-id="4b784-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="4b784-123">L'utente deve allocare la memoria per la struttura [**QUERYTABLE**](querytable.md) e liberare tale memoria dopo che la tabella non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="4b784-123">The user must allocate the memory for the [**QUERYTABLE**](querytable.md) structure and free that memory after the table is no longer required.</span></span> <span data-ttu-id="4b784-124">Questo requisito include la memoria necessaria per la matrice [**STATIONQUERY**](stationquery.md) usata in **QUERYTABLE**.</span><span class="sxs-lookup"><span data-stu-id="4b784-124">This requirement includes memory needed for the [**STATIONQUERY**](stationquery.md) array used in **QUERYTABLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b784-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b784-125">Requirements</span></span>



| <span data-ttu-id="4b784-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b784-126">Requirement</span></span> | <span data-ttu-id="4b784-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4b784-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b784-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b784-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4b784-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b784-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4b784-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b784-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4b784-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b784-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4b784-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b784-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b784-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b784-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4b784-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4b784-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b784-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b784-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b784-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b784-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b784-137">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="4b784-137">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="4b784-138">**QUERYTABLE**</span><span class="sxs-lookup"><span data-stu-id="4b784-138">**QUERYTABLE**</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="4b784-139">**STATIONQUERY**</span><span class="sxs-lookup"><span data-stu-id="4b784-139">**STATIONQUERY**</span></span>](stationquery.md)
</dt> </dl>

 

 




