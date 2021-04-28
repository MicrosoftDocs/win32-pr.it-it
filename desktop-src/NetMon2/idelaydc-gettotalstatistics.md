---
description: "Metodo IDelaydC::GetTotalStatistics: il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente."
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: Metodo IDelaydC::GetTotalStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b3a0ce4f230236e276fede528a5e778ecafd51fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113529"
---
# <a name="idelaydcgettotalstatistics-method"></a><span data-ttu-id="237a3-103">Metodo IDelaydC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="237a3-103">IDelaydC::GetTotalStatistics method</span></span>

<span data-ttu-id="237a3-104">Il **metodo GetTotalStatistics** recupera le [*statistiche totali per*](t.md) l'acquisizione [*corrente.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="237a3-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="237a3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="237a3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="237a3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="237a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="237a3-107">*lpStats* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="237a3-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="237a3-108">Puntatore a una [struttura STATISTICS](statistics.md)che fornisce le statistiche totali per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="237a3-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="237a3-109">È responsabilità del chiamante allocare e liberare la memoria usata dalla **struttura STATISTICS.**</span><span class="sxs-lookup"><span data-stu-id="237a3-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="237a3-110">*fClearAfterReading* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="237a3-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="237a3-111">Flag usato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali.</span><span class="sxs-lookup"><span data-stu-id="237a3-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="237a3-112">L'impostazione **TRUE** indica Network Monitor cancellare lo spazio di archiviazione interno delle statistiche totali dopo il recupero delle informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="237a3-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="237a3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="237a3-113">Return value</span></span>

<span data-ttu-id="237a3-114">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="237a3-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="237a3-115">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="237a3-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="237a3-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="237a3-116">Return code</span></span>                                                                                          | <span data-ttu-id="237a3-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="237a3-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="237a3-118"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="237a3-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="237a3-119">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="237a3-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="237a3-120">Chiamare [IDelaydC::Connect](idelaydc-connect.md) per connettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="237a3-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="237a3-121"><dt>**NMERR \_ NON \_ RITARDATO**</dt></span><span class="sxs-lookup"><span data-stu-id="237a3-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="237a3-122">Il NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="237a3-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="237a3-123"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="237a3-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="237a3-124">Il NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="237a3-124">The NPP is not capturing data.</span></span> <span data-ttu-id="237a3-125">Chiamare [IDelaydC::Start](idelaydc-start.md) per avviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="237a3-125">Call [IDelaydC::Start](idelaydc-start.md) to start capturing data.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="237a3-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="237a3-126">Remarks</span></span>

<span data-ttu-id="237a3-127">Questo metodo restituisce i dati solo mentre è in corso un'acquisizione. Quando l'acquisizione viene sospesa, le chiamate a questo metodo non avranno esito positivo.</span><span class="sxs-lookup"><span data-stu-id="237a3-127">This method returns data only while a capture is in progress; when the capture is paused, calls to this method will not succeed.</span></span>

<span data-ttu-id="237a3-128">Network Monitor anche le [*statistiche*](c.md)della conversazione, che possono essere recuperate chiamando il metodo [IDelaydC::GetConversationStatistics.](idelaydc-getconversationstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="237a3-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="237a3-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="237a3-129">Requirements</span></span>



| <span data-ttu-id="237a3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="237a3-130">Requirement</span></span> | <span data-ttu-id="237a3-131">Valore</span><span class="sxs-lookup"><span data-stu-id="237a3-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="237a3-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="237a3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="237a3-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="237a3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="237a3-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="237a3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="237a3-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="237a3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="237a3-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="237a3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="237a3-137"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="237a3-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="237a3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="237a3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="237a3-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="237a3-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="237a3-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="237a3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="237a3-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="237a3-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="237a3-142">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="237a3-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="237a3-143">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="237a3-143">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="237a3-144">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="237a3-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="237a3-145">Statistiche</span><span class="sxs-lookup"><span data-stu-id="237a3-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




