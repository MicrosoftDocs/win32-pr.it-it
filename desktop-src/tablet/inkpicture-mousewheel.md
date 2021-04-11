---
description: Si verifica quando viene spostata la rotellina del mouse mentre il controllo InkPicture dispone dello stato attivo.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: Evento InkPicture. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346111"
---
# <a name="inkpicturemousewheel-event"></a><span data-ttu-id="8c05e-103">Evento InkPicture. MouseWheel</span><span class="sxs-lookup"><span data-stu-id="8c05e-103">InkPicture.MouseWheel event</span></span>

<span data-ttu-id="8c05e-104">Si verifica quando viene spostata la rotellina del mouse mentre il controllo [InkPicture](inkpicture-control-reference.md) dispone dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="8c05e-104">Occurs when the mouse wheel moves while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c05e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c05e-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="8c05e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c05e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c05e-107">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c05e-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c05e-108">Pulsante premuto.</span><span class="sxs-lookup"><span data-stu-id="8c05e-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="8c05e-109">*Sposta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c05e-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c05e-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="8c05e-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="8c05e-111">*Delta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c05e-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c05e-112">Distanza di spostamento della rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="8c05e-112">The distance that the mouse wheel turned.</span></span>

</dd> <dt>

<span data-ttu-id="8c05e-113">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c05e-113">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c05e-114">Coordinata x, espressa in pixel, dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="8c05e-114">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="8c05e-115">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c05e-115">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c05e-116">Coordinata y, in pixel, dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="8c05e-116">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="8c05e-117">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8c05e-117">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c05e-118">VARIANT \_ true per annullare l'evento **MouseWheel** per il controllo padre; in caso contrario, VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="8c05e-118">VARIANT\_TRUE to cancel the **MouseWheel** event for the parent control; otherwise, VARIANT\_FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c05e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c05e-119">Return value</span></span>

<span data-ttu-id="8c05e-120">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8c05e-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c05e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c05e-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c05e-122">I parametri *x* e *y* sono in pixel e non le unità HIMETRIC associate al sistema di coordinate dello spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="8c05e-122">The parameters *x* and *y* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="8c05e-123">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione che non è compatibile con la penna e che il tipo di applicazione fa riferimento solo ai pixel.</span><span class="sxs-lookup"><span data-stu-id="8c05e-123">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

<span data-ttu-id="8c05e-124">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="8c05e-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="8c05e-125">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="8c05e-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c05e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c05e-126">Requirements</span></span>



| <span data-ttu-id="8c05e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c05e-127">Requirement</span></span> | <span data-ttu-id="8c05e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8c05e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c05e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c05e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8c05e-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8c05e-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8c05e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c05e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8c05e-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8c05e-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8c05e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c05e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c05e-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8c05e-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8c05e-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="8c05e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c05e-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c05e-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8c05e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c05e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c05e-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="8c05e-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

