---
description: Si verifica dopo l'eliminazione degli oggetti IInkStrokeDisp dalla proprietà Ink.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: Evento InkPicture. StrokesDeleted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf98e51196d760f467d507c133429201883b340e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317933"
---
# <a name="inkpicturestrokesdeleted-event"></a><span data-ttu-id="8660b-103">Evento InkPicture. StrokesDeleted</span><span class="sxs-lookup"><span data-stu-id="8660b-103">InkPicture.StrokesDeleted event</span></span>

<span data-ttu-id="8660b-104">Si verifica dopo l'eliminazione degli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="8660b-104">Occurs after [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8660b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8660b-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="8660b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8660b-106">Parameters</span></span>

<span data-ttu-id="8660b-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="8660b-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8660b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8660b-108">Return value</span></span>

<span data-ttu-id="8660b-109">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8660b-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8660b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8660b-110">Remarks</span></span>

<span data-ttu-id="8660b-111">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="8660b-111">There is no event data.</span></span>

<span data-ttu-id="8660b-112">Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOEStrokesDeleted.</span><span class="sxs-lookup"><span data-stu-id="8660b-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="8660b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8660b-113">Requirements</span></span>



| <span data-ttu-id="8660b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8660b-114">Requirement</span></span> | <span data-ttu-id="8660b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8660b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8660b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8660b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8660b-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8660b-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8660b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8660b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8660b-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8660b-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8660b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8660b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8660b-121"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8660b-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8660b-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="8660b-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="8660b-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8660b-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8660b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8660b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8660b-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="8660b-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




