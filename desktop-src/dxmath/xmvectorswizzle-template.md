---
description: Swizzles un vettore.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Modello XMVectorSwizzle (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333228"
---
# <a name="xmvectorswizzle-template"></a><span data-ttu-id="d8d98-103">Modello XMVectorSwizzle</span><span class="sxs-lookup"><span data-stu-id="d8d98-103">XMVectorSwizzle template</span></span>

<span data-ttu-id="d8d98-104">Swizzles un vettore.</span><span class="sxs-lookup"><span data-stu-id="d8d98-104">Swizzles a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d98-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8d98-105">Syntax</span></span>

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="d8d98-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8d98-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="d8d98-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="d8d98-108">\[\]da Vector a Swizzle.</span><span class="sxs-lookup"><span data-stu-id="d8d98-108">\[in\] Vector to swizzle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8d98-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8d98-109">Return Value</span></span>

<span data-ttu-id="d8d98-110">Restituisce il [**XMVECTOR**](xmvector-data-type.md)swizzled.</span><span class="sxs-lookup"><span data-stu-id="d8d98-110">Returns the swizzled [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8d98-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8d98-111">Remarks</span></span>

<span data-ttu-id="d8d98-112">Questa funzione è una versione modello di [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) in cui gli argomenti di *swizzle \** sono valori di modello.</span><span class="sxs-lookup"><span data-stu-id="d8d98-112">This function is a template version of [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) where the *Swizzle\** arguments are template values.</span></span>

<span data-ttu-id="d8d98-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` e `XM_SWIZZLE_W` sono costanti che restituiscono rispettivamente 0, 1, 2 e 3 per l'uso con `XMVectorSwizzle` .</span><span class="sxs-lookup"><span data-stu-id="d8d98-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y`, `XM_SWIZZLE_Z`, and `XM_SWIZZLE_W` are constants which evaluate to 0, 1, 2, and 3 respectively for use with `XMVectorSwizzle`.</span></span> <span data-ttu-id="d8d98-114">Questo è identico a `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , `XM_PERMUTE_0Z` e `XM_PERMUTE_0W` .</span><span class="sxs-lookup"><span data-stu-id="d8d98-114">This is identical to `XM_PERMUTE_0X`, `XM_PERMUTE_0Y`, `XM_PERMUTE_0Z`, and `XM_PERMUTE_0W`.</span></span>

> [!Note]  
> <span data-ttu-id="d8d98-115">Il `XMVectorSwizzle` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="d8d98-115">The `XMVectorSwizzle` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="d8d98-116">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="d8d98-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="d8d98-117">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="d8d98-117">Platform Requirements</span></span>

<span data-ttu-id="d8d98-118">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d8d98-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="d8d98-119">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="d8d98-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8d98-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8d98-120">Requirements</span></span>



| <span data-ttu-id="d8d98-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8d98-121">Requirement</span></span> | <span data-ttu-id="d8d98-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d8d98-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d98-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8d98-123">Header</span></span><br/> | <dl> <span data-ttu-id="d8d98-124"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8d98-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8d98-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8d98-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d98-126">Funzioni del modello di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="d8d98-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="d8d98-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="d8d98-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> </dl>

 

 
