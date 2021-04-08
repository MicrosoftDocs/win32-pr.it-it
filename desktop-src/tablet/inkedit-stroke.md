---
description: Si verifica quando l'utente disegna un nuovo oggetto IInkStrokeDisp in un oggetto IInkTablet.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: Evento InkEdit. Stroke (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d21abde9deb565f207a44ddd44b51681f1bfa6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759539"
---
# <a name="inkeditstroke-event"></a><span data-ttu-id="205a8-103">Evento InkEdit. Stroke</span><span class="sxs-lookup"><span data-stu-id="205a8-103">InkEdit.Stroke event</span></span>

<span data-ttu-id="205a8-104">Si verifica quando l'utente disegna un nuovo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in un oggetto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .</span><span class="sxs-lookup"><span data-stu-id="205a8-104">Occurs when the user draws a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object on any [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="205a8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="205a8-105">Syntax</span></span>


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="205a8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="205a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="205a8-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="205a8-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205a8-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="205a8-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="205a8-109">*Tratto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="205a8-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205a8-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto.</span><span class="sxs-lookup"><span data-stu-id="205a8-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="205a8-111">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="205a8-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="205a8-112">**Variante \_ TRUE** per annullare la raccolta dell'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) . **Variante \_ FALSE** per raccogliere l'oggetto **IInkStrokeDisp** e continuare anche con il **tratto** .</span><span class="sxs-lookup"><span data-stu-id="205a8-112">**VARIANT\_TRUE** to cancel the collection of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object; **VARIANT\_FALSE** to collect the **IInkStrokeDisp** object and continue with the **Stroke** even.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="205a8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="205a8-113">Return value</span></span>

<span data-ttu-id="205a8-114">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="205a8-114">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="205a8-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="205a8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="205a8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="205a8-116">Remarks</span></span>

<span data-ttu-id="205a8-117">Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="205a8-117">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="205a8-118">L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeStroke.</span><span class="sxs-lookup"><span data-stu-id="205a8-118">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeStroke.</span></span>

## <a name="requirements"></a><span data-ttu-id="205a8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="205a8-119">Requirements</span></span>



| <span data-ttu-id="205a8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="205a8-120">Requirement</span></span> | <span data-ttu-id="205a8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="205a8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="205a8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="205a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="205a8-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="205a8-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="205a8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="205a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="205a8-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="205a8-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="205a8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="205a8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="205a8-127"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="205a8-127"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="205a8-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="205a8-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="205a8-129"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="205a8-129"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="205a8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="205a8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205a8-131">InkEdit</span><span class="sxs-lookup"><span data-stu-id="205a8-131">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="205a8-132">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="205a8-132">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="205a8-133">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="205a8-133">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

