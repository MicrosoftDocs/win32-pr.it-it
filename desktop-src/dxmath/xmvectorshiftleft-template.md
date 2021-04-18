---
description: Sposta un vettore lasciato da un numero specificato di elementi a 32 bit, riempiendo gli elementi sgomberati con elementi da un secondo vettore.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Modello XMVectorShiftLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329172"
---
# <a name="xmvectorshiftleft-template"></a><span data-ttu-id="3ab31-103">Modello XMVectorShiftLeft</span><span class="sxs-lookup"><span data-stu-id="3ab31-103">XMVectorShiftLeft template</span></span>

<span data-ttu-id="3ab31-104">Sposta un vettore lasciato da un numero specificato di elementi a 32 bit, riempiendo gli elementi sgomberati con elementi da un secondo vettore.</span><span class="sxs-lookup"><span data-stu-id="3ab31-104">Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ab31-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="3ab31-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ab31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ab31-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="3ab31-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="3ab31-108">\[in \] Vector per spostare verso sinistra.</span><span class="sxs-lookup"><span data-stu-id="3ab31-108">\[in\] Vector to shift left.</span></span>

</dd> <dt>

<span data-ttu-id="3ab31-109"><span id="V2"></span><span id="v2"></span>*V2*</span><span class="sxs-lookup"><span data-stu-id="3ab31-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="3ab31-110">\[in \] vector usato per compilare i componenti sgomberati di V1 dopo che è stato spostato verso sinistra.</span><span class="sxs-lookup"><span data-stu-id="3ab31-110">\[in\] Vector used to fill in the vacated components of V1 after it is shifted left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ab31-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ab31-111">Return Value</span></span>

<span data-ttu-id="3ab31-112">Restituisce l'oggetto spostato e compilato in [**XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ab31-112">Returns the shifted and filled in [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ab31-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ab31-113">Remarks</span></span>

<span data-ttu-id="3ab31-114">Questa funzione è una versione modello di [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) in cui l'argomento *elements* è un valore di modello.</span><span class="sxs-lookup"><span data-stu-id="3ab31-114">This function is a template version of [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="3ab31-115">Il `XMVectorShiftLeft` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="3ab31-115">The `XMVectorShiftLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="3ab31-116">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="3ab31-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="3ab31-117">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="3ab31-117">Platform Requirements</span></span>

<span data-ttu-id="3ab31-118">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3ab31-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="3ab31-119">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="3ab31-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ab31-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ab31-120">Requirements</span></span>



| <span data-ttu-id="3ab31-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ab31-121">Requirement</span></span> | <span data-ttu-id="3ab31-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3ab31-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab31-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ab31-123">Header</span></span><br/> | <dl> <span data-ttu-id="3ab31-124"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ab31-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ab31-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ab31-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab31-126">Funzioni del modello di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="3ab31-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="3ab31-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="3ab31-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="3ab31-128">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="3ab31-128">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="3ab31-129">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="3ab31-129">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> </dl>

 

 
