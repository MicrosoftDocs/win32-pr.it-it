---
title: Funzione D2DGetInput (D2d1effecthelpers. h)
description: Restituisce il colore dell'input N nella coordinata di input. Disponibile solo per gli input semplici.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- Direct2D funzione D2DGetInput
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331663"
---
# <a name="d2dgetinput-function"></a><span data-ttu-id="520c6-105">D2DGetInput (funzione)</span><span class="sxs-lookup"><span data-stu-id="520c6-105">D2DGetInput function</span></span>

<span data-ttu-id="520c6-106">Restituisce il colore dell'input N nella coordinata di input.</span><span class="sxs-lookup"><span data-stu-id="520c6-106">Returns the color of input N at the input coordinate.</span></span> <span data-ttu-id="520c6-107">Disponibile solo per gli input semplici.</span><span class="sxs-lookup"><span data-stu-id="520c6-107">Only available for simple inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="520c6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="520c6-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="520c6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="520c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="520c6-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="520c6-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520c6-111">Numero di input.</span><span class="sxs-lookup"><span data-stu-id="520c6-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="520c6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="520c6-112">Return value</span></span>

<span data-ttu-id="520c6-113">La funzione restituisce un **float4** contenente il colore RGBA nel formato inputn.</span><span class="sxs-lookup"><span data-stu-id="520c6-113">The function returns a **float4**, containing the RGBA color in the format INPUTN.</span></span>

## <a name="remarks"></a><span data-ttu-id="520c6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="520c6-114">Remarks</span></span>

<span data-ttu-id="520c6-115">Nell'esempio seguente viene illustrata la funzione utilizzata come parte di un effetto composito aritmetico.</span><span class="sxs-lookup"><span data-stu-id="520c6-115">The following example shows the function being used as part of an arithmetic composite effect.</span></span>

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

<span data-ttu-id="520c6-116">Per un altro esempio dell'uso di questa funzione, vedere anche la sezione Osservazioni per la [ \_ \_ voce D2D PS](d2d-ps-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="520c6-116">Also, refer to the remarks for [D2D\_PS\_ENTRY](d2d-ps-entry.md) for another example of the use of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="520c6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="520c6-117">Requirements</span></span>



| <span data-ttu-id="520c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="520c6-118">Requirement</span></span> | <span data-ttu-id="520c6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="520c6-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="520c6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="520c6-120">Header</span></span><br/> | <dl> <span data-ttu-id="520c6-121"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="520c6-121"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="520c6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="520c6-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="520c6-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="520c6-123"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="520c6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="520c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520c6-125">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="520c6-125">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="520c6-126">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="520c6-126">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





