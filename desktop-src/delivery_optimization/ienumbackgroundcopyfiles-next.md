---
title: Metodo Next di IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Recupera un determinato numero di elementi nella sequenza di enumerazione. Se il numero di elementi rimasti nella sequenza è inferiore a quello richiesto, vengono recuperati gli elementi rimanenti.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Metodo Next
- Metodo Next, interfaccia IEnumBackgroundCopyFiles
- Interfaccia IEnumBackgroundCopyFiles, metodo Next
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964697"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a><span data-ttu-id="7ebd6-107">IEnumBackgroundCopyFiles:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="7ebd6-107">IEnumBackgroundCopyFiles::Next method</span></span>

<span data-ttu-id="7ebd6-108">Recupera un determinato numero di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="7ebd6-108">Retrieves a specified number of items in the enumeration sequence.</span></span> <span data-ttu-id="7ebd6-109">Se il numero di elementi rimasti nella sequenza è inferiore a quello richiesto, vengono recuperati gli elementi rimanenti.</span><span class="sxs-lookup"><span data-stu-id="7ebd6-109">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ebd6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ebd6-110">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="7ebd6-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ebd6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ebd6-112">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ebd6-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebd6-113">Numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="7ebd6-113">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="7ebd6-114">*rgelt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ebd6-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebd6-115">Matrice di oggetti [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="7ebd6-115">Array of [**IBackgroundCopyFile**](ibackgroundcopyfile.md) objects.</span></span> <span data-ttu-id="7ebd6-116">Al termine, è necessario rilasciare ogni oggetto in *rgelt* .</span><span class="sxs-lookup"><span data-stu-id="7ebd6-116">You must release each object in *rgelt* when done.</span></span>

</dd> <dt>

<span data-ttu-id="7ebd6-117">*pceltFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ebd6-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebd6-118">Numero di elementi restituiti in *rgelt*.</span><span class="sxs-lookup"><span data-stu-id="7ebd6-118">Number of elements returned in *rgelt*.</span></span> <span data-ttu-id="7ebd6-119">Se *celt* è uno, è possibile impostare *pceltFetched* su **null** .</span><span class="sxs-lookup"><span data-stu-id="7ebd6-119">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="7ebd6-120">In caso contrario, inizializzare il valore di *pceltFetched* su 0 prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="7ebd6-120">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ebd6-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ebd6-121">Return value</span></span>

<span data-ttu-id="7ebd6-122">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="7ebd6-122">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="7ebd6-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7ebd6-123">Return code</span></span>                                                                              | <span data-ttu-id="7ebd6-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ebd6-124">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ebd6-125"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd6-125"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="7ebd6-126">Il numero di elementi richiesti è stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="7ebd6-126">Successfully returned the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="7ebd6-127"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd6-127"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="7ebd6-128">Restituito minore del numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="7ebd6-128">Returned less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="7ebd6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ebd6-129">Requirements</span></span>



| <span data-ttu-id="7ebd6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ebd6-130">Requirement</span></span> | <span data-ttu-id="7ebd6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="7ebd6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ebd6-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ebd6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7ebd6-133">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ebd6-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7ebd6-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ebd6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7ebd6-135">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ebd6-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7ebd6-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ebd6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ebd6-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd6-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ebd6-138">IDL</span><span class="sxs-lookup"><span data-stu-id="7ebd6-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ebd6-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd6-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ebd6-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ebd6-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ebd6-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd6-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7ebd6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7ebd6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ebd6-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd6-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7ebd6-144">IID</span><span class="sxs-lookup"><span data-stu-id="7ebd6-144">IID</span></span><br/>                      | <span data-ttu-id="7ebd6-145">IID_IEnumBackgroundCopyFiles viene definito come CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="7ebd6-145">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="7ebd6-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ebd6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ebd6-147">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="7ebd6-147">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





