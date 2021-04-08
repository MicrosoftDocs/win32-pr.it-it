---
description: Il metodo GetConversationStatistics recupera le informazioni sulla sessione e sulla stazione relative all'acquisizione corrente.
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'Metodo IRTC:: GetConversationStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 758488cb3c3f65922bbf6aac4f39774a5430fc92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880714"
---
# <a name="irtcgetconversationstatistics-method"></a><span data-ttu-id="4428f-103">Metodo IRTC:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="4428f-103">IRTC::GetConversationStatistics method</span></span>

<span data-ttu-id="4428f-104">Il metodo **GetConversationStatistics** recupera le informazioni sulla [*sessione*](s.md) e sulla [*stazione*](s.md) relative all'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4428f-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="4428f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4428f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="4428f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4428f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4428f-107">*nSessions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4428f-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4428f-108">Puntatore a un valore DWORD che contiene il numero di [*sessioni*](s.md) registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4428f-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="4428f-109">*lpSessionStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4428f-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4428f-110">Puntatore a una struttura [SESSIONSTATS](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="4428f-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4428f-111">*nStations* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4428f-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4428f-112">Puntatore a un valore DWORD che contiene il numero di [*stazioni*](s.md) registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4428f-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="4428f-113">*lpStationStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4428f-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4428f-114">Puntatore a una struttura [STATIONSTATS](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="4428f-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4428f-115">*fClearAfterReading* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4428f-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4428f-116">Flag usato per indicare Network Monitor per cancellare l'archiviazione interna delle strutture [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) dopo aver recuperato le informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="4428f-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4428f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4428f-117">Return value</span></span>

<span data-ttu-id="4428f-118">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4428f-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4428f-119">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="4428f-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="4428f-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4428f-120">Return code</span></span>                                                                                                   | <span data-ttu-id="4428f-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4428f-121">Description</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4428f-122"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="4428f-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="4428f-123">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="4428f-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="4428f-124">Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="4428f-124">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="4428f-125"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="4428f-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="4428f-126">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="4428f-126">The NPP is not capturing data.</span></span> <span data-ttu-id="4428f-127">Chiamare [IRTC:: Start](irtc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4428f-127">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="4428f-128"><dt>**NMERR \_ non in \_ tempo reale**</dt></span><span class="sxs-lookup"><span data-stu-id="4428f-128"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>           | <span data-ttu-id="4428f-129">L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="4428f-129">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                                                                                                          |
| <dl> <span data-ttu-id="4428f-130"><dt>**NMERR \_ Nessuna \_ statistica di conversazione \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4428f-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="4428f-131">La configurazione per questa connessione è impostata in modo da non salvare le statistiche di conversazione.</span><span class="sxs-lookup"><span data-stu-id="4428f-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="4428f-132">Per salvare le statistiche delle conversazioni, arrestare l'acquisizione, impostare NoConversationStats = YES nel BLOB di configurazione, quindi riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4428f-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4428f-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="4428f-133">Remarks</span></span>

<span data-ttu-id="4428f-134">Questo metodo può essere chiamato solo durante l'acquisizione dei dati; Se si chiama questo metodo mentre l'acquisizione corrente viene sospesa, il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4428f-134">This method can only be called while you are capturing data; if you call this method while the current capture is paused, the method will not succeed.</span></span> <span data-ttu-id="4428f-135">Per avviare un'acquisizione, chiamare il metodo [IRTC:: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="4428f-135">To start a capture, call the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="4428f-136">Per recuperare altri tipi di statistiche, chiamare il metodo [IRTC:: GetTotalStatistics](irtc-gettotalstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="4428f-136">To retrieve other types of statistics, call the [IRTC::GetTotalStatistics](irtc-gettotalstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4428f-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4428f-137">Requirements</span></span>



| <span data-ttu-id="4428f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="4428f-138">Requirement</span></span> | <span data-ttu-id="4428f-139">Valore</span><span class="sxs-lookup"><span data-stu-id="4428f-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4428f-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4428f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4428f-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4428f-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4428f-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4428f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4428f-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4428f-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4428f-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4428f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4428f-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4428f-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4428f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4428f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4428f-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4428f-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4428f-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4428f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4428f-149">IRTC</span><span class="sxs-lookup"><span data-stu-id="4428f-149">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="4428f-150">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="4428f-150">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="4428f-151">IRTC:: GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="4428f-151">IRTC::GetTotalStatistics</span></span>](irtc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="4428f-152">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="4428f-152">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="4428f-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="4428f-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="4428f-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="4428f-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




