---
title: Metodo GetDisplayName di metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera il nome visualizzato per il processo. In genere, il nome visualizzato viene usato per identificare il processo in un'interfaccia utente.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName (metodo)
- Metodo GetDisplayName, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, Metodo GetDisplayName
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964700"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a><span data-ttu-id="49c9f-107">Metodo metodo ibackgroundcopyjob:: GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="49c9f-107">IBackgroundCopyJob::GetDisplayName method</span></span>

<span data-ttu-id="49c9f-108">Recupera il nome visualizzato per il processo.</span><span class="sxs-lookup"><span data-stu-id="49c9f-108">Retrieves the display name for the job.</span></span> <span data-ttu-id="49c9f-109">In genere, il nome visualizzato viene usato per identificare il processo in un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="49c9f-109">Typically, you use the display name to identify the job in a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="49c9f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49c9f-110">Syntax</span></span>


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a><span data-ttu-id="49c9f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="49c9f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49c9f-112">*ppDisplayName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="49c9f-112">*ppDisplayName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49c9f-113">Stringa con terminazione null che contiene il nome visualizzato che identifica il processo.</span><span class="sxs-lookup"><span data-stu-id="49c9f-113">Null-terminated string that contains the display name that identifies the job.</span></span> <span data-ttu-id="49c9f-114">Più di un processo può avere lo stesso nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="49c9f-114">More than one job can have the same display name.</span></span> <span data-ttu-id="49c9f-115">Chiamare la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare *ppDisplayName* al termine.</span><span class="sxs-lookup"><span data-stu-id="49c9f-115">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppDisplayName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49c9f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49c9f-116">Return value</span></span>

<span data-ttu-id="49c9f-117">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="49c9f-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="49c9f-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="49c9f-118">Return code</span></span>                                                                                  | <span data-ttu-id="49c9f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49c9f-119">Description</span></span>                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="49c9f-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="49c9f-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="49c9f-121">Il nome visualizzato è stato recuperato.</span><span class="sxs-lookup"><span data-stu-id="49c9f-121">Display name was successfully retrieved.</span></span><br/>          |
| <dl> <span data-ttu-id="49c9f-122"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="49c9f-122"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="49c9f-123">Il parametro *ppDisplayName* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="49c9f-123">The *ppDisplayName* parameter cannot be **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="49c9f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49c9f-124">Requirements</span></span>



| <span data-ttu-id="49c9f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="49c9f-125">Requirement</span></span> | <span data-ttu-id="49c9f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="49c9f-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49c9f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49c9f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="49c9f-128">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="49c9f-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="49c9f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49c9f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="49c9f-130">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49c9f-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="49c9f-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49c9f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="49c9f-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="49c9f-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="49c9f-133">IDL</span><span class="sxs-lookup"><span data-stu-id="49c9f-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49c9f-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49c9f-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="49c9f-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="49c9f-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="49c9f-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49c9f-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="49c9f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="49c9f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49c9f-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49c9f-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="49c9f-139">IID</span><span class="sxs-lookup"><span data-stu-id="49c9f-139">IID</span></span><br/>                      | <span data-ttu-id="49c9f-140">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="49c9f-140">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="49c9f-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49c9f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c9f-142">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="49c9f-142">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

