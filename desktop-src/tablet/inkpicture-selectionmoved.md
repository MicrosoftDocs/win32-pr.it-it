---
description: "Evento InkPicture.SelectionMoved: si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite modifiche all'interfaccia utente, procedure taglia e incolla o proprietà Selection."
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: Evento InkPicture.SelectionMoved (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2006b2580e8732c90187b265576b217cdbad9b02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086449"
---
# <a name="inkpictureselectionmoved-event"></a><span data-ttu-id="4fd9e-103">Evento InkPicture.SelectionMoved</span><span class="sxs-lookup"><span data-stu-id="4fd9e-103">InkPicture.SelectionMoved event</span></span>

<span data-ttu-id="4fd9e-104">Si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite modifiche all'interfaccia utente, procedure taglia e incolla o proprietà [**Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="4fd9e-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fd9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fd9e-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="4fd9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fd9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fd9e-107">*OldSelectionRect* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4fd9e-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd9e-108">Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata esistente prima che venga generato **l'evento SelectionMoved.**</span><span class="sxs-lookup"><span data-stu-id="4fd9e-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="4fd9e-109">Questo rettangolo viene specificato nelle coordinate dello spazio input penna, che consente scenari di annullamento.</span><span class="sxs-lookup"><span data-stu-id="4fd9e-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fd9e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4fd9e-110">Return value</span></span>

<span data-ttu-id="4fd9e-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4fd9e-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fd9e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fd9e-112">Remarks</span></span>

<span data-ttu-id="4fd9e-113">Questo metodo di evento è definito nelle interfacce di solo invio **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ DISPID IOESelectionMoved.</span><span class="sxs-lookup"><span data-stu-id="4fd9e-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="4fd9e-114">Per ottenere il nuovo rettangolo di delimitazione della raccolta di tratti spostati, chiama il [**metodo Selection.GetBoundingBox.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)</span><span class="sxs-lookup"><span data-stu-id="4fd9e-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fd9e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fd9e-115">Requirements</span></span>



| <span data-ttu-id="4fd9e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fd9e-116">Requirement</span></span> | <span data-ttu-id="4fd9e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4fd9e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd9e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fd9e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd9e-119">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="4fd9e-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4fd9e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fd9e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd9e-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4fd9e-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4fd9e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4fd9e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fd9e-123"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="4fd9e-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4fd9e-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="4fd9e-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fd9e-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fd9e-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4fd9e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fd9e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd9e-127">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="4fd9e-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="4fd9e-128">[**Controllo \[ InkPicture della proprietà Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="4fd9e-128">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="4fd9e-129">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="4fd9e-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

