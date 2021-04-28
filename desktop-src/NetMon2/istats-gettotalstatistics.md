---
description: "Metodo IStats::GetTotalStatistics: il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente."
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: Metodo IStats::GetTotalStatistics (Netmon.h)
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
ms.openlocfilehash: e6566a58212e8f20d0d999302f41ab97cb9f005e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098409"
---
# <a name="istatsgettotalstatistics-method"></a><span data-ttu-id="26f09-103">Metodo IStats::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="26f09-103">IStats::GetTotalStatistics method</span></span>

<span data-ttu-id="26f09-104">Il **metodo GetTotalStatistics** recupera le [*statistiche totali*](t.md) per l'acquisizione [*corrente.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="26f09-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="26f09-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26f09-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="26f09-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26f09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f09-107">*lpStats* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="26f09-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26f09-108">Puntatore a una [struttura STATISTICS](statistics.md)che fornisce le statistiche totali per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="26f09-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="26f09-109">È responsabilità del chiamante allocare e liberare la memoria usata dalla **struttura STATISTICS.**</span><span class="sxs-lookup"><span data-stu-id="26f09-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="26f09-110">*fClearAfterReading* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="26f09-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26f09-111">Flag usato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali.</span><span class="sxs-lookup"><span data-stu-id="26f09-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="26f09-112">L'impostazione TRUE indica Network Monitor l'archiviazione interna delle statistiche totali dopo il recupero delle informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="26f09-112">A setting of TRUE tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f09-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26f09-113">Return value</span></span>

<span data-ttu-id="26f09-114">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="26f09-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="26f09-115">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="26f09-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="26f09-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="26f09-116">Return code</span></span>                                                                                            | <span data-ttu-id="26f09-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26f09-117">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26f09-118"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="26f09-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="26f09-119">NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="26f09-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="26f09-120">Chiamare il [metodo IStats::Connect](istats-connect.md) per connettere NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="26f09-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="26f09-121"><dt>**NMERR \_ NON \_ STATS \_ ONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="26f09-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="26f09-122">NPP è connesso alla rete, ma non con il [metodo IStats::Connect.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="26f09-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |
| <dl> <span data-ttu-id="26f09-123"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="26f09-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="26f09-124">NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="26f09-124">The NPP is not capturing data.</span></span> <span data-ttu-id="26f09-125">Chiamare il [metodo IStats::Start](istats-start.md) per avviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="26f09-125">Call the [IStats::Start](istats-start.md) method to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="26f09-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="26f09-126">Remarks</span></span>

<span data-ttu-id="26f09-127">Questo metodo restituisce i dati solo mentre è in corso un'acquisizione, incluso mentre l'acquisizione è sospesa.</span><span class="sxs-lookup"><span data-stu-id="26f09-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="26f09-128">Network Monitor anche le [*statistiche*](c.md)della conversazione, che possono essere recuperate chiamando il [metodo IStats::GetConversationStatistics.](istats-getconversationstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="26f09-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IStats::GetConversationStatistics](istats-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f09-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26f09-129">Requirements</span></span>



| <span data-ttu-id="26f09-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f09-130">Requirement</span></span> | <span data-ttu-id="26f09-131">Valore</span><span class="sxs-lookup"><span data-stu-id="26f09-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f09-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26f09-132">Minimum supported client</span></span><br/> | <span data-ttu-id="26f09-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26f09-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="26f09-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26f09-134">Minimum supported server</span></span><br/> | <span data-ttu-id="26f09-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26f09-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="26f09-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26f09-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f09-137"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="26f09-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="26f09-138">DLL</span><span class="sxs-lookup"><span data-stu-id="26f09-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26f09-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26f09-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f09-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26f09-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f09-141">IStat</span><span class="sxs-lookup"><span data-stu-id="26f09-141">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="26f09-142">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="26f09-142">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="26f09-143">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="26f09-143">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="26f09-144">IStats::Start,</span><span class="sxs-lookup"><span data-stu-id="26f09-144">IStats::Start,</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="26f09-145">Statistiche</span><span class="sxs-lookup"><span data-stu-id="26f09-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




