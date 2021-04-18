---
description: Il metodo GetConversationStatistics recupera le informazioni sulla sessione e sulla stazione relative all'acquisizione corrente.
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: 'Metodo IDelaydC:: GetConversationStatistics (Netmon. h)'
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
ms.openlocfilehash: aaba5ccfbab48639f53395519f001f5f8e85e483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305887"
---
# <a name="idelaydcgetconversationstatistics-method"></a><span data-ttu-id="dfacb-103">Metodo IDelaydC:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="dfacb-103">IDelaydC::GetConversationStatistics method</span></span>

<span data-ttu-id="dfacb-104">Il metodo **GetConversationStatistics** recupera le informazioni sulla [*sessione*](s.md) e sulla [*stazione*](s.md) relative all'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="dfacb-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfacb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfacb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="dfacb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfacb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfacb-107">*nSessions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dfacb-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfacb-108">Puntatore a un valore DWORD che contiene il numero di [*sessioni*](s.md) registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="dfacb-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="dfacb-109">*lpSessionStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dfacb-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfacb-110">Puntatore a una struttura [SESSIONSTATS](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="dfacb-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dfacb-111">*nStations* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dfacb-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfacb-112">Puntatore a un valore DWORD che contiene il numero di [*stazioni*](s.md) registrate per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="dfacb-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="dfacb-113">*lpStationStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dfacb-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfacb-114">Puntatore a una struttura [STATIONSTATS](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="dfacb-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dfacb-115">*fClearAfterReading* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfacb-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfacb-116">Flag usato per indicare Network Monitor per cancellare l'archiviazione interna delle strutture [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) dopo aver recuperato le informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="dfacb-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfacb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dfacb-117">Return value</span></span>

<span data-ttu-id="dfacb-118">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="dfacb-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dfacb-119">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="dfacb-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="dfacb-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dfacb-120">Return code</span></span>                                                                                                   | <span data-ttu-id="dfacb-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfacb-121">Description</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfacb-122"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacb-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="dfacb-123">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="dfacb-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="dfacb-124">Chiamare [IDelaydC:: Connect](idelaydc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="dfacb-124">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="dfacb-125"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacb-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="dfacb-126">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="dfacb-126">The NPP is not capturing data.</span></span> <span data-ttu-id="dfacb-127">Chiamare [IDelaydC:: Start](idelaydc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="dfacb-127">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="dfacb-128"><dt>**NMERR \_ non \_ ritardato**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacb-128"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>            | <span data-ttu-id="dfacb-129">L'oggetto NPP è connesso alla rete, ma non con il metodo [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="dfacb-129">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="dfacb-130"><dt>**NMERR \_ Nessuna \_ statistica di conversazione \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacb-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="dfacb-131">La configurazione per questa connessione è impostata in modo da non salvare le statistiche di conversazione.</span><span class="sxs-lookup"><span data-stu-id="dfacb-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="dfacb-132">Per salvare le statistiche di conversazione, arrestare l'acquisizione, impostare NoConversationStats = YES nel BLOB di configurazione, quindi riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="dfacb-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfacb-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfacb-133">Remarks</span></span>

<span data-ttu-id="dfacb-134">Questo metodo può essere chiamato solo mentre è in corso l'acquisizione dei dati; Quando l'acquisizione corrente viene sospesa, le chiamate a questo metodo non riusciranno.</span><span class="sxs-lookup"><span data-stu-id="dfacb-134">This method can only be called only while data capture is in progress; when the current capture is paused, calls to this method will not succeed.</span></span> <span data-ttu-id="dfacb-135">Per avviare un'acquisizione, chiamare il metodo [IDelaydC:: Start](idelaydc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="dfacb-135">To start a capture, call the [IDelaydC::Start](idelaydc-start.md) method.</span></span>

<span data-ttu-id="dfacb-136">Per recuperare altri tipi di statistiche, chiamare [IDelaydC:: GetTotalStatistics](idelaydc-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="dfacb-136">To retrieve other types of statistics, call [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfacb-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfacb-137">Requirements</span></span>



| <span data-ttu-id="dfacb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfacb-138">Requirement</span></span> | <span data-ttu-id="dfacb-139">Valore</span><span class="sxs-lookup"><span data-stu-id="dfacb-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfacb-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfacb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="dfacb-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dfacb-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dfacb-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfacb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="dfacb-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dfacb-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dfacb-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dfacb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfacb-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfacb-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dfacb-146">DLL</span><span class="sxs-lookup"><span data-stu-id="dfacb-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfacb-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfacb-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfacb-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfacb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfacb-149">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="dfacb-149">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="dfacb-150">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="dfacb-150">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="dfacb-151">IDelaydC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="dfacb-151">IDelaydC::GetTotalStatistics</span></span>](idelaydc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="dfacb-152">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="dfacb-152">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="dfacb-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="dfacb-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="dfacb-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="dfacb-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




