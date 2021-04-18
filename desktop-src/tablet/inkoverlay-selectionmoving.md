---
description: Si verifica quando la posizione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: Evento InkOverlay. SelectionMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afc77198a6a7228e44b3f2bad8015c25a939812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316841"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="4a540-103">Evento InkOverlay. SelectionMoving</span><span class="sxs-lookup"><span data-stu-id="4a540-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="4a540-104">Si verifica quando la posizione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="4a540-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a540-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a540-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="4a540-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a540-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a540-107">*CurSelectionRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a540-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a540-108">Rettangolo in cui la selezione viene spostata dopo l'evento **SelectionMoving** .</span><span class="sxs-lookup"><span data-stu-id="4a540-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="4a540-109">Questo rettangolo viene specificato nelle coordinate della finestra client, che consente scenari come la gestione delle proporzioni durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="4a540-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a540-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a540-110">Return value</span></span>

<span data-ttu-id="4a540-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4a540-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a540-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a540-112">Remarks</span></span>

<span data-ttu-id="4a540-113">Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con un ID disattivato DISPID \_ IOESelectionMoving.</span><span class="sxs-lookup"><span data-stu-id="4a540-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a540-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a540-114">Requirements</span></span>



| <span data-ttu-id="4a540-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a540-115">Requirement</span></span> | <span data-ttu-id="4a540-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4a540-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a540-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a540-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a540-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4a540-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4a540-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a540-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a540-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4a540-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4a540-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a540-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a540-122"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4a540-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4a540-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a540-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a540-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a540-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4a540-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a540-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a540-126">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="4a540-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="4a540-127">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="4a540-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="4a540-128">**Proprietà Selection**</span><span class="sxs-lookup"><span data-stu-id="4a540-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="4a540-129">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="4a540-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




