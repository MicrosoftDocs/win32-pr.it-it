---
description: Si verifica quando uno o più tratti vengono eliminati dalla raccolta InkStrokes.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: Evento InkStrokes. StrokesRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86448f9676e07a11effe683ecd883874791ff3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349891"
---
# <a name="inkstrokesstrokesremoved-event"></a><span data-ttu-id="1007c-103">Evento InkStrokes. StrokesRemoved</span><span class="sxs-lookup"><span data-stu-id="1007c-103">InkStrokes.StrokesRemoved event</span></span>

<span data-ttu-id="1007c-104">Si verifica quando uno o più tratti vengono eliminati dalla raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1007c-104">Occurs when one or more strokes are deleted from the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1007c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1007c-105">Syntax</span></span>


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="1007c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1007c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1007c-107">*StrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1007c-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1007c-108">Matrice di interi degli identificatori per ogni oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) eliminato quando si verifica questo evento.</span><span class="sxs-lookup"><span data-stu-id="1007c-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object deleted when this event occurs.</span></span>

<span data-ttu-id="1007c-109">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="1007c-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1007c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1007c-110">Return value</span></span>

<span data-ttu-id="1007c-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1007c-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1007c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1007c-112">Remarks</span></span>

<span data-ttu-id="1007c-113">Questo metodo di evento è definito nell' \_ interfaccia IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="1007c-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="1007c-114">L' \_ interfaccia IInkEvents implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ SEStrokesRemoved.</span><span class="sxs-lookup"><span data-stu-id="1007c-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="1007c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1007c-115">Requirements</span></span>



| <span data-ttu-id="1007c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1007c-116">Requirement</span></span> | <span data-ttu-id="1007c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1007c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1007c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1007c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1007c-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1007c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1007c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1007c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1007c-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1007c-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1007c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1007c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1007c-123"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1007c-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1007c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="1007c-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="1007c-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1007c-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1007c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1007c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="1007c-127">[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1007c-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1007c-128">[**Rimuovere il metodo \[ InkStrokes collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span><span class="sxs-lookup"><span data-stu-id="1007c-128">[**Remove Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span></span>
</dt> <dt>

[<span data-ttu-id="1007c-129">**Classe InkDisp**</span><span class="sxs-lookup"><span data-stu-id="1007c-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 

