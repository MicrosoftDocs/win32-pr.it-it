---
title: Metodo IDWriteTextLayout3 GetLineSpacing
description: Ottiene le informazioni sulla spaziatura riga.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Scrittura diretta metodo GetLineSpacing
- Metodo GetLineSpacing scrittura diretta, interfaccia IDWriteTextLayout3
- IDWriteTextLayout3 Interface Direct Write, metodo GetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303030a5674f39c160804ae2dad5b91050d82f37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964454"
---
# <a name="idwritetextlayout3getlinespacing-method"></a><span data-ttu-id="96c33-106">Metodo IDWriteTextLayout3:: GetLineSpacing</span><span class="sxs-lookup"><span data-stu-id="96c33-106">IDWriteTextLayout3::GetLineSpacing method</span></span>

<span data-ttu-id="96c33-107">Ottiene le informazioni sulla spaziatura riga.</span><span class="sxs-lookup"><span data-stu-id="96c33-107">Gets line spacing information.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c33-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96c33-108">Syntax</span></span>


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="96c33-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="96c33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c33-110">*lineSpacingOptions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="96c33-110">*lineSpacingOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96c33-111">Come gestire lo spazio tra le linee.</span><span class="sxs-lookup"><span data-stu-id="96c33-111">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c33-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96c33-112">Return value</span></span>

<span data-ttu-id="96c33-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="96c33-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96c33-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96c33-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="96c33-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96c33-115">Requirements</span></span>



| <span data-ttu-id="96c33-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c33-116">Requirement</span></span> | <span data-ttu-id="96c33-117">Valore</span><span class="sxs-lookup"><span data-stu-id="96c33-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96c33-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96c33-118">Minimum supported client</span></span><br/> | <span data-ttu-id="96c33-119">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96c33-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="96c33-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96c33-120">Minimum supported server</span></span><br/> | <span data-ttu-id="96c33-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="96c33-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="96c33-122">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96c33-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="96c33-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="96c33-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="96c33-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="96c33-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="96c33-125"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96c33-125"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="96c33-126">DLL</span><span class="sxs-lookup"><span data-stu-id="96c33-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96c33-127"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96c33-127"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96c33-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96c33-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c33-129">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="96c33-129">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





