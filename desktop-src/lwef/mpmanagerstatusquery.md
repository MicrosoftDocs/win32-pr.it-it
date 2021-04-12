---
title: Funzione MpManagerStatusQuery (MpClient. h)
description: Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager. | Funzione MpManagerStatusQuery (MpClient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpManagerStatusQuery
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352251"
---
# <a name="mpmanagerstatusquery-function"></a><span data-ttu-id="e5d1e-105">MpManagerStatusQuery (funzione)</span><span class="sxs-lookup"><span data-stu-id="e5d1e-105">MpManagerStatusQuery function</span></span>

<span data-ttu-id="e5d1e-106">\[**MpManagerStatusQuery** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="e5d1e-106">\[**MpManagerStatusQuery** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="e5d1e-107">Usare invece [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span><span class="sxs-lookup"><span data-stu-id="e5d1e-107">Instead, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span></span>

<span data-ttu-id="e5d1e-108">Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="e5d1e-108">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d1e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5d1e-109">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e5d1e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5d1e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d1e-111">*hMpHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5d1e-111">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d1e-112">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e5d1e-112">Type: **MPHANDLE**</span></span>

<span data-ttu-id="e5d1e-113">Handle per l'interfaccia di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="e5d1e-113">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="e5d1e-114">Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="e5d1e-114">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e5d1e-115">*pStatusInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e5d1e-115">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d1e-116">Tipo: **PMPSTATUS \_ info**</span><span class="sxs-lookup"><span data-stu-id="e5d1e-116">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="e5d1e-117">Puntatore a una struttura che restituisce informazioni sullo stato relative a Last scansioni, minacce attive e stato di vari componenti.</span><span class="sxs-lookup"><span data-stu-id="e5d1e-117">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="e5d1e-118">Vedere [**MPSTATUS \_ info**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="e5d1e-118">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d1e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5d1e-119">Return value</span></span>

<span data-ttu-id="e5d1e-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e5d1e-120">Type: **HRESULT**</span></span>

<span data-ttu-id="e5d1e-121">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e5d1e-121">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="e5d1e-122">Questa chiamata di funzione ha esito positivo anche se un servizio antimalware non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e5d1e-122">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="e5d1e-123">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="e5d1e-123">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="e5d1e-124">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="e5d1e-124">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d1e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5d1e-125">Requirements</span></span>



| <span data-ttu-id="e5d1e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d1e-126">Requirement</span></span> | <span data-ttu-id="e5d1e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e5d1e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d1e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5d1e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d1e-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e5d1e-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e5d1e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5d1e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d1e-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e5d1e-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e5d1e-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5d1e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d1e-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d1e-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5d1e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e5d1e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5d1e-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5d1e-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5d1e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5d1e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d1e-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="e5d1e-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="e5d1e-138">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="e5d1e-138">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="e5d1e-139">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="e5d1e-139">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="e5d1e-140">**\_informazioni MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="e5d1e-140">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





