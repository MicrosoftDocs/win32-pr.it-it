---
title: Funzione MpScanControl (MpClient. h)
description: Consente il controllo di un'analisi che è stata avviata in modo asincrono tramite MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpScanControl
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476498"
---
# <a name="mpscancontrol-function"></a><span data-ttu-id="61a1f-104">MpScanControl (funzione)</span><span class="sxs-lookup"><span data-stu-id="61a1f-104">MpScanControl function</span></span>

<span data-ttu-id="61a1f-105">Consente il controllo di un'analisi che è stata avviata in modo asincrono tramite [**MpScanStart**](mpscanstart.md).</span><span class="sxs-lookup"><span data-stu-id="61a1f-105">Allows the control of a scan that was asynchronously initiated via [**MpScanStart**](mpscanstart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="61a1f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61a1f-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a><span data-ttu-id="61a1f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="61a1f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a1f-108">*hScanHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61a1f-108">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61a1f-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="61a1f-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="61a1f-110">Handle per un'operazione di analisi asincrona.</span><span class="sxs-lookup"><span data-stu-id="61a1f-110">Handle to an asynchronous scan operation.</span></span> <span data-ttu-id="61a1f-111">Questo handle viene restituito dalla funzione [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="61a1f-111">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="61a1f-112">Questo parametro può essere impostato anche sull'handle di interfaccia di malware Protection Manager restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) per controllare un'analisi avviata dal sistema, nel qual caso il chiamante deve avere privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="61a1f-112">This parameter can also be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) function to control a system initiated scan, in which case the caller must have administrative privilege.</span></span>

</dd> <dt>

<span data-ttu-id="61a1f-113">*ScanControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61a1f-113">*ScanControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61a1f-114">Tipo: **MPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="61a1f-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="61a1f-115">Specifica un'opzione di controllo Scan.</span><span class="sxs-lookup"><span data-stu-id="61a1f-115">Specifies a scan control option.</span></span> <span data-ttu-id="61a1f-116">Questo parametro deve essere una delle opzioni di controllo seguenti:</span><span class="sxs-lookup"><span data-stu-id="61a1f-116">This parameter must be one of the following control options:</span></span>



| <span data-ttu-id="61a1f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="61a1f-117">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="61a1f-118">Significato</span><span class="sxs-lookup"><span data-stu-id="61a1f-118">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="61a1f-119"><dt>**\_interruzione MPCONTROL**</dt></span><span class="sxs-lookup"><span data-stu-id="61a1f-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl>    | <span data-ttu-id="61a1f-120">Interrompere l'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="61a1f-120">Abort the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <span data-ttu-id="61a1f-121"><dt>**MPCONTROL \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="61a1f-121"><dt>**MPCONTROL\_PAUSE**</dt></span></span> </dl>    | <span data-ttu-id="61a1f-122">Sospendere l'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="61a1f-122">Pause the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <span data-ttu-id="61a1f-123"><dt>**Riprendi MPCONTROL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61a1f-123"><dt>**MPCONTROL\_RESUME**</dt></span></span> </dl> | <span data-ttu-id="61a1f-124">Riprendere l'operazione di analisi sospesa.</span><span class="sxs-lookup"><span data-stu-id="61a1f-124">Resume the paused scan operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a1f-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61a1f-125">Return value</span></span>

<span data-ttu-id="61a1f-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="61a1f-126">Type: **HRESULT**</span></span>

<span data-ttu-id="61a1f-127">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="61a1f-127">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="61a1f-128">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="61a1f-128">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="61a1f-129">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="61a1f-129">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a1f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61a1f-130">Requirements</span></span>



| <span data-ttu-id="61a1f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a1f-131">Requirement</span></span> | <span data-ttu-id="61a1f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="61a1f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61a1f-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61a1f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="61a1f-134">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61a1f-134">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="61a1f-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61a1f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="61a1f-136">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61a1f-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61a1f-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61a1f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="61a1f-138"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="61a1f-138"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="61a1f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="61a1f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61a1f-140"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61a1f-140"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61a1f-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61a1f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a1f-142">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="61a1f-142">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="61a1f-143">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="61a1f-143">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="61a1f-144">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="61a1f-144">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





