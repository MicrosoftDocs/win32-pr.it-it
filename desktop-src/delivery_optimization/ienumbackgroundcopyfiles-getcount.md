---
title: Metodo GetCount IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Recupera un conteggio del numero di file nell'enumerazione.
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount (metodo)
- Metodo GetCount, interfaccia IEnumBackgroundCopyFiles
- Interfaccia IEnumBackgroundCopyFiles, metodo GetCount
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05e2672f0cda3c572024a0865b2fb534dddb6598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741471"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a><span data-ttu-id="15c10-106">Metodo IEnumBackgroundCopyFiles:: GetCount</span><span class="sxs-lookup"><span data-stu-id="15c10-106">IEnumBackgroundCopyFiles::GetCount method</span></span>

<span data-ttu-id="15c10-107">Recupera un conteggio del numero di file nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="15c10-107">Retrieves a count of the number of files in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c10-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15c10-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="15c10-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="15c10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c10-110">*pcount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="15c10-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15c10-111">Numero di file nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="15c10-111">Number of files in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c10-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15c10-112">Return value</span></span>

<span data-ttu-id="15c10-113">Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.</span><span class="sxs-lookup"><span data-stu-id="15c10-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c10-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15c10-114">Requirements</span></span>



| <span data-ttu-id="15c10-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="15c10-115">Requirement</span></span> | <span data-ttu-id="15c10-116">Valore</span><span class="sxs-lookup"><span data-stu-id="15c10-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15c10-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15c10-117">Minimum supported client</span></span><br/> | <span data-ttu-id="15c10-118">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="15c10-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="15c10-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15c10-119">Minimum supported server</span></span><br/> | <span data-ttu-id="15c10-120">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15c10-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="15c10-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15c10-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="15c10-122"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="15c10-122"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="15c10-123">IDL</span><span class="sxs-lookup"><span data-stu-id="15c10-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15c10-124"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15c10-124"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="15c10-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="15c10-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="15c10-126"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15c10-126"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="15c10-127">DLL</span><span class="sxs-lookup"><span data-stu-id="15c10-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15c10-128"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15c10-128"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="15c10-129">IID</span><span class="sxs-lookup"><span data-stu-id="15c10-129">IID</span></span><br/>                      | <span data-ttu-id="15c10-130">IID_IEnumBackgroundCopyFiles viene definito come CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="15c10-130">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="15c10-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15c10-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c10-132">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="15c10-132">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





