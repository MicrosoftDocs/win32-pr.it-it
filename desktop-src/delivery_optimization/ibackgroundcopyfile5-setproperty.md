---
title: Metodo SetProperty IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Imposta una proprietà generica di un trasferimento di file di ottimizzazione recapito.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- Metodo SetProperty
- Metodo SetProperty, interfaccia IBackgroundCopyFile5
- Interfaccia IBackgroundCopyFile5, metodo SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964127"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a><span data-ttu-id="c5ea5-106">Metodo IBackgroundCopyFile5:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="c5ea5-106">IBackgroundCopyFile5::SetProperty method</span></span>

<span data-ttu-id="c5ea5-107">Imposta una proprietà generica di un trasferimento di file di ottimizzazione recapito.</span><span class="sxs-lookup"><span data-stu-id="c5ea5-107">Sets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ea5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5ea5-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="c5ea5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5ea5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ea5-110">*PropertyId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5ea5-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ea5-111">Specifica la proprietà da impostare.</span><span class="sxs-lookup"><span data-stu-id="c5ea5-111">Specifies the property to be set.</span></span>

</dd> <dt>

<span data-ttu-id="c5ea5-112">*ProertyValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c5ea5-112">*ProertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ea5-113">Puntatore a un'Unione che specifica il valore da impostare.</span><span class="sxs-lookup"><span data-stu-id="c5ea5-113">A pointer to a union that specifies the value to be set.</span></span> <span data-ttu-id="c5ea5-114">Viene usato il membro dell'Unione appropriato per l'ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5ea5-114">The union member appropriate for the property ID is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ea5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5ea5-115">Return value</span></span>

<span data-ttu-id="c5ea5-116">Se questo metodo ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="c5ea5-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="c5ea5-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5ea5-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ea5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5ea5-118">Requirements</span></span>



| <span data-ttu-id="c5ea5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ea5-119">Requirement</span></span> | <span data-ttu-id="c5ea5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c5ea5-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ea5-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5ea5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ea5-122">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5ea5-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c5ea5-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5ea5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ea5-124">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c5ea5-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c5ea5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5ea5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ea5-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea5-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5ea5-127">IDL</span><span class="sxs-lookup"><span data-stu-id="c5ea5-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5ea5-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea5-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c5ea5-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="c5ea5-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c5ea5-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea5-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c5ea5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ea5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5ea5-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea5-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c5ea5-133">IID</span><span class="sxs-lookup"><span data-stu-id="c5ea5-133">IID</span></span><br/>                      | <span data-ttu-id="c5ea5-134">IID_IBackgroundCopyFile5 viene definito come 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="c5ea5-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c5ea5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5ea5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ea5-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="c5ea5-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="c5ea5-137">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="c5ea5-137">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





