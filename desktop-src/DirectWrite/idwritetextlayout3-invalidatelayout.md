---
title: Metodo IDWriteTextLayout3 InvalidateLayout
description: Invalida il layout, forzando il layout da rimisurare prima di chiamare le metriche o le funzioni di disegno. Questa operazione è utile se la località di un tipo di carattere viene modificata e il layout deve essere ridisegnato o se le dimensioni di un client implementate IDWriteInlineObject cambiano.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Scrittura diretta metodo InvalidateLayout
- Metodo InvalidateLayout scrittura diretta, interfaccia IDWriteTextLayout3
- IDWriteTextLayout3 Interface Direct Write, metodo InvalidateLayout
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120254"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a><span data-ttu-id="de17a-107">Metodo IDWriteTextLayout3:: InvalidateLayout</span><span class="sxs-lookup"><span data-stu-id="de17a-107">IDWriteTextLayout3::InvalidateLayout method</span></span>

<span data-ttu-id="de17a-108">Invalida il layout, forzando il layout da rimisurare prima di chiamare le metriche o le funzioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="de17a-108">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="de17a-109">Questa operazione è utile se la località di un tipo di carattere viene modificata e il layout deve essere ridisegnato o se le dimensioni di un client implementate IDWriteInlineObject cambiano.</span><span class="sxs-lookup"><span data-stu-id="de17a-109">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="de17a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de17a-110">Syntax</span></span>


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a><span data-ttu-id="de17a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="de17a-111">Parameters</span></span>

<span data-ttu-id="de17a-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="de17a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de17a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de17a-113">Return value</span></span>

<span data-ttu-id="de17a-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="de17a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de17a-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de17a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="de17a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de17a-116">Requirements</span></span>



| <span data-ttu-id="de17a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="de17a-117">Requirement</span></span> | <span data-ttu-id="de17a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="de17a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de17a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de17a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="de17a-120">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de17a-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="de17a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de17a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="de17a-122">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="de17a-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="de17a-123">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de17a-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="de17a-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="de17a-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="de17a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="de17a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="de17a-126"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de17a-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="de17a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="de17a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de17a-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de17a-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de17a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de17a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de17a-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="de17a-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





