---
description: Si verifica dopo che il controllo InkPicture è stato ridimensionato, in particolare, dopo la modifica del valore della proprietà Width o Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Evento InkPicture. SizeChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968420"
---
# <a name="inkpicturesizechanged-event"></a><span data-ttu-id="67b61-103">Evento InkPicture. SizeChanged</span><span class="sxs-lookup"><span data-stu-id="67b61-103">InkPicture.SizeChanged event</span></span>

<span data-ttu-id="67b61-104">Si verifica dopo che il controllo [InkPicture](inkpicture-control-reference.md) è stato ridimensionato, in particolare, dopo la modifica del valore della proprietà [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .</span><span class="sxs-lookup"><span data-stu-id="67b61-104">Occurs after the [InkPicture](inkpicture-control-reference.md) control has been resized, specifically, after the [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) or [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) property value changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b61-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67b61-105">Syntax</span></span>


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="67b61-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="67b61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b61-107">A *sinistra* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67b61-107">*Left* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67b61-108">Coordinata x del lato sinistro del controllo [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="67b61-108">The x-coordinate of the left side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="67b61-109">In *alto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67b61-109">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67b61-110">Coordinata y della parte superiore del controllo [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="67b61-110">The y-coordinate of the top of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="67b61-111">A *destra* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67b61-111">*Right* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67b61-112">Coordinata x del lato destro del controllo [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="67b61-112">The x-coordinate of the right side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="67b61-113">In *basso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67b61-113">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67b61-114">Coordinata y della parte inferiore del controllo [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="67b61-114">The y-coordinate of the bottom of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67b61-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67b61-115">Return value</span></span>

<span data-ttu-id="67b61-116">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="67b61-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67b61-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="67b61-117">Remarks</span></span>

<span data-ttu-id="67b61-118">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="67b61-118">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="67b61-119">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPESizeChanged.</span><span class="sxs-lookup"><span data-stu-id="67b61-119">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="67b61-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67b61-120">Requirements</span></span>



| <span data-ttu-id="67b61-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="67b61-121">Requirement</span></span> | <span data-ttu-id="67b61-122">Valore</span><span class="sxs-lookup"><span data-stu-id="67b61-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67b61-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67b61-123">Minimum supported client</span></span><br/> | <span data-ttu-id="67b61-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="67b61-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="67b61-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67b61-125">Minimum supported server</span></span><br/> | <span data-ttu-id="67b61-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="67b61-126">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="67b61-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67b61-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="67b61-128"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="67b61-128"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="67b61-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="67b61-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="67b61-130"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67b61-130"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="67b61-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67b61-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b61-132">InkPicture</span><span class="sxs-lookup"><span data-stu-id="67b61-132">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

