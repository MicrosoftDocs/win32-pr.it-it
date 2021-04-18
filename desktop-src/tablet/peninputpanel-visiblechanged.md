---
description: Deprecato. L'oggetto PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica quando l'oggetto PenInputPanel è stato visualizzato o nascosto.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Evento PenInputPanel. VisibleChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319156"
---
# <a name="peninputpanelvisiblechanged-event"></a><span data-ttu-id="19532-104">PenInputPanel. VisibleChanged, evento</span><span class="sxs-lookup"><span data-stu-id="19532-104">PenInputPanel.VisibleChanged event</span></span>

<span data-ttu-id="19532-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="19532-105">Deprecated.</span></span> <span data-ttu-id="19532-106">L'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="19532-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="19532-107">Si verifica quando l'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato visualizzato o nascosto.</span><span class="sxs-lookup"><span data-stu-id="19532-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object has shown or hidden itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="19532-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19532-108">Syntax</span></span>


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a><span data-ttu-id="19532-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="19532-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19532-110">*NewVisibility* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19532-110">*NewVisibility* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19532-111">**Variante \_ TRUE** per fare in modo che l'oggetto [**PenInputPanel**](peninputpanel-class.md) diventi visibile. in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="19532-111">**VARIANT\_TRUE** to cause the [**PenInputPanel**](peninputpanel-class.md) object to become visible; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19532-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19532-112">Return value</span></span>

<span data-ttu-id="19532-113">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="19532-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19532-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19532-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19532-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="19532-115">Remarks</span></span>

<span data-ttu-id="19532-116">L'evento **VisibleChanged** si applica alla destinazione del passaggio del mouse sul pannello di input di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="19532-116">The **VisibleChanged** event applies to the Tablet PC Input Panel hover target.</span></span> <span data-ttu-id="19532-117">Tuttavia, non viene generato quando la destinazione del passaggio del mouse si espande per visualizzare il pannello di input completo di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="19532-117">However, it is not raised when the hover target expands to show the full Tablet PC Input Panel.</span></span>

## <a name="requirements"></a><span data-ttu-id="19532-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19532-118">Requirements</span></span>



| <span data-ttu-id="19532-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="19532-119">Requirement</span></span> | <span data-ttu-id="19532-120">Valore</span><span class="sxs-lookup"><span data-stu-id="19532-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19532-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19532-121">Minimum supported client</span></span><br/> | <span data-ttu-id="19532-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="19532-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="19532-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19532-123">Minimum supported server</span></span><br/> | <span data-ttu-id="19532-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="19532-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="19532-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19532-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="19532-126"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="19532-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="19532-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="19532-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="19532-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19532-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="19532-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19532-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19532-130">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="19532-130">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




