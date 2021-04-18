---
title: Funzione MpManagerStatusQueryEx (MpClient. h)
description: Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager. | Funzione MpManagerStatusQueryEx (MpClient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpManagerStatusQueryEx
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321968"
---
# <a name="mpmanagerstatusqueryex-function"></a><span data-ttu-id="3386a-105">MpManagerStatusQueryEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="3386a-105">MpManagerStatusQueryEx function</span></span>

<span data-ttu-id="3386a-106">Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="3386a-106">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="3386a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3386a-107">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3386a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3386a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3386a-109">*hMpHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3386a-109">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3386a-110">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="3386a-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="3386a-111">Handle per l'interfaccia di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="3386a-111">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="3386a-112">Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="3386a-112">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3386a-113">*dwFlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3386a-113">*dwFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3386a-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3386a-114">Type: **DWORD**</span></span>

<span data-ttu-id="3386a-115">Controlla quali informazioni della query vengono restituite.</span><span class="sxs-lookup"><span data-stu-id="3386a-115">Controls which query information is returned.</span></span> <span data-ttu-id="3386a-116">Alcune informazioni sono costose e potrebbero non essere necessarie.</span><span class="sxs-lookup"><span data-stu-id="3386a-116">Some information is expensive and may not be needed.</span></span>



| <span data-ttu-id="3386a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3386a-117">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="3386a-118">Significato</span><span class="sxs-lookup"><span data-stu-id="3386a-118">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <span data-ttu-id="3386a-119"><dt>**\_flag di \_ query stato MP \_ \_ nessuno**</dt></span><span class="sxs-lookup"><span data-stu-id="3386a-119"><dt>**MP\_STATUS\_QUERY\_FLAGS\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="3386a-120">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3386a-120">Default.</span></span><br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <span data-ttu-id="3386a-121"><dt>**\_flag di \_ query stato MP \_ \_ nostate**</dt></span><span class="sxs-lookup"><span data-stu-id="3386a-121"><dt>**MP\_STATUS\_QUERY\_FLAG\_NOSTATE**</dt></span></span> </dl> | <span data-ttu-id="3386a-122">Non eseguire una query per ottenere informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="3386a-122">Do not query for state information.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3386a-123">*pStatusInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3386a-123">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3386a-124">Tipo: **PMPSTATUS \_ info**</span><span class="sxs-lookup"><span data-stu-id="3386a-124">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="3386a-125">Puntatore a una struttura che restituisce informazioni sullo stato relative a Last scansioni, minacce attive e stato di vari componenti.</span><span class="sxs-lookup"><span data-stu-id="3386a-125">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="3386a-126">Vedere [**MPSTATUS \_ info**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="3386a-126">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3386a-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3386a-127">Return value</span></span>

<span data-ttu-id="3386a-128">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3386a-128">Type: **HRESULT**</span></span>

<span data-ttu-id="3386a-129">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3386a-129">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="3386a-130">Questa chiamata di funzione ha esito positivo anche se un servizio antimalware non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3386a-130">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="3386a-131">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="3386a-131">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="3386a-132">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="3386a-132">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3386a-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3386a-133">Requirements</span></span>



| <span data-ttu-id="3386a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3386a-134">Requirement</span></span> | <span data-ttu-id="3386a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3386a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3386a-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3386a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3386a-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3386a-137">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3386a-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3386a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3386a-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3386a-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3386a-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3386a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3386a-141"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3386a-141"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3386a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3386a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3386a-143"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3386a-143"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3386a-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3386a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3386a-145">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="3386a-145">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="3386a-146">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="3386a-146">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="3386a-147">**\_informazioni MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="3386a-147">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





