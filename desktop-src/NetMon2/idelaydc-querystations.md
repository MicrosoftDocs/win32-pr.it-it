---
description: Il metodo QueryStations fornisce un elenco di tutti i computer che attualmente utilizzano Network Monitor per acquisire i dati.
ms.assetid: 8e578f50-685e-4799-90ca-5da8810ec2a3
title: 'Metodo IDelaydC:: QueryStations (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5a45f5046dbd2e5714424baf42621e0c1d5539ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305884"
---
# <a name="idelaydcquerystations-method"></a><span data-ttu-id="caaa5-103">Metodo IDelaydC:: QueryStations</span><span class="sxs-lookup"><span data-stu-id="caaa5-103">IDelaydC::QueryStations method</span></span>

<span data-ttu-id="caaa5-104">Il metodo **QueryStations** fornisce un elenco di tutti i computer che attualmente utilizzano Network Monitor per acquisire i dati.</span><span class="sxs-lookup"><span data-stu-id="caaa5-104">The **QueryStations** method provides a list of all computers that are currently using Network Monitor to capture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="caaa5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="caaa5-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="caaa5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="caaa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caaa5-107">*lpQueryTable* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="caaa5-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="caaa5-108">Puntatore a una struttura [QUERYTABLE](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="caaa5-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="caaa5-109">In input questa struttura deve contenere il numero massimo di computer che si desidera vengano restituiti Network Monitor e una matrice di strutture [STATIONQUERY](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="caaa5-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="caaa5-110">Nell'output, questa struttura restituisce il numero di computer che acquisiscono i dati e una struttura [STATIONQUERY](stationquery.md) per ogni computer rilevato.</span><span class="sxs-lookup"><span data-stu-id="caaa5-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="caaa5-111">Si noti che questo elenco potrebbe includere computer che usano versioni di Network Monitor la versione data di 2,0.</span><span class="sxs-lookup"><span data-stu-id="caaa5-111">Note that this list might include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caaa5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="caaa5-112">Return value</span></span>

<span data-ttu-id="caaa5-113">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="caaa5-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="caaa5-114">Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="caaa5-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="caaa5-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="caaa5-115">Return code</span></span>                                                                                           | <span data-ttu-id="caaa5-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caaa5-116">Description</span></span>                                               |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="caaa5-117"><dt>**\_ \_ \_ memoria insufficiente NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="caaa5-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="caaa5-118">Memoria non disponibile per l'elaborazione della query.</span><span class="sxs-lookup"><span data-stu-id="caaa5-118">No memory was available to process this query.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="caaa5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="caaa5-119">Remarks</span></span>

<span data-ttu-id="caaa5-120">Questo metodo può essere chiamato in qualsiasi momento dopo la chiamata a [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="caaa5-120">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="caaa5-121">Una chiamata a questo metodo è una chiamata sincrona, che può richiedere alcuni secondi per il completamento come Network Monitor attende che i computer remoti rispondano alla query.</span><span class="sxs-lookup"><span data-stu-id="caaa5-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="caaa5-122">È possibile eseguire query solo sui computer della subnet locale.</span><span class="sxs-lookup"><span data-stu-id="caaa5-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="caaa5-123">È responsabilità dell'utente allocare la memoria per la struttura [QUERYTABLE](querytable.md) e liberarla dopo che la tabella non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="caaa5-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="caaa5-124">Questo requisito include la memoria necessaria per la matrice [STATIONQUERY](stationquery.md) usata in QUERYTABLE.</span><span class="sxs-lookup"><span data-stu-id="caaa5-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="caaa5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="caaa5-125">Requirements</span></span>



| <span data-ttu-id="caaa5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="caaa5-126">Requirement</span></span> | <span data-ttu-id="caaa5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="caaa5-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caaa5-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caaa5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="caaa5-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="caaa5-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="caaa5-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caaa5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="caaa5-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="caaa5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="caaa5-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="caaa5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="caaa5-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="caaa5-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="caaa5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="caaa5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caaa5-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caaa5-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caaa5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="caaa5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caaa5-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="caaa5-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="caaa5-138">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="caaa5-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="caaa5-139">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="caaa5-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




