---
description: Il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente.
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'Metodo IStats:: GetTotalStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 51cdbfdcc796aa7d8091e8da5837809efaa63379
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315458"
---
# <a name="istatsgettotalstatistics-method"></a><span data-ttu-id="d3a85-103">IStats:: GetTotalStatistics (metodo)</span><span class="sxs-lookup"><span data-stu-id="d3a85-103">IStats::GetTotalStatistics method</span></span>

<span data-ttu-id="d3a85-104">Il metodo **GetTotalStatistics** recupera le [*statistiche totali*](t.md) per l' [*acquisizione*](c.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="d3a85-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a85-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3a85-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="d3a85-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3a85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3a85-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3a85-108">Puntatore a una struttura di [statistiche](statistics.md)che fornisce le statistiche totali per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d3a85-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="d3a85-109">È responsabilità del chiamante allocare e liberare la memoria usata dalla struttura delle **statistiche** .</span><span class="sxs-lookup"><span data-stu-id="d3a85-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d3a85-110">*fClearAfterReading* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3a85-111">Flag utilizzato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali.</span><span class="sxs-lookup"><span data-stu-id="d3a85-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="d3a85-112">Un'impostazione di TRUE indica Network Monitor per cancellare l'archiviazione interna delle statistiche totali dopo che sono state recuperate le informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="d3a85-112">A setting of TRUE tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3a85-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3a85-113">Return value</span></span>

<span data-ttu-id="d3a85-114">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d3a85-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d3a85-115">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="d3a85-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d3a85-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d3a85-116">Return code</span></span>                                                                                            | <span data-ttu-id="d3a85-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3a85-117">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3a85-118"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="d3a85-119">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="d3a85-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="d3a85-120">Chiamare il metodo [IStats:: Connect](istats-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="d3a85-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="d3a85-121"><dt>**NMERR \_ non \_ \_ solo statistiche**</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="d3a85-122">L'oggetto NPP è connesso alla rete, ma non con il metodo [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="d3a85-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |
| <dl> <span data-ttu-id="d3a85-123"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="d3a85-124">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="d3a85-124">The NPP is not capturing data.</span></span> <span data-ttu-id="d3a85-125">Chiamare il metodo [IStats:: Start](istats-start.md) per avviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="d3a85-125">Call the [IStats::Start](istats-start.md) method to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="d3a85-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3a85-126">Remarks</span></span>

<span data-ttu-id="d3a85-127">Questo metodo restituisce i dati solo mentre è in corso un'acquisizione, incluso mentre l'acquisizione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="d3a85-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="d3a85-128">Network Monitor archivia anche le [*statistiche di conversazione*](c.md), che possono essere recuperate chiamando il metodo [IStats:: GetConversationStatistics](istats-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="d3a85-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IStats::GetConversationStatistics](istats-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a85-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3a85-129">Requirements</span></span>



| <span data-ttu-id="d3a85-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3a85-130">Requirement</span></span> | <span data-ttu-id="d3a85-131">Valore</span><span class="sxs-lookup"><span data-stu-id="d3a85-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a85-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3a85-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a85-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d3a85-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3a85-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a85-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d3a85-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3a85-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3a85-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d3a85-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d3a85-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3a85-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3a85-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3a85-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a85-141">IStats</span><span class="sxs-lookup"><span data-stu-id="d3a85-141">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="d3a85-142">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="d3a85-142">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="d3a85-143">IStats:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="d3a85-143">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="d3a85-144">IStats:: Start,</span><span class="sxs-lookup"><span data-stu-id="d3a85-144">IStats::Start,</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="d3a85-145">Statistiche</span><span class="sxs-lookup"><span data-stu-id="d3a85-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




