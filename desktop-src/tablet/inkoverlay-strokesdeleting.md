---
description: Si verifica prima che i tratti vengano eliminati dalla proprietà Ink.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Evento InkOverlay. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968253"
---
# <a name="inkoverlaystrokesdeleting-event"></a><span data-ttu-id="a8f7f-103">Evento InkOverlay. StrokesDeleting</span><span class="sxs-lookup"><span data-stu-id="a8f7f-103">InkOverlay.StrokesDeleting event</span></span>

<span data-ttu-id="a8f7f-104">Si verifica prima che i tratti vengano eliminati dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="a8f7f-104">Occurs before strokes are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f7f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8f7f-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="a8f7f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8f7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f7f-107">*Tratti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8f7f-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f7f-108">Raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) eliminata quando viene generato l'evento **StrokesDeleting** .</span><span class="sxs-lookup"><span data-stu-id="a8f7f-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f7f-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8f7f-109">Return value</span></span>

<span data-ttu-id="a8f7f-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a8f7f-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f7f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8f7f-111">Remarks</span></span>

<span data-ttu-id="a8f7f-112">Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con ID DISPID \_ IOEStrokesDeleting.</span><span class="sxs-lookup"><span data-stu-id="a8f7f-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f7f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8f7f-113">Requirements</span></span>



| <span data-ttu-id="a8f7f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f7f-114">Requirement</span></span> | <span data-ttu-id="a8f7f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a8f7f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f7f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8f7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f7f-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a8f7f-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a8f7f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8f7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f7f-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a8f7f-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a8f7f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8f7f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8f7f-121"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a8f7f-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a8f7f-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="a8f7f-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8f7f-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f7f-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a8f7f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8f7f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f7f-125">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="a8f7f-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="a8f7f-126">[**\[Classe InkCollector/InkOverLay della proprietà Ink\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="a8f7f-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

