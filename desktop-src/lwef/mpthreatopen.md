---
title: Funzione MpThreatOpen (MpClient. h)
description: Restituisce un handle di enumerazione allo scopo di recuperare le minacce.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpThreatOpen
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301674"
---
# <a name="mpthreatopen-function"></a><span data-ttu-id="b9d63-104">MpThreatOpen (funzione)</span><span class="sxs-lookup"><span data-stu-id="b9d63-104">MpThreatOpen function</span></span>

<span data-ttu-id="b9d63-105">Restituisce un handle di enumerazione allo scopo di recuperare le minacce.</span><span class="sxs-lookup"><span data-stu-id="b9d63-105">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="b9d63-106">Questa funzione può essere utilizzata per aprire le minacce rilevate da un'analisi specifica, tutte le minacce attive nel sistema, la cronologia della disinfezione da minacce o tutte le minacce presenti nel database di firma.</span><span class="sxs-lookup"><span data-stu-id="b9d63-106">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9d63-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9d63-107">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a><span data-ttu-id="b9d63-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9d63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9d63-109">*hScanHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9d63-109">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9d63-110">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b9d63-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="b9d63-111">Può essere un handle per un'operazione di analisi completata, restituito dalla funzione [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="b9d63-111">Can be a handle to a completed scan operation, returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="b9d63-112">In alternativa, questo parametro può essere impostato sull'handle di interfaccia di malware Protection Manager restituito da [**MpManagerOpen**](mpmanageropen.md) per enumerare tutte le minacce attive nel sistema, la cronologia della disinfettazione delle minacce o le minacce del database di firma.</span><span class="sxs-lookup"><span data-stu-id="b9d63-112">Alternately, this parameter can be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) to enumerate all active threats in the system, the history of threat disinfection, or threats from signature database.</span></span>

</dd> <dt>

<span data-ttu-id="b9d63-113">*ThreatSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9d63-113">*ThreatSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9d63-114">Tipo: **\_ origine MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="b9d63-114">Type: **MPTHREAT\_SOURCE**</span></span>

<span data-ttu-id="b9d63-115">Utilizzato per controllare l'origine dell'enumerazione delle minacce.</span><span class="sxs-lookup"><span data-stu-id="b9d63-115">Used to control the source of threat enumeration.</span></span> <span data-ttu-id="b9d63-116">I valori possibili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b9d63-116">The possible values for this parameter are:</span></span>



| <span data-ttu-id="b9d63-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b9d63-117">Value</span></span>                                                                                                                                                                                                 | <span data-ttu-id="b9d63-118">Significato</span><span class="sxs-lookup"><span data-stu-id="b9d63-118">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <span data-ttu-id="b9d63-119"><dt>**\_analisi origine \_ MPTHREAT**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-119"><dt>**MPTHREAT\_SOURCE\_SCAN**</dt></span></span> </dl>                   | <span data-ttu-id="b9d63-120">Minacce associate all'handle di analisi specifico.</span><span class="sxs-lookup"><span data-stu-id="b9d63-120">Threats that are associated with the specific scan handle.</span></span><br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <span data-ttu-id="b9d63-121"><dt>**\_origine MPTHREAT \_ attiva**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-121"><dt>**MPTHREAT\_SOURCE\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="b9d63-122">Minacce attualmente attive nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b9d63-122">Threats that are currently active in the system.</span></span><br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <span data-ttu-id="b9d63-123"><dt>**\_Cronologia origine \_ MPTHREAT**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-123"><dt>**MPTHREAT\_SOURCE\_HISTORY**</dt></span></span> </dl>          | <span data-ttu-id="b9d63-124">Minacce che vengono eseguite e conservate come cronologia.</span><span class="sxs-lookup"><span data-stu-id="b9d63-124">Threats that are acted upon and preserved as a history.</span></span><br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <span data-ttu-id="b9d63-125"><dt>**\_ \_ quarantena origine MPTHREAT**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-125"><dt>**MPTHREAT\_SOURCE\_QUARANTINE**</dt></span></span> </dl> | <span data-ttu-id="b9d63-126">Minacce in quarantena.</span><span class="sxs-lookup"><span data-stu-id="b9d63-126">Threats that are quarantined.</span></span><br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <span data-ttu-id="b9d63-127"><dt>**\_firma di origine MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-127"><dt>**MPTHREAT\_SOURCE\_SIGNATURE**</dt></span></span> </dl>    | <span data-ttu-id="b9d63-128">Minacce che è possibile rilevare con il database della firma corrente.</span><span class="sxs-lookup"><span data-stu-id="b9d63-128">Threats that are possible to detect with the current signature database.</span></span><br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <span data-ttu-id="b9d63-129"><dt>**\_stato origine \_ MPTHREAT**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-129"><dt>**MPTHREAT\_SOURCE\_STATE**</dt></span></span> </dl>                | <span data-ttu-id="b9d63-130">Minacce che sono state eseguite di recente.</span><span class="sxs-lookup"><span data-stu-id="b9d63-130">Threats that have been acted upon recently.</span></span> <span data-ttu-id="b9d63-131">("Di recente" è definito da un'impostazione interna configurabile).</span><span class="sxs-lookup"><span data-stu-id="b9d63-131">("Recently" is defined by a configurable internal setting.)</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b9d63-132">*ThreatType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9d63-132">*ThreatType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9d63-133">Tipo: **MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="b9d63-133">Type: **MPTHREAT\_TYPE**</span></span>

<span data-ttu-id="b9d63-134">Utilizzato per filtrare le minacce enumerate in base al tipo di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="b9d63-134">Used to filter enumerated threats based on the detection type.</span></span> <span data-ttu-id="b9d63-135">I valori possibili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b9d63-135">The possible values for this parameter are:</span></span>



| <span data-ttu-id="b9d63-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b9d63-136">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="b9d63-137">Significato</span><span class="sxs-lookup"><span data-stu-id="b9d63-137">Meaning</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <span data-ttu-id="b9d63-138"><dt>**MPTHREAT \_ tipo \_ KNOWNBAD**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-138"><dt>**MPTHREAT\_TYPE\_KNOWNBAD**</dt></span></span> </dl>       | <span data-ttu-id="b9d63-139">Il rilevamento viene eseguito in base a una firma specifica, un'emulazione o un altro metodo di rilevamento delle minacce.</span><span class="sxs-lookup"><span data-stu-id="b9d63-139">Detection is performed based on a specific signature, emulation, or other threat detection method.</span></span><br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <span data-ttu-id="b9d63-140"><dt>**\_tipo MPTHREAT \_ sospetto**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-140"><dt>**MPTHREAT\_TYPE\_SUSPICIOUS**</dt></span></span> </dl> | <span data-ttu-id="b9d63-141">Il rilevamento viene eseguito in base al monitoraggio del comportamento.</span><span class="sxs-lookup"><span data-stu-id="b9d63-141">Detection is performed based on behavior monitoring.</span></span><br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <span data-ttu-id="b9d63-142"><dt>**\_tipo MPTHREAT \_ sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-142"><dt>**MPTHREAT\_TYPE\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="b9d63-143">Il rilevamento viene eseguito in base a minacce sconosciute (non classificate).</span><span class="sxs-lookup"><span data-stu-id="b9d63-143">Detection is performed based on unknown threats (unclassified).</span></span><br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <span data-ttu-id="b9d63-144"><dt>**MPTHREAT \_ tipo \_ KNOWNGOOD**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-144"><dt>**MPTHREAT\_TYPE\_KNOWNGOOD**</dt></span></span> </dl>    | <span data-ttu-id="b9d63-145">Il rilevamento viene eseguito in base a minacce sicure note.</span><span class="sxs-lookup"><span data-stu-id="b9d63-145">Detection is performed based on known safe threats.</span></span><br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <span data-ttu-id="b9d63-146"><dt>**MPTHREAT di \_ tipo \_ NIS**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-146"><dt>**MPTHREAT\_TYPE\_NIS**</dt></span></span> </dl>                      | <span data-ttu-id="b9d63-147">Il rilevamento viene eseguito in base alle minacce NIS.</span><span class="sxs-lookup"><span data-stu-id="b9d63-147">Detection is performed based on NIS threats.</span></span><br/>                                                       |



 

</dd> <dt>

<span data-ttu-id="b9d63-148">*phThreatEnumHandle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b9d63-148">*phThreatEnumHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9d63-149">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b9d63-149">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="b9d63-150">Handle di enumerazione della minaccia restituito che identifica il contesto di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="b9d63-150">Returned threat enumeration handle which identifies the enumeration context.</span></span> <span data-ttu-id="b9d63-151">Questo handle può essere usato per enumerare le informazioni sulle minacce usando [**MpThreatEnumerate**](mpthreatenumerate.md).</span><span class="sxs-lookup"><span data-stu-id="b9d63-151">This handle can be used to enumerate threat information using [**MpThreatEnumerate**](mpthreatenumerate.md).</span></span> <span data-ttu-id="b9d63-152">L'handle deve essere chiuso con la funzione [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="b9d63-152">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9d63-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9d63-153">Return value</span></span>

<span data-ttu-id="b9d63-154">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b9d63-154">Type: **HRESULT**</span></span>

<span data-ttu-id="b9d63-155">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b9d63-155">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="b9d63-156">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="b9d63-156">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="b9d63-157">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="b9d63-157">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9d63-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9d63-158">Requirements</span></span>



| <span data-ttu-id="b9d63-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9d63-159">Requirement</span></span> | <span data-ttu-id="b9d63-160">Valore</span><span class="sxs-lookup"><span data-stu-id="b9d63-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d63-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9d63-161">Minimum supported client</span></span><br/> | <span data-ttu-id="b9d63-162">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b9d63-162">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b9d63-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9d63-163">Minimum supported server</span></span><br/> | <span data-ttu-id="b9d63-164">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b9d63-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9d63-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9d63-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9d63-166"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-166"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9d63-167">DLL</span><span class="sxs-lookup"><span data-stu-id="b9d63-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9d63-168"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9d63-168"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9d63-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9d63-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d63-170">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="b9d63-170">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="b9d63-171">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="b9d63-171">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="b9d63-172">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="b9d63-172">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="b9d63-173">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="b9d63-173">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="b9d63-174">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="b9d63-174">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> </dl>

 

 





