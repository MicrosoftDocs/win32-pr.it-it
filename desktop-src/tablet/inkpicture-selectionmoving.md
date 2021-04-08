---
description: Si verifica quando la posizione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: Evento InkPicture. SelectionMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2dbc0064e22f21faf80d67f51ca1eeb58b6433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058197"
---
# <a name="inkpictureselectionmoving-event"></a><span data-ttu-id="b42b1-103">Evento InkPicture. SelectionMoving</span><span class="sxs-lookup"><span data-stu-id="b42b1-103">InkPicture.SelectionMoving event</span></span>

<span data-ttu-id="b42b1-104">Si verifica quando la posizione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="b42b1-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b42b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b42b1-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="b42b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b42b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b42b1-107">*CurSelectionRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b42b1-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b42b1-108">Rettangolo in cui la selezione viene spostata dopo l'evento **SelectionMoving** .</span><span class="sxs-lookup"><span data-stu-id="b42b1-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="b42b1-109">Questo rettangolo viene specificato nelle coordinate della finestra client, che consente scenari come la gestione delle proporzioni durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="b42b1-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b42b1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b42b1-110">Return value</span></span>

<span data-ttu-id="b42b1-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b42b1-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b42b1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b42b1-112">Remarks</span></span>

<span data-ttu-id="b42b1-113">Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOESelectionMoving.</span><span class="sxs-lookup"><span data-stu-id="b42b1-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="b42b1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b42b1-114">Requirements</span></span>



| <span data-ttu-id="b42b1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b42b1-115">Requirement</span></span> | <span data-ttu-id="b42b1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b42b1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b42b1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b42b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b42b1-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b42b1-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b42b1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b42b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b42b1-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b42b1-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b42b1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b42b1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b42b1-122"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b42b1-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b42b1-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b42b1-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b42b1-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b42b1-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b42b1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b42b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b42b1-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="b42b1-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="b42b1-127">[**Controllo InkPicture della proprietà Selection \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="b42b1-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="b42b1-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="b42b1-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




