---
description: "Evento InkCollector.DoubleClick: si verifica quando si fa doppio clic sull'oggetto InkCollector o InkOverlay."
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Evento InkCollector.DoubleClick (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51c3fef9ee999bbe2701da64e09a360f07db345
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110209"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="b83e7-103">Evento InkCollector.DoubleClick</span><span class="sxs-lookup"><span data-stu-id="b83e7-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="b83e7-104">Si verifica quando si fa doppio clic sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay.**](inkoverlay-class.md)</span><span class="sxs-lookup"><span data-stu-id="b83e7-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="b83e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b83e7-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="b83e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b83e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b83e7-107">*Annulla* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b83e7-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b83e7-108">**VARIANT \_ TRUE** per annullare l'evento per il controllo padre. in caso contrario, **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="b83e7-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b83e7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b83e7-109">Return value</span></span>

<span data-ttu-id="b83e7-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b83e7-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b83e7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b83e7-111">Remarks</span></span>

<span data-ttu-id="b83e7-112">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEDblClick.</span><span class="sxs-lookup"><span data-stu-id="b83e7-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="b83e7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b83e7-113">Requirements</span></span>



| <span data-ttu-id="b83e7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b83e7-114">Requirement</span></span> | <span data-ttu-id="b83e7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b83e7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b83e7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b83e7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b83e7-117">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="b83e7-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b83e7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b83e7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b83e7-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b83e7-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b83e7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b83e7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b83e7-121"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="b83e7-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b83e7-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="b83e7-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="b83e7-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b83e7-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b83e7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b83e7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b83e7-125">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="b83e7-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 




