---
description: Si verifica prima dell'eliminazione degli oggetti IInkStrokeDisp dalla proprietà Ink.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: Evento InkPicture. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057990"
---
# <a name="inkpicturestrokesdeleting-event"></a><span data-ttu-id="60142-103">Evento InkPicture. StrokesDeleting</span><span class="sxs-lookup"><span data-stu-id="60142-103">InkPicture.StrokesDeleting event</span></span>

<span data-ttu-id="60142-104">Si verifica prima dell'eliminazione degli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="60142-104">Occurs before [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="60142-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60142-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="60142-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60142-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60142-107">*Tratti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60142-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60142-108">Raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) eliminata quando viene generato l'evento **StrokesDeleting** .</span><span class="sxs-lookup"><span data-stu-id="60142-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60142-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60142-109">Return value</span></span>

<span data-ttu-id="60142-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="60142-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60142-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="60142-111">Remarks</span></span>

<span data-ttu-id="60142-112">Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOEStrokesDeleting.</span><span class="sxs-lookup"><span data-stu-id="60142-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="60142-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60142-113">Requirements</span></span>



| <span data-ttu-id="60142-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="60142-114">Requirement</span></span> | <span data-ttu-id="60142-115">Valore</span><span class="sxs-lookup"><span data-stu-id="60142-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60142-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60142-116">Minimum supported client</span></span><br/> | <span data-ttu-id="60142-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="60142-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="60142-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60142-118">Minimum supported server</span></span><br/> | <span data-ttu-id="60142-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="60142-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="60142-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60142-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="60142-121"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="60142-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="60142-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="60142-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="60142-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60142-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="60142-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60142-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60142-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="60142-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

