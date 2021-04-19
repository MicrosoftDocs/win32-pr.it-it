---
description: Si verifica quando si fa doppio clic sul controllo InkEdit.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: Evento InkEdit. DblClick (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317959"
---
# <a name="inkeditdblclick-event"></a><span data-ttu-id="980dd-103">Evento InkEdit. DblClick</span><span class="sxs-lookup"><span data-stu-id="980dd-103">InkEdit.DblClick event</span></span>

<span data-ttu-id="980dd-104">Si verifica quando si fa doppio clic sul controllo [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="980dd-104">Occurs when the [InkEdit](inkedit-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="980dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="980dd-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="980dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="980dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="980dd-107">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="980dd-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="980dd-108">**Variante \_ TRUE** per annullare l'evento per il controllo padre; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="980dd-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="980dd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="980dd-109">Return value</span></span>

<span data-ttu-id="980dd-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="980dd-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="980dd-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="980dd-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="980dd-112">Per distinguere tra i pulsanti sinistro, destro e centrale del mouse, utilizzare gli eventi [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="980dd-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span> <span data-ttu-id="980dd-113">Se nell'evento [**Click**](inkedit-click.md) è presente codice, l'evento **DblClick** non verrà mai attivato.</span><span class="sxs-lookup"><span data-stu-id="980dd-113">If there is code in the [**Click**](inkedit-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="980dd-114">Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="980dd-114">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="980dd-115">L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IeeDblClick**.</span><span class="sxs-lookup"><span data-stu-id="980dd-115">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="980dd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="980dd-116">Requirements</span></span>



| <span data-ttu-id="980dd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="980dd-117">Requirement</span></span> | <span data-ttu-id="980dd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="980dd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="980dd-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="980dd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="980dd-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="980dd-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="980dd-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="980dd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="980dd-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="980dd-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="980dd-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="980dd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="980dd-124"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="980dd-124"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="980dd-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="980dd-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="980dd-126"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="980dd-126"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="980dd-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="980dd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980dd-128">InkEdit</span><span class="sxs-lookup"><span data-stu-id="980dd-128">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




