---
title: Metodo IDWriteTextLayout3 SetLineSpacing
description: Imposta spaziatura riga. | Metodo IDWriteTextLayout3 SetLineSpacing
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Scrittura diretta Metodo SetLineSpacing
- Metodo SetLineSpacing scrittura diretta, interfaccia IDWriteTextLayout3
- IDWriteTextLayout3 Interface Direct Write, Metodo SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321218"
---
# <a name="idwritetextlayout3setlinespacing-method"></a><span data-ttu-id="75378-107">Metodo IDWriteTextLayout3:: SetLineSpacing</span><span class="sxs-lookup"><span data-stu-id="75378-107">IDWriteTextLayout3::SetLineSpacing method</span></span>

<span data-ttu-id="75378-108">Imposta spaziatura riga.</span><span class="sxs-lookup"><span data-stu-id="75378-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="75378-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75378-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="75378-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="75378-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75378-111">*lineSpacingOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75378-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75378-112">Come gestire lo spazio tra le linee.</span><span class="sxs-lookup"><span data-stu-id="75378-112">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75378-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75378-113">Return value</span></span>

<span data-ttu-id="75378-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="75378-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="75378-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75378-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="75378-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75378-116">Requirements</span></span>



| <span data-ttu-id="75378-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="75378-117">Requirement</span></span> | <span data-ttu-id="75378-118">Valore</span><span class="sxs-lookup"><span data-stu-id="75378-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75378-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75378-119">Minimum supported client</span></span><br/> | <span data-ttu-id="75378-120">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75378-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="75378-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75378-121">Minimum supported server</span></span><br/> | <span data-ttu-id="75378-122">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="75378-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75378-123">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75378-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="75378-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="75378-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="75378-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="75378-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="75378-126"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75378-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="75378-127">DLL</span><span class="sxs-lookup"><span data-stu-id="75378-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75378-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75378-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75378-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75378-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75378-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="75378-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





