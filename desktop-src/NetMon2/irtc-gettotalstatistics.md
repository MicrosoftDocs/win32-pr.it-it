---
description: Il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente.
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'Metodo IRTC:: GetTotalStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 27128048b4326aae14ae6a2e2e6c0540b1105538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310506"
---
# <a name="irtcgettotalstatistics-method"></a><span data-ttu-id="2d388-103">Metodo IRTC:: GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="2d388-103">IRTC::GetTotalStatistics method</span></span>

<span data-ttu-id="2d388-104">Il metodo **GetTotalStatistics** recupera le [*statistiche totali*](t.md) per l' [*acquisizione*](c.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="2d388-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d388-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d388-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="2d388-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d388-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d388-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2d388-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d388-108">Puntatore a una struttura di [statistiche](statistics.md) che fornisce le statistiche totali per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2d388-108">Pointer to a [STATISTICS](statistics.md) structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="2d388-109">È responsabilità dei chiamanti allocare e liberare la memoria utilizzata dalla struttura delle **statistiche** .</span><span class="sxs-lookup"><span data-stu-id="2d388-109">It is the callers responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="2d388-110">*fClearAfterReading* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d388-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d388-111">Flag utilizzato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali.</span><span class="sxs-lookup"><span data-stu-id="2d388-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="2d388-112">Un'impostazione di **true** indica Network Monitor per cancellare l'archiviazione interna delle statistiche totali dopo che sono state recuperate le informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="2d388-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d388-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d388-113">Return value</span></span>

<span data-ttu-id="2d388-114">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2d388-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2d388-115">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d388-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2d388-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2d388-116">Return code</span></span>                                                                                          | <span data-ttu-id="2d388-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d388-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d388-118"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="2d388-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2d388-119">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="2d388-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="2d388-120">Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="2d388-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="2d388-121"><dt>**NMERR \_ non in \_ tempo reale**</dt></span><span class="sxs-lookup"><span data-stu-id="2d388-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="2d388-122">L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="2d388-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |
| <dl> <span data-ttu-id="2d388-123"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="2d388-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="2d388-124">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="2d388-124">The NPP is not capturing data.</span></span> <span data-ttu-id="2d388-125">Chiamare [IRTC:: Start](irtc-start.md) per avviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="2d388-125">Call [IRTC::Start](irtc-start.md) to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="2d388-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d388-126">Remarks</span></span>

<span data-ttu-id="2d388-127">Questo metodo restituisce i dati solo mentre è in corso un'acquisizione, incluso mentre l'acquisizione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="2d388-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="2d388-128">Network Monitor archivia anche le [*statistiche di conversazione*](c.md).</span><span class="sxs-lookup"><span data-stu-id="2d388-128">Network Monitor also stores [*conversation statistics*](c.md).</span></span> <span data-ttu-id="2d388-129">Per recuperare le statistiche di conversazione, chiamare il metodo [IRTC:: GetConversationStatistics](irtc-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="2d388-129">To retrieve conversation statistics, call the [IRTC::GetConversationStatistics](irtc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d388-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d388-130">Requirements</span></span>



| <span data-ttu-id="2d388-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d388-131">Requirement</span></span> | <span data-ttu-id="2d388-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2d388-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d388-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d388-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2d388-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d388-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2d388-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d388-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2d388-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d388-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2d388-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d388-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d388-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d388-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2d388-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2d388-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d388-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d388-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d388-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d388-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d388-142">IRTC</span><span class="sxs-lookup"><span data-stu-id="2d388-142">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="2d388-143">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="2d388-143">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="2d388-144">IRTC:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="2d388-144">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="2d388-145">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="2d388-145">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="2d388-146">Statistiche</span><span class="sxs-lookup"><span data-stu-id="2d388-146">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




