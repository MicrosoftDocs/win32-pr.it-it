---
description: Si verifica in seguito alla modifica della dimensione della selezione corrente, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: Evento InkOverlay. SelectionResized (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf9cbb01821756d830b7c0a24adc55dad11b403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233551"
---
# <a name="inkoverlayselectionresized-event"></a><span data-ttu-id="f7b22-103">Evento InkOverlay. SelectionResized</span><span class="sxs-lookup"><span data-stu-id="f7b22-103">InkOverlay.SelectionResized event</span></span>

<span data-ttu-id="f7b22-104">Si verifica in seguito alla modifica della dimensione della selezione corrente, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="f7b22-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b22-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7b22-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="f7b22-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7b22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b22-107">*OldSelectionRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7b22-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b22-108">Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata esistente prima dell'evento **SelectionResized** generato.</span><span class="sxs-lookup"><span data-stu-id="f7b22-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="f7b22-109">Questo rettangolo viene specificato nelle coordinate dello spazio di input penna, che consente scenari di annullamento.</span><span class="sxs-lookup"><span data-stu-id="f7b22-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b22-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7b22-110">Return value</span></span>

<span data-ttu-id="f7b22-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f7b22-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b22-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7b22-112">Remarks</span></span>

<span data-ttu-id="f7b22-113">Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con ID DISPID \_ IOESelectionResized.</span><span class="sxs-lookup"><span data-stu-id="f7b22-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b22-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7b22-114">Requirements</span></span>



| <span data-ttu-id="f7b22-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b22-115">Requirement</span></span> | <span data-ttu-id="f7b22-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f7b22-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b22-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7b22-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b22-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f7b22-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f7b22-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7b22-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b22-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f7b22-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f7b22-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7b22-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b22-122"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f7b22-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f7b22-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f7b22-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7b22-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b22-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f7b22-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7b22-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b22-126">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="f7b22-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="f7b22-127">**Proprietà Selection**</span><span class="sxs-lookup"><span data-stu-id="f7b22-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="f7b22-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="f7b22-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

