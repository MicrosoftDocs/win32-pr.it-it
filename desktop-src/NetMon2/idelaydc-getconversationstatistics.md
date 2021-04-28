---
description: "Metodo IDelaydC::GetConversationStatistics: il metodo GetConversationStatistics recupera le informazioni sulla sessione e sulla stazione relative all'acquisizione corrente."
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: Metodo IDelaydC::GetConversationStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d4d4c1bb1ad7ecb45b640c16322e297f9f640ef1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103809"
---
# <a name="idelaydcgetconversationstatistics-method"></a><span data-ttu-id="4c5e6-103">Metodo IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="4c5e6-103">IDelaydC::GetConversationStatistics method</span></span>

<span data-ttu-id="4c5e6-104">Il **metodo GetConversationStatistics** recupera le [*informazioni sulla*](s.md) sessione e sulla [*stazione*](s.md) relative all'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5e6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c5e6-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="4c5e6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c5e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c5e6-107">*nSessions* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4c5e6-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5e6-108">Puntatore a un valore DWORD che contiene il [*numero*](s.md) di sessioni registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="4c5e6-109">*lpSessionStats* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4c5e6-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5e6-110">Puntatore a [una struttura SESSIONSTATS.](sessionstats.md)</span><span class="sxs-lookup"><span data-stu-id="4c5e6-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4c5e6-111">*nStations* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4c5e6-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5e6-112">Puntatore a un valore DWORD che contiene il numero di [*stazioni*](s.md) registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="4c5e6-113">*lpStationStats* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4c5e6-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5e6-114">Puntatore a [una struttura STATIONSTATS.](stationstats.md)</span><span class="sxs-lookup"><span data-stu-id="4c5e6-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4c5e6-115">*fClearAfterReading* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4c5e6-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5e6-116">Flag usato per indicare Network Monitor cancellare l'archiviazione interna delle strutture [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) dopo il recupero delle informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c5e6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c5e6-117">Return value</span></span>

<span data-ttu-id="4c5e6-118">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4c5e6-119">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c5e6-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="4c5e6-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4c5e6-120">Return code</span></span>                                                                                                   | <span data-ttu-id="4c5e6-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c5e6-121">Description</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c5e6-122"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="4c5e6-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="4c5e6-123">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="4c5e6-124">Chiamare [IDelaydC::Connect](idelaydc-connect.md) per connettere il NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-124">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="4c5e6-125"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="4c5e6-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="4c5e6-126">NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-126">The NPP is not capturing data.</span></span> <span data-ttu-id="4c5e6-127">Chiamare [IDelaydC::Start](idelaydc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-127">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="4c5e6-128"><dt>**NMERR \_ NON \_ IN RITARDO**</dt></span><span class="sxs-lookup"><span data-stu-id="4c5e6-128"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>            | <span data-ttu-id="4c5e6-129">NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="4c5e6-129">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="4c5e6-130"><dt>**NO \_ CONVERSATION \_ \_ STATS DI NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="4c5e6-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="4c5e6-131">La configurazione per questa connessione è impostata in modo da non salvare le statistiche della conversazione.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="4c5e6-132">Per salvare le statistiche della conversazione, arrestare l'acquisizione, impostare NoConversationStats = YES nel BLOB di configurazione e quindi riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4c5e6-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c5e6-133">Remarks</span></span>

<span data-ttu-id="4c5e6-134">Questo metodo può essere chiamato solo mentre è in corso Data Capture. Quando l'acquisizione corrente viene sospesa, le chiamate a questo metodo non avranno esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4c5e6-134">This method can only be called only while data capture is in progress; when the current capture is paused, calls to this method will not succeed.</span></span> <span data-ttu-id="4c5e6-135">Per avviare un'acquisizione, chiamare il [metodo IDelaydC::Start.](idelaydc-start.md)</span><span class="sxs-lookup"><span data-stu-id="4c5e6-135">To start a capture, call the [IDelaydC::Start](idelaydc-start.md) method.</span></span>

<span data-ttu-id="4c5e6-136">Per recuperare altri tipi di statistiche, chiamare [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="4c5e6-136">To retrieve other types of statistics, call [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c5e6-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c5e6-137">Requirements</span></span>



| <span data-ttu-id="4c5e6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c5e6-138">Requirement</span></span> | <span data-ttu-id="4c5e6-139">Valore</span><span class="sxs-lookup"><span data-stu-id="4c5e6-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5e6-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c5e6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4c5e6-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4c5e6-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4c5e6-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c5e6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4c5e6-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4c5e6-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4c5e6-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c5e6-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c5e6-145"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="4c5e6-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4c5e6-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4c5e6-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c5e6-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c5e6-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c5e6-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c5e6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5e6-149">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="4c5e6-149">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="4c5e6-150">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="4c5e6-150">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="4c5e6-151">IDelaydC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="4c5e6-151">IDelaydC::GetTotalStatistics</span></span>](idelaydc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="4c5e6-152">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="4c5e6-152">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="4c5e6-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="4c5e6-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="4c5e6-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="4c5e6-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




