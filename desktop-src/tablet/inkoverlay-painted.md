---
description: Si verifica quando l'oggetto InkOverlay o il controllo InkPicture ha completato il ridisegno.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Evento InkOverlay. Painted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485764"
---
# <a name="inkoverlaypainted-event"></a><span data-ttu-id="7b482-103">Evento InkOverlay. Painted</span><span class="sxs-lookup"><span data-stu-id="7b482-103">InkOverlay.Painted event</span></span>

<span data-ttu-id="7b482-104">Si verifica quando l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) ha completato il ridisegno.</span><span class="sxs-lookup"><span data-stu-id="7b482-104">Occurs when the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b482-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b482-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="7b482-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b482-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b482-107">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b482-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b482-108">Contesto di dispositivo in cui si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="7b482-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7b482-109">*Rect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b482-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b482-110">[**InkRectangle**](inkrectangle-class.md) ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="7b482-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b482-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b482-111">Return value</span></span>

<span data-ttu-id="7b482-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7b482-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b482-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b482-113">Remarks</span></span>

<span data-ttu-id="7b482-114">Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con ID DISPID \_ IOEPainted.</span><span class="sxs-lookup"><span data-stu-id="7b482-114">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b482-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b482-115">Requirements</span></span>



| <span data-ttu-id="7b482-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b482-116">Requirement</span></span> | <span data-ttu-id="7b482-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7b482-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b482-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b482-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b482-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b482-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7b482-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b482-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b482-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7b482-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7b482-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b482-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b482-123"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b482-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b482-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="7b482-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b482-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b482-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7b482-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b482-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b482-127">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="7b482-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




