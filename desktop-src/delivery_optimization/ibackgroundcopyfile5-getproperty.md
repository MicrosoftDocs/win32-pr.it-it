---
title: Metodo GetProperty IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Ottiene una proprietà generica di un trasferimento di file di ottimizzazione recapito.
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- Metodo GetProperty
- Metodo GetProperty, interfaccia IBackgroundCopyFile5
- Interfaccia IBackgroundCopyFile5, metodo GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119614"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a><span data-ttu-id="63cd2-106">Metodo IBackgroundCopyFile5:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="63cd2-106">IBackgroundCopyFile5::GetProperty method</span></span>

<span data-ttu-id="63cd2-107">Ottiene una proprietà generica di un trasferimento di file di ottimizzazione recapito.</span><span class="sxs-lookup"><span data-stu-id="63cd2-107">Gets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="63cd2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63cd2-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="63cd2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="63cd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63cd2-110">*PropertyId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63cd2-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63cd2-111">Specifica la proprietà del file di cui recuperare il valore.</span><span class="sxs-lookup"><span data-stu-id="63cd2-111">Specifies the file property whose value is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="63cd2-112">*PropertyValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="63cd2-112">*PropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63cd2-113">Valore della proprietà, restituito come puntatore a un'Unione BITS_FILE_PROPERTY_VALUE.</span><span class="sxs-lookup"><span data-stu-id="63cd2-113">The property value, returned as a pointer to a BITS_FILE_PROPERTY_VALUE union.</span></span> <span data-ttu-id="63cd2-114">Utilizzare il campo unione appropriato per il valore ID proprietà passato.</span><span class="sxs-lookup"><span data-stu-id="63cd2-114">Use the union field appropriate for the property ID value passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63cd2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63cd2-115">Return value</span></span>

<span data-ttu-id="63cd2-116">Se questo metodo ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="63cd2-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="63cd2-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63cd2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="63cd2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63cd2-118">Requirements</span></span>



| <span data-ttu-id="63cd2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="63cd2-119">Requirement</span></span> | <span data-ttu-id="63cd2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="63cd2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63cd2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63cd2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="63cd2-122">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="63cd2-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="63cd2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63cd2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="63cd2-124">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63cd2-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="63cd2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63cd2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="63cd2-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="63cd2-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="63cd2-127">IDL</span><span class="sxs-lookup"><span data-stu-id="63cd2-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63cd2-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63cd2-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="63cd2-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="63cd2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="63cd2-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63cd2-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="63cd2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="63cd2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63cd2-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63cd2-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="63cd2-133">IID</span><span class="sxs-lookup"><span data-stu-id="63cd2-133">IID</span></span><br/>                      | <span data-ttu-id="63cd2-134">IID_IBackgroundCopyFile5 viene definito come 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="63cd2-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="63cd2-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63cd2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63cd2-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="63cd2-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="63cd2-137">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="63cd2-137">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





