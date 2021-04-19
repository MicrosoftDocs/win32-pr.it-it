---
description: Si verifica quando la selezione dell'input penna all'interno del controllo viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: Evento InkOverlay. SelectionChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317948"
---
# <a name="inkoverlayselectionchanged-event"></a><span data-ttu-id="6bb5e-103">InkOverlay. SelectionChanged (evento)</span><span class="sxs-lookup"><span data-stu-id="6bb5e-103">InkOverlay.SelectionChanged event</span></span>

<span data-ttu-id="6bb5e-104">Si verifica quando la selezione dell'input penna all'interno del controllo viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="6bb5e-104">Occurs when the selection of ink within the control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb5e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bb5e-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="6bb5e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bb5e-106">Parameters</span></span>

<span data-ttu-id="6bb5e-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="6bb5e-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bb5e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bb5e-108">Return value</span></span>

<span data-ttu-id="6bb5e-109">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6bb5e-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb5e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bb5e-110">Remarks</span></span>

<span data-ttu-id="6bb5e-111">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="6bb5e-111">There are no event data.</span></span>

<span data-ttu-id="6bb5e-112">Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con ID DISPID \_ IOESelectionChanged.</span><span class="sxs-lookup"><span data-stu-id="6bb5e-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb5e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bb5e-113">Requirements</span></span>



| <span data-ttu-id="6bb5e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb5e-114">Requirement</span></span> | <span data-ttu-id="6bb5e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6bb5e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb5e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bb5e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb5e-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6bb5e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6bb5e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bb5e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb5e-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6bb5e-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6bb5e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6bb5e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb5e-121"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb5e-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6bb5e-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="6bb5e-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bb5e-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb5e-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6bb5e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bb5e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb5e-125">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="6bb5e-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="6bb5e-126">**Proprietà Selection**</span><span class="sxs-lookup"><span data-stu-id="6bb5e-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

 




