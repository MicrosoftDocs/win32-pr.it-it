---
title: Metodo IDWriteTextLayout DetermineMinWidth
description: Determina la larghezza minima possibile con cui è possibile impostare il layout senza interruzioni di emergenza tra i caratteri di parole intere che si verificano.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Scrittura diretta metodo DetermineMinWidth
- Metodo DetermineMinWidth scrittura diretta, interfaccia IDWriteTextLayout
- IDWriteTextLayout Interface Direct Write, metodo DetermineMinWidth
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330156"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a><span data-ttu-id="f53f1-106">IDWriteTextLayout::D Metodo etermineMinWidth</span><span class="sxs-lookup"><span data-stu-id="f53f1-106">IDWriteTextLayout::DetermineMinWidth method</span></span>

<span data-ttu-id="f53f1-107">Determina la larghezza minima possibile con cui è possibile impostare il layout senza interruzioni di emergenza tra i caratteri di parole intere che si verificano.</span><span class="sxs-lookup"><span data-stu-id="f53f1-107">Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.</span></span>

## <a name="syntax"></a><span data-ttu-id="f53f1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f53f1-108">Syntax</span></span>


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f53f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f53f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f53f1-110">*MinWidth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f53f1-110">*minWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f53f1-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="f53f1-111">Type: **FLOAT\***</span></span>

<span data-ttu-id="f53f1-112">Larghezza minima.</span><span class="sxs-lookup"><span data-stu-id="f53f1-112">Minimum width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f53f1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f53f1-113">Return value</span></span>

<span data-ttu-id="f53f1-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f53f1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f53f1-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f53f1-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f53f1-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f53f1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f53f1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f53f1-117">Requirements</span></span>



| <span data-ttu-id="f53f1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f53f1-118">Requirement</span></span> | <span data-ttu-id="f53f1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f53f1-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f53f1-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="f53f1-120">Library</span></span><br/> | <dl> <span data-ttu-id="f53f1-121"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f53f1-121"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="f53f1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f53f1-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="f53f1-123"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f53f1-123"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f53f1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f53f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53f1-125">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="f53f1-125">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="f53f1-126">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="f53f1-126">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

