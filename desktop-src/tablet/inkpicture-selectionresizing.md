---
description: Si verifica quando la dimensione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: Evento InkPicture. SelectionResizing (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1b7923810777c6ebe0af3364121cbcee67b18d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968421"
---
# <a name="inkpictureselectionresizing-event"></a><span data-ttu-id="1a467-103">Evento InkPicture. SelectionResizing</span><span class="sxs-lookup"><span data-stu-id="1a467-103">InkPicture.SelectionResizing event</span></span>

<span data-ttu-id="1a467-104">Si verifica quando la dimensione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="1a467-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a467-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a467-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="1a467-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a467-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a467-107">*CurSelectionRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a467-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a467-108">Rettangolo di delimitazione della selezione dopo l'evento **SelectionResizing** .</span><span class="sxs-lookup"><span data-stu-id="1a467-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="1a467-109">Questo rettangolo viene specificato nelle coordinate della finestra client, che consente scenari come la gestione delle proporzioni durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="1a467-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a467-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a467-110">Return value</span></span>

<span data-ttu-id="1a467-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1a467-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a467-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a467-112">Remarks</span></span>

<span data-ttu-id="1a467-113">Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="1a467-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a467-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a467-114">Requirements</span></span>



| <span data-ttu-id="1a467-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a467-115">Requirement</span></span> | <span data-ttu-id="1a467-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1a467-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a467-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a467-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1a467-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1a467-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1a467-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a467-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1a467-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1a467-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1a467-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a467-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a467-122"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1a467-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1a467-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="1a467-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a467-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a467-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1a467-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a467-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a467-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1a467-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="1a467-127">[**Controllo InkPicture della proprietà Selection \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="1a467-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="1a467-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="1a467-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




