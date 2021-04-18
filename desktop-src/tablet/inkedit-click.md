---
description: Si verifica quando un utente fa clic sul controllo InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: Evento InkEdit. Click (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316851"
---
# <a name="inkeditclick-event"></a><span data-ttu-id="088ed-103">Evento InkEdit. Click</span><span class="sxs-lookup"><span data-stu-id="088ed-103">InkEdit.Click event</span></span>

<span data-ttu-id="088ed-104">Si verifica quando un utente fa clic sul controllo [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="088ed-104">Occurs when a user clicks the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="088ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="088ed-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="088ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="088ed-106">Parameters</span></span>

<span data-ttu-id="088ed-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="088ed-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="088ed-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="088ed-108">Return value</span></span>

<span data-ttu-id="088ed-109">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="088ed-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="088ed-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="088ed-110">Remarks</span></span>

<span data-ttu-id="088ed-111">Se si fa clic su un controllo, vengono generati eventi [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) oltre all'evento click.</span><span class="sxs-lookup"><span data-stu-id="088ed-111">Clicking a control generates [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="088ed-112">Per distinguere tra i pulsanti sinistro, destro e centrale del mouse, utilizzare gli eventi [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="088ed-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span>

 

<span data-ttu-id="088ed-113">Se nell'evento **Click** è presente codice, l'evento [**DblClick**](inkedit-dblclick.md) non verrà mai attivato, perché l'evento **Click** è il primo evento da attivare tra i due.</span><span class="sxs-lookup"><span data-stu-id="088ed-113">If there is code in the **Click** event, the [**DblClick**](inkedit-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="088ed-114">Di conseguenza, il clic del mouse viene intercettato dall'evento **Click** , quindi l'evento **DblClick** non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="088ed-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="088ed-115">Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="088ed-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="088ed-116">L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IeeClick**.</span><span class="sxs-lookup"><span data-stu-id="088ed-116">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="088ed-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="088ed-117">Requirements</span></span>



| <span data-ttu-id="088ed-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="088ed-118">Requirement</span></span> | <span data-ttu-id="088ed-119">Valore</span><span class="sxs-lookup"><span data-stu-id="088ed-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="088ed-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="088ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="088ed-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="088ed-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="088ed-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="088ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="088ed-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="088ed-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="088ed-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="088ed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="088ed-125"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="088ed-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="088ed-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="088ed-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="088ed-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="088ed-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="088ed-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="088ed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088ed-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="088ed-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




