---
description: Permuta i componenti di due vettori per creare un nuovo vettore.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Modello XMVectorPermute (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333231"
---
# <a name="xmvectorpermute-template"></a><span data-ttu-id="e4f7a-103">Modello XMVectorPermute</span><span class="sxs-lookup"><span data-stu-id="e4f7a-103">XMVectorPermute template</span></span>

<span data-ttu-id="e4f7a-104">Permuta i componenti di due vettori per creare un nuovo vettore.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-104">Permutes the components of two vectors to create a new vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f7a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4f7a-105">Syntax</span></span>

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="e4f7a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4f7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4f7a-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="e4f7a-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="e4f7a-108">\[nel \] primo vettore.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-108">\[in\] First vector.</span></span>

</dd> <dt>

<span data-ttu-id="e4f7a-109"><span id="V2"></span><span id="v2"></span>*V2*</span><span class="sxs-lookup"><span data-stu-id="e4f7a-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="e4f7a-110">\[nel \] secondo vettore.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-110">\[in\] Second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4f7a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4f7a-111">Return Value</span></span>

<span data-ttu-id="e4f7a-112">Restituisce il vettore permutati risultante dalla combinazione dei vettori di origine.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-112">Returns the permuted vector that resulted from combining the source vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4f7a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4f7a-113">Remarks</span></span>

<span data-ttu-id="e4f7a-114">Se tutti i 4 indici fanno riferimento solo a un singolo vettore (ovvero sono tutti compresi nell'intervallo 0-3 o tutti nell'intervallo 4-7), usare [**XMVectorSwizzle**](xmvectorswizzle-template.md) invece per ottenere prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-114">If all 4 indices reference only a single vector (i.e. they are all in the range 0-3 or all in the range 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) instead for better performance.</span></span>

<span data-ttu-id="e4f7a-115">Nota la libreria usa le specializzazioni dei modelli in alcune piattaforme per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-115">Note the library makes use of template specializations on some platforms to improve performance.</span></span> <span data-ttu-id="e4f7a-116">Non ogni possibile mirror case è implementato per questi casi speciali, quindi preferisce permuta in cui l'elemento X del vettore risultante deriva dal parametro V1 anziché dal parametro V2.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-116">Not every possible mirror case is implemented for these special cases, so prefer permutes where the X element of the resulting vector comes from the V1 parameter rather than the V2 parameter.</span></span> <span data-ttu-id="e4f7a-117">Si preferisce, ad esempio, usare `XMVectorPermute<0,1,4,5>(A,B);` a `XMVectorPermute(4,5,0,1)(B,A);` .</span><span class="sxs-lookup"><span data-stu-id="e4f7a-117">For example, prefer using `XMVectorPermute<0,1,4,5>(A,B);` to `XMVectorPermute(4,5,0,1)(B,A);`.</span></span>

<span data-ttu-id="e4f7a-118">Questa funzione è una versione modello di [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) in cui gli argomenti di *permute \** sono valori di modello.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-118">This function is a template version of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) where the *Permute\** arguments are template values.</span></span>

<span data-ttu-id="e4f7a-119">Le [costanti \_ permute \_ XM](ovw-xnamath-reference-constants.md) vengono fornite da usare come valori di input per *PermuteX*,*PermuteY*,*PermuteZ* e *PermuteW*.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-119">The [XM\_PERMUTE\_](ovw-xnamath-reference-constants.md) constants are provided to use as input values for *PermuteX*,*PermuteY*,*PermuteZ*, and *PermuteW*.</span></span>

> [!Note]  
> <span data-ttu-id="e4f7a-120">Il `XMVectorPermute` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-120">The `XMVectorPermute` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="e4f7a-121">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="e4f7a-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="e4f7a-122">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="e4f7a-122">Platform Requirements</span></span>

<span data-ttu-id="e4f7a-123">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="e4f7a-124">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="e4f7a-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f7a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4f7a-125">Requirements</span></span>



| <span data-ttu-id="e4f7a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4f7a-126">Requirement</span></span> | <span data-ttu-id="e4f7a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e4f7a-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f7a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4f7a-128">Header</span></span><br/> | <dl> <span data-ttu-id="e4f7a-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4f7a-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4f7a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4f7a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f7a-131">Funzioni del modello di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="e4f7a-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="e4f7a-132">**XMVectorSwizzle**</span><span class="sxs-lookup"><span data-stu-id="e4f7a-132">**XMVectorSwizzle**</span></span>](xmvectorswizzle-template.md)
</dt> </dl>

 

 
