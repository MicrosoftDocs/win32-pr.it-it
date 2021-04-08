---
description: Si verifica quando l'utente preme un tasto mentre il controllo InkEdit dispone dello stato attivo.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: Evento InkEdit. KeyDown (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cee260d4c902534b9b234e0e30d0b60645c579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968424"
---
# <a name="inkeditkeydown-event"></a><span data-ttu-id="4254d-103">Evento InkEdit. KeyDown</span><span class="sxs-lookup"><span data-stu-id="4254d-103">InkEdit.KeyDown event</span></span>

<span data-ttu-id="4254d-104">Si verifica quando l'utente preme un tasto mentre il controllo [InkEdit](inkedit-control-reference.md) dispone dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="4254d-104">Occurs when the user presses a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="4254d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4254d-105">Syntax</span></span>


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="4254d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4254d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4254d-107">*pKey*</span><span class="sxs-lookup"><span data-stu-id="4254d-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="4254d-108">Codice della chiave virtuale del tasto premuto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4254d-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="4254d-109">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="4254d-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="4254d-110">Membro dell'enumerazione [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) che indica i tasti di modifica che vengono depressi al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="4254d-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration, that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="4254d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="4254d-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="4254d-112">Significato</span><span class="sxs-lookup"><span data-stu-id="4254d-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="4254d-113"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="4254d-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="4254d-114">Specifica che il tasto MAIUSC è stato utilizzato come modificatore.</span><span class="sxs-lookup"><span data-stu-id="4254d-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="4254d-115"><dt>**IKM \_ Controllo** di</dt></span><span class="sxs-lookup"><span data-stu-id="4254d-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="4254d-116">Specifica che il tasto CTRL è stato utilizzato come modificatore.</span><span class="sxs-lookup"><span data-stu-id="4254d-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="4254d-117"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="4254d-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="4254d-118">Specifica che il tasto ALT è stato utilizzato come modificatore.</span><span class="sxs-lookup"><span data-stu-id="4254d-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4254d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4254d-119">Return value</span></span>

<span data-ttu-id="4254d-120">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4254d-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4254d-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4254d-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4254d-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="4254d-122">Remarks</span></span>

<span data-ttu-id="4254d-123">Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="4254d-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="4254d-124">L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeKeyDown.</span><span class="sxs-lookup"><span data-stu-id="4254d-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="4254d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4254d-125">Requirements</span></span>



| <span data-ttu-id="4254d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4254d-126">Requirement</span></span> | <span data-ttu-id="4254d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4254d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4254d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4254d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4254d-129">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4254d-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4254d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4254d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4254d-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4254d-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4254d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4254d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4254d-133"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="4254d-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4254d-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="4254d-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="4254d-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4254d-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4254d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4254d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4254d-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="4254d-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="4254d-138">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="4254d-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="4254d-139">[**\[Controllo InkEdit evento KeyPress\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="4254d-139">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> <dt>

<span data-ttu-id="4254d-140">[**\[Controllo InkEdit evento KeyUp\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="4254d-140">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

