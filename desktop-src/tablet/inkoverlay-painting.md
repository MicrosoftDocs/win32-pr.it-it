---
description: Si verifica prima che l'oggetto InkOverlay o InkPicture abbia completato il ridisegno.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Evento InkOverlay. painting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529904"
---
# <a name="inkoverlaypainting-event"></a><span data-ttu-id="de492-103">Evento InkOverlay. painting</span><span class="sxs-lookup"><span data-stu-id="de492-103">InkOverlay.Painting event</span></span>

<span data-ttu-id="de492-104">Si verifica prima che l'oggetto [**InkOverlay**](inkoverlay-class.md) o [InkPicture](inkpicture-control-reference.md) abbia completato il ridisegno.</span><span class="sxs-lookup"><span data-stu-id="de492-104">Occurs before the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="de492-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de492-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="de492-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de492-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de492-107">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de492-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de492-108">Contesto di dispositivo in cui si verificherà il disegno.</span><span class="sxs-lookup"><span data-stu-id="de492-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="de492-109">*Rect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de492-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de492-110">Rettangolo da ridisegnare.</span><span class="sxs-lookup"><span data-stu-id="de492-110">The rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="de492-111">*Consenti* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="de492-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de492-112">Indica se si verificherà il ridisegno.</span><span class="sxs-lookup"><span data-stu-id="de492-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de492-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de492-113">Return value</span></span>

<span data-ttu-id="de492-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="de492-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de492-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="de492-115">Remarks</span></span>

<span data-ttu-id="de492-116">Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con ID DISPID \_ IOEPainting.</span><span class="sxs-lookup"><span data-stu-id="de492-116">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="de492-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de492-117">Requirements</span></span>



| <span data-ttu-id="de492-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="de492-118">Requirement</span></span> | <span data-ttu-id="de492-119">Valore</span><span class="sxs-lookup"><span data-stu-id="de492-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de492-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de492-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de492-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="de492-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="de492-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de492-122">Minimum supported server</span></span><br/> | <span data-ttu-id="de492-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="de492-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="de492-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de492-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="de492-125"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="de492-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="de492-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="de492-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="de492-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de492-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="de492-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de492-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de492-129">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="de492-129">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




