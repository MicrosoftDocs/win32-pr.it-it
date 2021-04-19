---
description: Recupera le informazioni sulla sessione e sulla stazione relative all'acquisizione corrente.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'Metodo IStats:: GetConversationStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319941"
---
# <a name="istatsgetconversationstatistics-method"></a><span data-ttu-id="0fbde-103">IStats:: GetConversationStatistics (metodo)</span><span class="sxs-lookup"><span data-stu-id="0fbde-103">IStats::GetConversationStatistics method</span></span>

<span data-ttu-id="0fbde-104">Il metodo **GetConversationStatistics** recupera le informazioni sulla sessione e sulla stazione relative all'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="0fbde-104">The **GetConversationStatistics** method retrieves session and station information about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fbde-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fbde-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="0fbde-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fbde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fbde-107">*nSessions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0fbde-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbde-108">Puntatore a un valore DWORD che contiene il numero di [*sessioni*](s.md) registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="0fbde-108">A pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="0fbde-109">*lpSessionStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0fbde-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbde-110">Puntatore a una struttura [**SESSIONSTATS**](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="0fbde-110">A pointer to a [**SESSIONSTATS**](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0fbde-111">*nStations* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0fbde-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbde-112">Puntatore a un valore DWORD che contiene il numero di [*stazioni*](s.md) registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="0fbde-112">A pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="0fbde-113">*lpStationStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0fbde-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbde-114">Puntatore a una struttura [**STATIONSTATS**](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="0fbde-114">A pointer to a [**STATIONSTATS**](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0fbde-115">*fClearAfterReading* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fbde-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbde-116">Flag utilizzato per indicare Network Monitor per cancellare l'archiviazione interna delle strutture [**SESSIONSTATS**](sessionstats.md) e [**STATIONSTATS**](stationstats.md) dopo il recupero dei dati correnti.</span><span class="sxs-lookup"><span data-stu-id="0fbde-116">Flag used to instruct Network Monitor to clear the internal storage of the [**SESSIONSTATS**](sessionstats.md) and [**STATIONSTATS**](stationstats.md) structures after the current data is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fbde-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fbde-117">Return value</span></span>

<span data-ttu-id="0fbde-118">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0fbde-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0fbde-119">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="0fbde-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0fbde-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0fbde-120">Return code</span></span>                                                                                                   | <span data-ttu-id="0fbde-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fbde-121">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fbde-122"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="0fbde-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="0fbde-123">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="0fbde-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="0fbde-124">Chiamare [**IStats:: Connect**](istats-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="0fbde-124">Call [**IStats::Connect**](istats-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="0fbde-125"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="0fbde-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="0fbde-126">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="0fbde-126">The NPP is not capturing data.</span></span> <span data-ttu-id="0fbde-127">Chiamare [**IStats:: Start**](istats-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="0fbde-127">Call [**IStats::Start**](istats-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="0fbde-128"><dt>**NMERR \_ non \_ \_ solo statistiche**</dt></span><span class="sxs-lookup"><span data-stu-id="0fbde-128"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>        | <span data-ttu-id="0fbde-129">L'oggetto NPP è connesso alla rete, ma non con il metodo [**IStats:: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0fbde-129">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="0fbde-130"><dt>**NMERR \_ Nessuna \_ statistica di conversazione \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0fbde-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="0fbde-131">La configurazione per questa connessione è impostata in modo da non salvare le statistiche di conversazione.</span><span class="sxs-lookup"><span data-stu-id="0fbde-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="0fbde-132">Per salvare le statistiche di conversazione, arrestare l'acquisizione, impostare **NoConversationStats = Yes** nel BLOB di configurazione, quindi riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="0fbde-132">To save conversation statistics, stop the capture, set **NoConversationStats = YES** in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0fbde-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fbde-133">Remarks</span></span>

<span data-ttu-id="0fbde-134">Questo metodo può essere chiamato solo mentre è in corso l'acquisizione dei dati; Quando l'acquisizione corrente viene sospesa, una chiamata a questo metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0fbde-134">This method can be called only while data capture is in progress; when the current capture is paused, a call to this method will not succeed.</span></span>

<span data-ttu-id="0fbde-135">Per avviare un'acquisizione, chiamare il metodo [**IStats:: Start**](istats-start.md) .</span><span class="sxs-lookup"><span data-stu-id="0fbde-135">To start a capture, call the [**IStats::Start**](istats-start.md) method.</span></span> <span data-ttu-id="0fbde-136">Per recuperare altri tipi di statistiche, chiamare [**IStats:: GetTotalStatistics**](istats-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="0fbde-136">To retrieve other types of statistics, call [**IStats::GetTotalStatistics**](istats-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fbde-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fbde-137">Requirements</span></span>



| <span data-ttu-id="0fbde-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fbde-138">Requirement</span></span> | <span data-ttu-id="0fbde-139">Valore</span><span class="sxs-lookup"><span data-stu-id="0fbde-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fbde-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fbde-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0fbde-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0fbde-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0fbde-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fbde-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0fbde-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0fbde-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0fbde-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fbde-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fbde-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fbde-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0fbde-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0fbde-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fbde-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fbde-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fbde-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fbde-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fbde-149">**IStats**</span><span class="sxs-lookup"><span data-stu-id="0fbde-149">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="0fbde-150">**IStats:: GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="0fbde-150">**IStats::GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="0fbde-151">**IStats:: Start**</span><span class="sxs-lookup"><span data-stu-id="0fbde-151">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="0fbde-152">**IStats:: Connect**</span><span class="sxs-lookup"><span data-stu-id="0fbde-152">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="0fbde-153">**SESSIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="0fbde-153">**SESSIONSTATS**</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="0fbde-154">**STATIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="0fbde-154">**STATIONSTATS**</span></span>](stationstats.md)
</dt> </dl>

 

 




