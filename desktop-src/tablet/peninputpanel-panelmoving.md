---
description: Deprecato. L'oggetto PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica quando l'oggetto PenInputPanel viene spostato.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Evento PenInputPanel. PanelMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319157"
---
# <a name="peninputpanelpanelmoving-event"></a><span data-ttu-id="051e2-104">PenInputPanel. PanelMoving, evento</span><span class="sxs-lookup"><span data-stu-id="051e2-104">PenInputPanel.PanelMoving event</span></span>

<span data-ttu-id="051e2-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="051e2-105">Deprecated.</span></span> <span data-ttu-id="051e2-106">L'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="051e2-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="051e2-107">Si verifica quando l'oggetto [**PenInputPanel**](peninputpanel-class.md) viene spostato.</span><span class="sxs-lookup"><span data-stu-id="051e2-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object is moving.</span></span>

## <a name="syntax"></a><span data-ttu-id="051e2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="051e2-108">Syntax</span></span>


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a><span data-ttu-id="051e2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="051e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="051e2-110">A *sinistra* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="051e2-110">*Left* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="051e2-111">Nuova posizione orizzontale, o asse x, del bordo sinistro dell'oggetto [**PenInputPanel**](peninputpanel-class.md) , in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="051e2-111">The new horizontal, or x-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="051e2-112">In *alto* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="051e2-112">*Top* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="051e2-113">Nuova posizione verticale, o asse y, del bordo sinistro dell'oggetto [**PenInputPanel**](peninputpanel-class.md) , in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="051e2-113">The new vertical, or y-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="051e2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="051e2-114">Return value</span></span>

<span data-ttu-id="051e2-115">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="051e2-115">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="051e2-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="051e2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="051e2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="051e2-117">Remarks</span></span>

<span data-ttu-id="051e2-118">L'evento **PanelMoving** è progettato per essere usato per modificare la posizione del pannello input penna cambiando i parametri *Left* e *Top* .</span><span class="sxs-lookup"><span data-stu-id="051e2-118">The **PanelMoving** event is designed to be used to change the position of the pen input panel by changing the *Left* and *Top* parameters.</span></span>

<span data-ttu-id="051e2-119">I metodi [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) e [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) fanno sì che l'oggetto [**PenInputPanel**](peninputpanel-class.md) chiami il codice di posizionamento automatico che attiva un evento **PanelMoving** .</span><span class="sxs-lookup"><span data-stu-id="051e2-119">The [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) and [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) methods cause the [**PenInputPanel**](peninputpanel-class.md) object to call its auto-positioning code which triggers a **PanelMoving** event.</span></span> <span data-ttu-id="051e2-120">Di conseguenza, la chiamata di questi metodi all'interno di un gestore **PanelMoving** può causare un ciclo infinito ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="051e2-120">Consequently, calling these methods inside a **PanelMoving** handler can result in a recursive endless loop.</span></span>

## <a name="requirements"></a><span data-ttu-id="051e2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="051e2-121">Requirements</span></span>



| <span data-ttu-id="051e2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="051e2-122">Requirement</span></span> | <span data-ttu-id="051e2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="051e2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="051e2-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="051e2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="051e2-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="051e2-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="051e2-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="051e2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="051e2-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="051e2-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="051e2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="051e2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="051e2-129"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="051e2-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="051e2-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="051e2-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="051e2-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="051e2-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="051e2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="051e2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="051e2-133">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="051e2-133">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




