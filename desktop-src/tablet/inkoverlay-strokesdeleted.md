---
description: Si verifica dopo l'eliminazione dei tratti dalla proprietà Ink.
ms.assetid: 60ee8bbd-9230-4b6a-a4b0-4783195e3173
title: Evento InkOverlay. StrokesDeleted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc37b0de7f86f7d2b68df7074a0f3bb6c9e075e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231916"
---
# <a name="inkoverlaystrokesdeleted-event"></a><span data-ttu-id="c29ca-103">Evento InkOverlay. StrokesDeleted</span><span class="sxs-lookup"><span data-stu-id="c29ca-103">InkOverlay.StrokesDeleted event</span></span>

<span data-ttu-id="c29ca-104">Si verifica dopo l'eliminazione dei tratti dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="c29ca-104">Occurs after strokes have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c29ca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c29ca-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="c29ca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c29ca-106">Parameters</span></span>

<span data-ttu-id="c29ca-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="c29ca-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c29ca-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c29ca-108">Return value</span></span>

<span data-ttu-id="c29ca-109">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c29ca-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c29ca-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c29ca-110">Remarks</span></span>

<span data-ttu-id="c29ca-111">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c29ca-111">There is no event data.</span></span>

<span data-ttu-id="c29ca-112">Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con ID DISPID \_ IOEStrokesDeleted.</span><span class="sxs-lookup"><span data-stu-id="c29ca-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="c29ca-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c29ca-113">Requirements</span></span>



| <span data-ttu-id="c29ca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c29ca-114">Requirement</span></span> | <span data-ttu-id="c29ca-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c29ca-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c29ca-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c29ca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c29ca-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c29ca-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c29ca-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c29ca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c29ca-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c29ca-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c29ca-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c29ca-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c29ca-121"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c29ca-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c29ca-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="c29ca-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="c29ca-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c29ca-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c29ca-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c29ca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c29ca-125">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="c29ca-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="c29ca-126">[**\[Classe InkCollector/InkOverLay della proprietà Ink\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="c29ca-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

 




