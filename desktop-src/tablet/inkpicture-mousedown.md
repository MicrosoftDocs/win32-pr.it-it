---
description: Si verifica quando il puntatore del mouse si trova sul controllo InkPicture e viene premuto un pulsante del mouse.
ms.assetid: ff776b2b-7dd8-4d3d-b0f6-714b186d447e
title: Evento InkPicture. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e4459f5c304b3350f9cbad6aba69418bd24844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232484"
---
# <a name="inkpicturemousedown-event"></a><span data-ttu-id="a585a-103">Evento InkPicture. MouseDown</span><span class="sxs-lookup"><span data-stu-id="a585a-103">InkPicture.MouseDown event</span></span>

<span data-ttu-id="a585a-104">Si verifica quando il puntatore del mouse si trova sul controllo [InkPicture](inkpicture-control-reference.md) e viene premuto un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="a585a-104">Occurs when the mouse pointer is over the [InkPicture](inkpicture-control-reference.md) control and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a585a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a585a-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="a585a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a585a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a585a-107">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a585a-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a585a-108">Pulsante premuto.</span><span class="sxs-lookup"><span data-stu-id="a585a-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="a585a-109">*Sposta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a585a-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a585a-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="a585a-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="a585a-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a585a-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a585a-112">Coordinata x, espressa in pixel, dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="a585a-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="a585a-113">*py* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a585a-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a585a-114">Coordinata y, in pixel, dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="a585a-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="a585a-115">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a585a-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a585a-116">**Variante \_ TRUE** per annullare l'evento per il controllo padre; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a585a-116">**VARIANT\_TRUE** to cancel this event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a585a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a585a-117">Return value</span></span>

<span data-ttu-id="a585a-118">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a585a-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a585a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a585a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a585a-120">I parametri pX e pY sono in pixel e non le unità HIMETRIC associate al sistema di coordinate dello spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="a585a-120">The parameters pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="a585a-121">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione che non è compatibile con la penna e che il tipo di applicazione fa riferimento solo ai pixel.</span><span class="sxs-lookup"><span data-stu-id="a585a-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="a585a-122">Alcuni controlli si basano su una relazione specifica tra gli eventi **MouseDown**, [**MouseMove**](inkpicture-mousemove.md)e [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="a585a-122">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkpicture-mousemove.md), and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="a585a-123">L'annullamento di alcuni di questi eventi potrebbe avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="a585a-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="a585a-124">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="a585a-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="a585a-125">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="a585a-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="a585a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a585a-126">Requirements</span></span>



| <span data-ttu-id="a585a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a585a-127">Requirement</span></span> | <span data-ttu-id="a585a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a585a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a585a-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a585a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a585a-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a585a-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a585a-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a585a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a585a-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a585a-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a585a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a585a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a585a-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a585a-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a585a-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="a585a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a585a-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a585a-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a585a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a585a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a585a-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="a585a-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

