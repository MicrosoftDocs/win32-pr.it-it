---
description: Il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente.
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'Metodo IDelaydC:: GetTotalStatistics (Netmon. h)'
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
ms.openlocfilehash: 0d194426933532fcf7a1965ed59b099489eefcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401604"
---
# <a name="idelaydcgettotalstatistics-method"></a><span data-ttu-id="9e8bd-103">Metodo IDelaydC:: GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="9e8bd-103">IDelaydC::GetTotalStatistics method</span></span>

<span data-ttu-id="9e8bd-104">Il metodo **GetTotalStatistics** recupera le [*statistiche totali*](t.md) per l' [*acquisizione*](c.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e8bd-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="9e8bd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e8bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e8bd-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9e8bd-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8bd-108">Puntatore a una struttura di [statistiche](statistics.md)che fornisce le statistiche totali per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="9e8bd-109">È responsabilità del chiamante allocare e liberare la memoria usata dalla struttura delle **statistiche** .</span><span class="sxs-lookup"><span data-stu-id="9e8bd-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="9e8bd-110">*fClearAfterReading* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e8bd-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8bd-111">Flag utilizzato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="9e8bd-112">Un'impostazione di **true** indica Network Monitor per cancellare l'archiviazione interna delle statistiche totali dopo che sono state recuperate le informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e8bd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e8bd-113">Return value</span></span>

<span data-ttu-id="9e8bd-114">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9e8bd-115">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e8bd-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="9e8bd-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9e8bd-116">Return code</span></span>                                                                                          | <span data-ttu-id="9e8bd-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e8bd-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e8bd-118"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="9e8bd-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9e8bd-119">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="9e8bd-120">Chiamare [IDelaydC:: Connect](idelaydc-connect.md) per connettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="9e8bd-121"><dt>**NMERR \_ non \_ ritardato**</dt></span><span class="sxs-lookup"><span data-stu-id="9e8bd-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="9e8bd-122">L'oggetto NPP è connesso alla rete, ma non con il metodo [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="9e8bd-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="9e8bd-123"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="9e8bd-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="9e8bd-124">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-124">The NPP is not capturing data.</span></span> <span data-ttu-id="9e8bd-125">Chiamare [IDelaydC:: Start](idelaydc-start.md) per avviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-125">Call [IDelaydC::Start](idelaydc-start.md) to start capturing data.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="9e8bd-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e8bd-126">Remarks</span></span>

<span data-ttu-id="9e8bd-127">Questo metodo restituisce i dati solo mentre è in corso un'acquisizione. Quando l'acquisizione viene sospesa, le chiamate a questo metodo non riusciranno.</span><span class="sxs-lookup"><span data-stu-id="9e8bd-127">This method returns data only while a capture is in progress; when the capture is paused, calls to this method will not succeed.</span></span>

<span data-ttu-id="9e8bd-128">Network Monitor archivia anche le [*statistiche di conversazione*](c.md), che possono essere recuperate chiamando il metodo [IDelaydC:: GetConversationStatistics](idelaydc-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="9e8bd-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8bd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e8bd-129">Requirements</span></span>



| <span data-ttu-id="9e8bd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e8bd-130">Requirement</span></span> | <span data-ttu-id="9e8bd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9e8bd-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8bd-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e8bd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9e8bd-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e8bd-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9e8bd-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e8bd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9e8bd-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e8bd-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9e8bd-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e8bd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e8bd-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e8bd-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9e8bd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9e8bd-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e8bd-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e8bd-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e8bd-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e8bd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8bd-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="9e8bd-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="9e8bd-142">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="9e8bd-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="9e8bd-143">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="9e8bd-143">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="9e8bd-144">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="9e8bd-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="9e8bd-145">Statistiche</span><span class="sxs-lookup"><span data-stu-id="9e8bd-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




