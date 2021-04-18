---
description: Ruota un vettore lasciato da un determinato numero di componenti a 32 bit e inserisce gli elementi selezionati di tale risultato in un altro vettore.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Modello XMVectorInsert (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329182"
---
# <a name="xmvectorinsert-template"></a><span data-ttu-id="b52a6-103">Modello XMVectorInsert</span><span class="sxs-lookup"><span data-stu-id="b52a6-103">XMVectorInsert template</span></span>

<span data-ttu-id="b52a6-104">Ruota un vettore lasciato da un determinato numero di componenti a 32 bit e inserisce gli elementi selezionati di tale risultato in un altro vettore.</span><span class="sxs-lookup"><span data-stu-id="b52a6-104">Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b52a6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b52a6-105">Syntax</span></span>

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a><span data-ttu-id="b52a6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b52a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b52a6-107"><span id="VD"></span><span id="vd"></span>*VD*</span><span class="sxs-lookup"><span data-stu-id="b52a6-107"><span id="VD"></span><span id="vd"></span>*VD*</span></span>
</dt> <dd>

<span data-ttu-id="b52a6-108">\[in \] vector da inserire in.</span><span class="sxs-lookup"><span data-stu-id="b52a6-108">\[in\] Vector to insert into.</span></span>

</dd> <dt>

<span data-ttu-id="b52a6-109"><span id="VS"></span><span id="vs"></span>*VS*</span><span class="sxs-lookup"><span data-stu-id="b52a6-109"><span id="VS"></span><span id="vs"></span>*VS*</span></span>
</dt> <dd>

<span data-ttu-id="b52a6-110">\[in \] Vector per ruotare verso sinistra.</span><span class="sxs-lookup"><span data-stu-id="b52a6-110">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b52a6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b52a6-111">Return Value</span></span>

<span data-ttu-id="b52a6-112">Restituisce il [**XMVECTOR**](xmvector-data-type.md) risultante dalla rotazione e dall'inserimento.</span><span class="sxs-lookup"><span data-stu-id="b52a6-112">Returns the [**XMVECTOR**](xmvector-data-type.md) that results from the rotation and insertion.</span></span>

## <a name="remarks"></a><span data-ttu-id="b52a6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b52a6-113">Remarks</span></span>

<span data-ttu-id="b52a6-114">Questa funzione è una versione modello di [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) in cui gli argomenti *Select \** sono valori di modello.</span><span class="sxs-lookup"><span data-stu-id="b52a6-114">This function is a template version of [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) where the *Select\** arguments are template values.</span></span>

<span data-ttu-id="b52a6-115">Per ottenere prestazioni ottimali, il risultato di `XMVectorInsert` deve essere assegnato nuovamente a *VD*.</span><span class="sxs-lookup"><span data-stu-id="b52a6-115">For best performance, the result of `XMVectorInsert` should be assigned back to *VD*.</span></span>

> [!Note]  
> <span data-ttu-id="b52a6-116">Il `XMVectorInsert` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="b52a6-116">The `XMVectorInsert` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="b52a6-117">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="b52a6-117">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="b52a6-118">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="b52a6-118">Platform Requirements</span></span>

<span data-ttu-id="b52a6-119">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b52a6-119">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="b52a6-120">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="b52a6-120">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="b52a6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b52a6-121">Requirements</span></span>



| <span data-ttu-id="b52a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b52a6-122">Requirement</span></span> | <span data-ttu-id="b52a6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b52a6-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b52a6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b52a6-124">Header</span></span><br/> | <dl> <span data-ttu-id="b52a6-125"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="b52a6-125"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b52a6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b52a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52a6-127">Funzioni del modello di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="b52a6-127">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="b52a6-128">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="b52a6-128">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="b52a6-129">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="b52a6-129">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="b52a6-130">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="b52a6-130">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="b52a6-131">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="b52a6-131">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
