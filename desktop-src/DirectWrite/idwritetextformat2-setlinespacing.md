---
title: Metodo IDWriteTextFormat2 SetLineSpacing
description: Imposta spaziatura riga. | Metodo IDWriteTextFormat2 SetLineSpacing
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- Scrittura diretta Metodo SetLineSpacing
- Metodo SetLineSpacing scrittura diretta, interfaccia IDWriteTextFormat2
- IDWriteTextFormat2 Interface Direct Write, Metodo SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3514c52c9b8a51666d36eec7ce893735635f3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234870"
---
# <a name="idwritetextformat2setlinespacing-method"></a><span data-ttu-id="5c2f8-107">Metodo IDWriteTextFormat2:: SetLineSpacing</span><span class="sxs-lookup"><span data-stu-id="5c2f8-107">IDWriteTextFormat2::SetLineSpacing method</span></span>

<span data-ttu-id="5c2f8-108">Imposta spaziatura riga.</span><span class="sxs-lookup"><span data-stu-id="5c2f8-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2f8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c2f8-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="5c2f8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c2f8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2f8-111">*lineSpacingOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c2f8-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2f8-112">Tipo: **const \* [**DWrite \_ line interlinea \_**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)**</span><span class="sxs-lookup"><span data-stu-id="5c2f8-112">Type: **const [**DWRITE\_LINE\_SPACING**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)\***</span></span>

<span data-ttu-id="5c2f8-113">Come gestire lo spazio tra le linee.</span><span class="sxs-lookup"><span data-stu-id="5c2f8-113">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2f8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c2f8-114">Return value</span></span>

<span data-ttu-id="5c2f8-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5c2f8-115">Type: **HRESULT**</span></span>

<span data-ttu-id="5c2f8-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c2f8-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c2f8-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c2f8-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2f8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c2f8-118">Requirements</span></span>



| <span data-ttu-id="5c2f8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c2f8-119">Requirement</span></span> | <span data-ttu-id="5c2f8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5c2f8-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2f8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c2f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2f8-122">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c2f8-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5c2f8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c2f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2f8-124">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c2f8-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5c2f8-125">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c2f8-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5c2f8-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="5c2f8-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="5c2f8-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c2f8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c2f8-128"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c2f8-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5c2f8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5c2f8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c2f8-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c2f8-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5c2f8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c2f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2f8-132">**IDWriteTextFormat2**</span><span class="sxs-lookup"><span data-stu-id="5c2f8-132">**IDWriteTextFormat2**</span></span>](idwritetextformat2.md)
</dt> </dl>

 

 





