---
description: Si verifica quando si fa doppio clic sull'oggetto InkCollector o InkOverlay.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Evento InkOverlay. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4baddc89e309b7d64ba2294827b58956b3e6c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233184"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="4682a-103">InkOverlay. DoubleClick (evento)</span><span class="sxs-lookup"><span data-stu-id="4682a-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="4682a-104">Si verifica quando si fa doppio clic sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="4682a-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="4682a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4682a-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="4682a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4682a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4682a-107">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4682a-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4682a-108">Indica se l'evento deve essere annullato per il controllo padre.</span><span class="sxs-lookup"><span data-stu-id="4682a-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4682a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4682a-109">Return value</span></span>

<span data-ttu-id="4682a-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4682a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4682a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4682a-111">Remarks</span></span>

<span data-ttu-id="4682a-112">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEDblClick.</span><span class="sxs-lookup"><span data-stu-id="4682a-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="4682a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4682a-113">Requirements</span></span>



| <span data-ttu-id="4682a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4682a-114">Requirement</span></span> | <span data-ttu-id="4682a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4682a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4682a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4682a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4682a-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4682a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4682a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4682a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4682a-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4682a-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4682a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4682a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4682a-121"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4682a-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4682a-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="4682a-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="4682a-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4682a-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4682a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4682a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4682a-125">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="4682a-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




