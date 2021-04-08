---
title: Metodo Skip IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Ignora il numero specificato successivo di elementi nella sequenza di enumerazione. Se nella sequenza sono rimasti meno elementi del numero richiesto di elementi da ignorare, l'ultimo elemento nella sequenza viene ignorato.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip (metodo)
- Metodo Skip, interfaccia IEnumBackgroundCopyFiles
- Interfaccia IEnumBackgroundCopyFiles, metodo Skip
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048008"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a><span data-ttu-id="027bd-107">Metodo IEnumBackgroundCopyFiles:: Skip</span><span class="sxs-lookup"><span data-stu-id="027bd-107">IEnumBackgroundCopyFiles::Skip method</span></span>

<span data-ttu-id="027bd-108">Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="027bd-108">Skips the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="027bd-109">Se nella sequenza sono rimasti meno elementi del numero richiesto di elementi da ignorare, l'ultimo elemento nella sequenza viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="027bd-109">If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="027bd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="027bd-110">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="027bd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="027bd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027bd-112">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="027bd-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="027bd-113">Numero di elementi da ignorare.</span><span class="sxs-lookup"><span data-stu-id="027bd-113">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="027bd-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="027bd-114">Return value</span></span>

<span data-ttu-id="027bd-115">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="027bd-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="027bd-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="027bd-116">Return code</span></span>                                                                              | <span data-ttu-id="027bd-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="027bd-117">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="027bd-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="027bd-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="027bd-119">Il numero di elementi richiesti è stato ignorato.</span><span class="sxs-lookup"><span data-stu-id="027bd-119">Successfully skipped the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="027bd-120"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="027bd-120"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="027bd-121">Ignorato minore del numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="027bd-121">Skipped less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="027bd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="027bd-122">Requirements</span></span>



| <span data-ttu-id="027bd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="027bd-123">Requirement</span></span> | <span data-ttu-id="027bd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="027bd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="027bd-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="027bd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="027bd-126">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="027bd-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="027bd-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="027bd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="027bd-128">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="027bd-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="027bd-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="027bd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="027bd-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="027bd-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="027bd-131">IDL</span><span class="sxs-lookup"><span data-stu-id="027bd-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="027bd-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="027bd-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="027bd-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="027bd-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="027bd-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="027bd-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="027bd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="027bd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="027bd-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="027bd-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="027bd-137">IID</span><span class="sxs-lookup"><span data-stu-id="027bd-137">IID</span></span><br/>                      | <span data-ttu-id="027bd-138">IID_IEnumBackgroundCopyFiles viene definito come CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="027bd-138">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="027bd-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="027bd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027bd-140">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="027bd-140">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





