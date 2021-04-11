---
description: Si verifica quando la dimensione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: Evento InkOverlay. SelectionResizing (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7debb9461aae39c0549bce863a0513b86c53ffa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233179"
---
# <a name="inkoverlayselectionresizing-event"></a><span data-ttu-id="02178-103">Evento InkOverlay. SelectionResizing</span><span class="sxs-lookup"><span data-stu-id="02178-103">InkOverlay.SelectionResizing event</span></span>

<span data-ttu-id="02178-104">Si verifica quando la dimensione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="02178-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="02178-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02178-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="02178-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02178-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02178-107">*CurSelectionRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02178-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02178-108">Rettangolo di delimitazione della selezione dopo l'evento **SelectionResizing** .</span><span class="sxs-lookup"><span data-stu-id="02178-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="02178-109">Questo rettangolo viene specificato nelle coordinate della finestra client, che consente scenari come la gestione delle proporzioni durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="02178-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02178-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02178-110">Return value</span></span>

<span data-ttu-id="02178-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="02178-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02178-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="02178-112">Remarks</span></span>

<span data-ttu-id="02178-113">Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con ID DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="02178-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="02178-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02178-114">Requirements</span></span>



| <span data-ttu-id="02178-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="02178-115">Requirement</span></span> | <span data-ttu-id="02178-116">Valore</span><span class="sxs-lookup"><span data-stu-id="02178-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02178-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02178-117">Minimum supported client</span></span><br/> | <span data-ttu-id="02178-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="02178-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="02178-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02178-119">Minimum supported server</span></span><br/> | <span data-ttu-id="02178-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="02178-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="02178-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02178-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="02178-122"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="02178-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="02178-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="02178-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="02178-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02178-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="02178-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02178-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02178-126">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="02178-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="02178-127">**Proprietà Selection**</span><span class="sxs-lookup"><span data-stu-id="02178-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="02178-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="02178-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




