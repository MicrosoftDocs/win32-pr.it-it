---
title: Metodo GetError IBackgroundCopyError (Deliveryoptimization. h)
description: Recupera il codice di errore e identifica il contesto in cui si è verificato l'errore.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Metodo GetError
- Metodo GetError, interfaccia IBackgroundCopyError
- Interfaccia IBackgroundCopyError, metodo getError
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964129"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a><span data-ttu-id="61560-106">Metodo IBackgroundCopyError:: GetError</span><span class="sxs-lookup"><span data-stu-id="61560-106">IBackgroundCopyError::GetError method</span></span>

<span data-ttu-id="61560-107">Recupera il codice di errore e identifica il contesto in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="61560-107">Retrieves the error code and identify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="61560-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61560-108">Syntax</span></span>


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="61560-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="61560-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61560-110">*pContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="61560-110">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61560-111">Contesto in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="61560-111">Context in which the error occurred.</span></span> <span data-ttu-id="61560-112">Per un elenco di valori di contesto, vedere l'enumerazione [**BG_ERROR_CONTEXT**](bg-error-context.md) .</span><span class="sxs-lookup"><span data-stu-id="61560-112">For a list of context values, see the [**BG_ERROR_CONTEXT**](bg-error-context.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="61560-113">*pErrorCode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="61560-113">*pErrorCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61560-114">Codice di errore dell'errore che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="61560-114">Error code of the error that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61560-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61560-115">Return value</span></span>

<span data-ttu-id="61560-116">Questo metodo restituisce **S_OK** in esito positivo o uno dei valori HRESULT COM standard in errore.</span><span class="sxs-lookup"><span data-stu-id="61560-116">This method returns **S_OK** on success or one of the standard COM HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="61560-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61560-117">Requirements</span></span>



| <span data-ttu-id="61560-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="61560-118">Requirement</span></span> | <span data-ttu-id="61560-119">Valore</span><span class="sxs-lookup"><span data-stu-id="61560-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61560-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61560-120">Minimum supported client</span></span><br/> | <span data-ttu-id="61560-121">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="61560-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="61560-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61560-122">Minimum supported server</span></span><br/> | <span data-ttu-id="61560-123">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="61560-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="61560-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61560-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="61560-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="61560-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="61560-126">IDL</span><span class="sxs-lookup"><span data-stu-id="61560-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61560-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61560-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="61560-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="61560-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="61560-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61560-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="61560-130">DLL</span><span class="sxs-lookup"><span data-stu-id="61560-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61560-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61560-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="61560-132">IID</span><span class="sxs-lookup"><span data-stu-id="61560-132">IID</span></span><br/>                      | <span data-ttu-id="61560-133">IID_IBackgroundCopyError viene definito come 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="61560-133">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="61560-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61560-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61560-135">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="61560-135">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="61560-136">**IBackgroundCopyError:: GetFile**</span><span class="sxs-lookup"><span data-stu-id="61560-136">**IBackgroundCopyError::GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





