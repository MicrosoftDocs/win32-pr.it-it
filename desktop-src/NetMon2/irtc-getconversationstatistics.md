---
description: "Metodo IRTC::GetConversationStatistics: il metodo GetConversationStatistics recupera le informazioni di sessione e stazione sull'acquisizione corrente."
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: Metodo IRTC::GetConversationStatistics (Netmon.h)
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
ms.openlocfilehash: 4d2476f4eb33d7e74d0de8363fa88d5e688a2e73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110699"
---
# <a name="irtcgetconversationstatistics-method"></a><span data-ttu-id="5a3a4-103">Metodo IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="5a3a4-103">IRTC::GetConversationStatistics method</span></span>

<span data-ttu-id="5a3a4-104">Il **metodo GetConversationStatistics** recupera le [*informazioni di*](s.md) sessione e [*stazione*](s.md) sull'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3a4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a3a4-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="5a3a4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a3a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3a4-107">*nSessioni* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="5a3a4-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3a4-108">Puntatore a un valore DWORD che contiene il numero [*di*](s.md) sessioni registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="5a3a4-109">*lpSessionStats* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="5a3a4-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3a4-110">Puntatore a [una struttura SESSIONSTATS.](sessionstats.md)</span><span class="sxs-lookup"><span data-stu-id="5a3a4-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a3a4-111">*nStations* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="5a3a4-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3a4-112">Puntatore a un valore DWORD che contiene il numero di [*stazioni*](s.md) registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="5a3a4-113">*lpStationStats* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="5a3a4-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3a4-114">Puntatore a [una struttura STATIONSTATS.](stationstats.md)</span><span class="sxs-lookup"><span data-stu-id="5a3a4-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a3a4-115">*fClearAfterReading* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5a3a4-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3a4-116">Flag usato per indicare Network Monitor l'archiviazione interna delle strutture [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) dopo il recupero delle informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3a4-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a3a4-117">Return value</span></span>

<span data-ttu-id="5a3a4-118">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5a3a4-119">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a3a4-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5a3a4-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a3a4-120">Return code</span></span>                                                                                                   | <span data-ttu-id="5a3a4-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a3a4-121">Description</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a3a4-122"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="5a3a4-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="5a3a4-123">NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="5a3a4-124">Chiamare [IRTC::Connect](irtc-connect.md) per connettere NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-124">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="5a3a4-125"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="5a3a4-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="5a3a4-126">Il NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-126">The NPP is not capturing data.</span></span> <span data-ttu-id="5a3a4-127">Chiamare [IRTC::Start](irtc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-127">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="5a3a4-128"><dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt></span><span class="sxs-lookup"><span data-stu-id="5a3a4-128"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>           | <span data-ttu-id="5a3a4-129">Il protocollo NPP è connesso alla rete, ma non con [il metodo IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="5a3a4-129">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                                                                                                          |
| <dl> <span data-ttu-id="5a3a4-130"><dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt></span><span class="sxs-lookup"><span data-stu-id="5a3a4-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="5a3a4-131">La configurazione per questa connessione è impostata in modo da non salvare le statistiche della conversazione.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="5a3a4-132">Per salvare le statistiche della conversazione, arrestare l'acquisizione, impostare NoConversationStats = YES nel BLOB di configurazione, quindi riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a3a4-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a3a4-133">Remarks</span></span>

<span data-ttu-id="5a3a4-134">Questo metodo può essere chiamato solo durante l'acquisizione dei dati. Se si chiama questo metodo mentre l'acquisizione corrente è sospesa, il metodo non avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5a3a4-134">This method can only be called while you are capturing data; if you call this method while the current capture is paused, the method will not succeed.</span></span> <span data-ttu-id="5a3a4-135">Per avviare un'acquisizione, chiamare [il metodo IRTC::Start.](irtc-start.md)</span><span class="sxs-lookup"><span data-stu-id="5a3a4-135">To start a capture, call the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="5a3a4-136">Per recuperare altri tipi di statistiche, chiamare [il metodo IRTC::GetTotalStatistics.](irtc-gettotalstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="5a3a4-136">To retrieve other types of statistics, call the [IRTC::GetTotalStatistics](irtc-gettotalstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3a4-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a3a4-137">Requirements</span></span>



| <span data-ttu-id="5a3a4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a3a4-138">Requirement</span></span> | <span data-ttu-id="5a3a4-139">Valore</span><span class="sxs-lookup"><span data-stu-id="5a3a4-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3a4-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a3a4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3a4-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5a3a4-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5a3a4-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a3a4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3a4-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5a3a4-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5a3a4-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a3a4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3a4-145"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3a4-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5a3a4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5a3a4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a3a4-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a3a4-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3a4-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a3a4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3a4-149">IRTC</span><span class="sxs-lookup"><span data-stu-id="5a3a4-149">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="5a3a4-150">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="5a3a4-150">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="5a3a4-151">IRTC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="5a3a4-151">IRTC::GetTotalStatistics</span></span>](irtc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="5a3a4-152">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="5a3a4-152">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="5a3a4-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="5a3a4-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="5a3a4-154">STATISTICHE DI STAZIONE</span><span class="sxs-lookup"><span data-stu-id="5a3a4-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




