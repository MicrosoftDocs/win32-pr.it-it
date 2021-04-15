---
title: Funzione MpUpdateControl (MpClient. h)
description: Consente il controllo di un'operazione di aggiornamento della firma avviata in modo asincrono tramite MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpUpdateControl
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477656"
---
# <a name="mpupdatecontrol-function"></a><span data-ttu-id="3718a-104">MpUpdateControl (funzione)</span><span class="sxs-lookup"><span data-stu-id="3718a-104">MpUpdateControl function</span></span>

<span data-ttu-id="3718a-105">Consente il controllo di un'operazione di aggiornamento della firma avviata in modo asincrono tramite [**MpUpdateStart**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="3718a-105">Allows the control of a signature update operation that was asynchronously initiated via [**MpUpdateStart**](mpupdatestart.md).</span></span> <span data-ttu-id="3718a-106">La chiamata a questa funzione richiede privilegi amministrativi perché consente l'annullamento di un aggiornamento della firma a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="3718a-106">Calling this function requires administrator privilege as it allows the cancellation of a system-wide signature update.</span></span>

## <a name="syntax"></a><span data-ttu-id="3718a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3718a-107">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a><span data-ttu-id="3718a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3718a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3718a-109">*hUpdateHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3718a-109">*hUpdateHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3718a-110">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="3718a-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="3718a-111">Handle per un'operazione di aggiornamento della firma asincrona.</span><span class="sxs-lookup"><span data-stu-id="3718a-111">Handle to an asynchronous signature update operation.</span></span> <span data-ttu-id="3718a-112">Questo handle viene restituito dalla funzione [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="3718a-112">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3718a-113">*UpdateControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3718a-113">*UpdateControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3718a-114">Tipo: **MPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="3718a-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="3718a-115">Specifica l'opzione di controllo dell'aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="3718a-115">Specifies the signature update control option.</span></span> <span data-ttu-id="3718a-116">Deve essere il valore seguente:</span><span class="sxs-lookup"><span data-stu-id="3718a-116">It must be the following value:</span></span>



| <span data-ttu-id="3718a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3718a-117">Value</span></span>                                                                                                                                                               | <span data-ttu-id="3718a-118">Significato</span><span class="sxs-lookup"><span data-stu-id="3718a-118">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="3718a-119"><dt>**\_interruzione MPCONTROL**</dt></span><span class="sxs-lookup"><span data-stu-id="3718a-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="3718a-120">Interrompere l'operazione di aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="3718a-120">Abort the signature update operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3718a-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3718a-121">Return value</span></span>

<span data-ttu-id="3718a-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3718a-122">Type: **HRESULT**</span></span>

<span data-ttu-id="3718a-123">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3718a-123">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="3718a-124">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="3718a-124">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="3718a-125">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="3718a-125">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3718a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3718a-126">Requirements</span></span>



| <span data-ttu-id="3718a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3718a-127">Requirement</span></span> | <span data-ttu-id="3718a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3718a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3718a-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3718a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3718a-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3718a-130">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3718a-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3718a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3718a-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3718a-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3718a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3718a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3718a-134"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3718a-134"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3718a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3718a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3718a-136"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3718a-136"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3718a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3718a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3718a-138">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="3718a-138">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="3718a-139">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="3718a-139">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





