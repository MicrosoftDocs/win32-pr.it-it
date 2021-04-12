---
description: Si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: Evento InkOverlay. SelectionMoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f254b5e3ae3c23f50b12c097608946aad3b3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348666"
---
# <a name="inkoverlayselectionmoved-event"></a><span data-ttu-id="1cc20-103">Evento InkOverlay. SelectionMoved</span><span class="sxs-lookup"><span data-stu-id="1cc20-103">InkOverlay.SelectionMoved event</span></span>

<span data-ttu-id="1cc20-104">Si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="1cc20-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc20-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cc20-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="1cc20-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cc20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc20-107">*OldSelectionRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cc20-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc20-108">Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata esistente prima dell'evento **SelectionMoved** generato.</span><span class="sxs-lookup"><span data-stu-id="1cc20-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="1cc20-109">Questo rettangolo viene specificato nelle coordinate dello spazio di input penna, che consente scenari di annullamento.</span><span class="sxs-lookup"><span data-stu-id="1cc20-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc20-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cc20-110">Return value</span></span>

<span data-ttu-id="1cc20-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1cc20-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc20-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cc20-112">Remarks</span></span>

<span data-ttu-id="1cc20-113">Il metodo dell'evento TThis è definito nelle \_ \_ interfacce di sola invio IInkOverlayEvents e IInkPictureEvents (dispinterfaces) con un ID di DISPID \_ IOESelectionMoved.</span><span class="sxs-lookup"><span data-stu-id="1cc20-113">TThis event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="1cc20-114">Per ottenere il nuovo rettangolo di delimitazione della raccolta di tratti spostati, chiamare il metodo [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="1cc20-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc20-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cc20-115">Requirements</span></span>



| <span data-ttu-id="1cc20-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc20-116">Requirement</span></span> | <span data-ttu-id="1cc20-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1cc20-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc20-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cc20-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc20-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1cc20-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1cc20-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cc20-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc20-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1cc20-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1cc20-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cc20-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cc20-123"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1cc20-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1cc20-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="1cc20-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cc20-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cc20-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1cc20-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cc20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc20-127">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="1cc20-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="1cc20-128">**Proprietà Selection**</span><span class="sxs-lookup"><span data-stu-id="1cc20-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="1cc20-129">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="1cc20-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

