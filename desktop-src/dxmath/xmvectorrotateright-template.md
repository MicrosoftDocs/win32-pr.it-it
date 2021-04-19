---
description: Ruota il vettore a destra di un numero specificato di elementi a 32 bit.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Modello XMVectorRotateRight (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333229"
---
# <a name="xmvectorrotateright-template"></a><span data-ttu-id="20af0-103">Modello XMVectorRotateRight</span><span class="sxs-lookup"><span data-stu-id="20af0-103">XMVectorRotateRight template</span></span>

<span data-ttu-id="20af0-104">Ruota il vettore a destra di un numero specificato di elementi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="20af0-104">Rotates the vector right by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="20af0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20af0-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="20af0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20af0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20af0-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="20af0-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="20af0-108">\[in \] Vector per ruotare a destra.</span><span class="sxs-lookup"><span data-stu-id="20af0-108">\[in\] Vector to rotate right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20af0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20af0-109">Return Value</span></span>

<span data-ttu-id="20af0-110">Restituisce il [**XMVECTOR**](xmvector-data-type.md)ruotato.</span><span class="sxs-lookup"><span data-stu-id="20af0-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20af0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="20af0-111">Remarks</span></span>

<span data-ttu-id="20af0-112">Questa funzione è una versione modello di [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) in cui l'argomento *elements* è un valore di modello.</span><span class="sxs-lookup"><span data-stu-id="20af0-112">This function is a template version of [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="20af0-113">Il `XMVectorRotateRight` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="20af0-113">The `XMVectorRotateRight` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="20af0-114">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="20af0-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="20af0-115">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="20af0-115">Platform Requirements</span></span>

<span data-ttu-id="20af0-116">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="20af0-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="20af0-117">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="20af0-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="20af0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20af0-118">Requirements</span></span>



| <span data-ttu-id="20af0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="20af0-119">Requirement</span></span> | <span data-ttu-id="20af0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="20af0-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20af0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20af0-121">Header</span></span><br/> | <dl> <span data-ttu-id="20af0-122"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="20af0-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20af0-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20af0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20af0-124">Funzioni del modello di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="20af0-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="20af0-125">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="20af0-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="20af0-126">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="20af0-126">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="20af0-127">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="20af0-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
