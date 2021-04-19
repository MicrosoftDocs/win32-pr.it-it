---
description: Si verifica in seguito alla modifica della dimensione della selezione corrente, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: Evento InkPicture. SelectionResized (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90e04533e3551fd4e1ba4ac661d8060377e6d06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317942"
---
# <a name="inkpictureselectionresized-event"></a><span data-ttu-id="47932-103">Evento InkPicture. SelectionResized</span><span class="sxs-lookup"><span data-stu-id="47932-103">InkPicture.SelectionResized event</span></span>

<span data-ttu-id="47932-104">Si verifica in seguito alla modifica della dimensione della selezione corrente, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="47932-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="47932-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47932-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="47932-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="47932-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47932-107">*OldSelectionRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47932-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47932-108">Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata esistente prima dell'evento **SelectionResized** generato.</span><span class="sxs-lookup"><span data-stu-id="47932-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="47932-109">Questo rettangolo viene specificato nelle coordinate dello spazio di input penna, che consente scenari di annullamento.</span><span class="sxs-lookup"><span data-stu-id="47932-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47932-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47932-110">Return value</span></span>

<span data-ttu-id="47932-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="47932-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47932-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="47932-112">Remarks</span></span>

<span data-ttu-id="47932-113">Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOESelectionResized.</span><span class="sxs-lookup"><span data-stu-id="47932-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="47932-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47932-114">Requirements</span></span>



| <span data-ttu-id="47932-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="47932-115">Requirement</span></span> | <span data-ttu-id="47932-116">Valore</span><span class="sxs-lookup"><span data-stu-id="47932-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47932-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47932-117">Minimum supported client</span></span><br/> | <span data-ttu-id="47932-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="47932-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="47932-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47932-119">Minimum supported server</span></span><br/> | <span data-ttu-id="47932-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="47932-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="47932-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47932-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="47932-122"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="47932-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="47932-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="47932-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="47932-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47932-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="47932-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47932-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47932-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="47932-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="47932-127">[**Controllo InkPicture della proprietà Selection \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="47932-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="47932-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="47932-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

