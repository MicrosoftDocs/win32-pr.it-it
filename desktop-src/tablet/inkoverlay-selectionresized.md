---
description: "Evento InkOverlay.SelectionResized: si verifica quando le dimensioni della selezione corrente sono state modificate, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o alla proprietà Selection."
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: Evento InkOverlay.SelectionResized (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f3dd3cf1bdda004733dde99bb66150710044310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116879"
---
# <a name="inkoverlayselectionresized-event"></a><span data-ttu-id="9e3aa-103">Evento InkOverlay.SelectionResized</span><span class="sxs-lookup"><span data-stu-id="9e3aa-103">InkOverlay.SelectionResized event</span></span>

<span data-ttu-id="9e3aa-104">Si verifica quando le dimensioni della selezione corrente sono cambiate, ad esempio tramite modifiche all'interfaccia utente, alle procedure taglia e incolla o [**alla proprietà**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) Selection.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e3aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e3aa-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="9e3aa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e3aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e3aa-107">*OldSelectionRect* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9e3aa-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e3aa-108">Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata così come esisteva prima della **generazione dell'evento SelectionResized.**</span><span class="sxs-lookup"><span data-stu-id="9e3aa-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="9e3aa-109">Questo rettangolo viene specificato nelle coordinate dello spazio input penna, che consente scenari di annullamento.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e3aa-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e3aa-110">Return value</span></span>

<span data-ttu-id="9e3aa-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e3aa-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e3aa-112">Remarks</span></span>

<span data-ttu-id="9e3aa-113">Questo metodo di evento è definito nelle interfacce \_ dispatch (dispatchinterface) IInkOverlayEvents e \_ IInkPictureEvents con ID \_ DISPID IOESelectionResized.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e3aa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e3aa-114">Requirements</span></span>



| <span data-ttu-id="9e3aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e3aa-115">Requirement</span></span> | <span data-ttu-id="9e3aa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9e3aa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e3aa-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e3aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9e3aa-118">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="9e3aa-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9e3aa-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e3aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9e3aa-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9e3aa-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9e3aa-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e3aa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e3aa-122"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="9e3aa-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9e3aa-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="9e3aa-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e3aa-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e3aa-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9e3aa-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e3aa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e3aa-126">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="9e3aa-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="9e3aa-127">**Proprietà Selection**</span><span class="sxs-lookup"><span data-stu-id="9e3aa-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="9e3aa-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="9e3aa-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

