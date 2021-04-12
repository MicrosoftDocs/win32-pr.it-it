---
description: Si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: Evento InkPicture. SelectionMoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25810b87d5a0a3554c46b1a3869bb9b6c88d2fb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346876"
---
# <a name="inkpictureselectionmoved-event"></a><span data-ttu-id="5390c-103">Evento InkPicture. SelectionMoved</span><span class="sxs-lookup"><span data-stu-id="5390c-103">InkPicture.SelectionMoved event</span></span>

<span data-ttu-id="5390c-104">Si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="5390c-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5390c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5390c-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="5390c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5390c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5390c-107">*OldSelectionRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5390c-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5390c-108">Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata esistente prima dell'evento **SelectionMoved** generato.</span><span class="sxs-lookup"><span data-stu-id="5390c-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="5390c-109">Questo rettangolo viene specificato nelle coordinate dello spazio di input penna, che consente scenari di annullamento.</span><span class="sxs-lookup"><span data-stu-id="5390c-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5390c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5390c-110">Return value</span></span>

<span data-ttu-id="5390c-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5390c-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5390c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5390c-112">Remarks</span></span>

<span data-ttu-id="5390c-113">Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOESelectionMoved.</span><span class="sxs-lookup"><span data-stu-id="5390c-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="5390c-114">Per ottenere il nuovo rettangolo di delimitazione della raccolta di tratti spostati, chiamare il metodo [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="5390c-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5390c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5390c-115">Requirements</span></span>



| <span data-ttu-id="5390c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5390c-116">Requirement</span></span> | <span data-ttu-id="5390c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5390c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5390c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5390c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5390c-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5390c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5390c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5390c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5390c-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5390c-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5390c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5390c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5390c-123"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5390c-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5390c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="5390c-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="5390c-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5390c-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5390c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5390c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5390c-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="5390c-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="5390c-128">[**Controllo InkPicture della proprietà Selection \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="5390c-128">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="5390c-129">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="5390c-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

