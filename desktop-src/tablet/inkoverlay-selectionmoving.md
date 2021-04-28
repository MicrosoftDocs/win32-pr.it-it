---
description: "Evento InkOverlay.SelectionMoving: si verifica quando la posizione della selezione corrente sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, procedure taglia e incolla o proprietà Selection."
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: Evento InkOverlay.SelectionMoving (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ee4784e6b4c475c30d9b2a3ab30fe166ea3d67d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086699"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="da75a-103">Evento InkOverlay.SelectionMoving</span><span class="sxs-lookup"><span data-stu-id="da75a-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="da75a-104">Si verifica quando la posizione della selezione corrente sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, procedure taglia e incolla o proprietà [**Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)</span><span class="sxs-lookup"><span data-stu-id="da75a-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="da75a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da75a-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="da75a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da75a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da75a-107">*CurSelectionRect* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="da75a-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da75a-108">Rettangolo in cui viene spostata la selezione dopo **l'evento SelectionMoving.**</span><span class="sxs-lookup"><span data-stu-id="da75a-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="da75a-109">Questo rettangolo viene specificato nelle coordinate della finestra client, che consente scenari come la gestione delle proporzioni durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="da75a-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da75a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da75a-110">Return value</span></span>

<span data-ttu-id="da75a-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="da75a-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da75a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="da75a-112">Remarks</span></span>

<span data-ttu-id="da75a-113">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID off DISPID \_ IOESelectionMoving.</span><span class="sxs-lookup"><span data-stu-id="da75a-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="da75a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da75a-114">Requirements</span></span>



| <span data-ttu-id="da75a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="da75a-115">Requirement</span></span> | <span data-ttu-id="da75a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="da75a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da75a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da75a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="da75a-118">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="da75a-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="da75a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da75a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="da75a-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="da75a-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="da75a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da75a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="da75a-122"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="da75a-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="da75a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="da75a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="da75a-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da75a-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="da75a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da75a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da75a-126">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="da75a-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="da75a-127">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="da75a-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="da75a-128">**Proprietà Selection**</span><span class="sxs-lookup"><span data-stu-id="da75a-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="da75a-129">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="da75a-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




