---
description: Si verifica quando l'utente rilascia un tasto mentre il controllo InkEdit dispone dello stato attivo.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Evento InkEdit. KeyUp (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590f5f6b2e81e1996bca973f4994c0eade7ead18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530043"
---
# <a name="inkeditkeyup-event"></a><span data-ttu-id="f56da-103">Evento InkEdit. KeyUp</span><span class="sxs-lookup"><span data-stu-id="f56da-103">InkEdit.KeyUp event</span></span>

<span data-ttu-id="f56da-104">Si verifica quando l'utente rilascia un tasto mentre il controllo [InkEdit](inkedit-control-reference.md) dispone dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="f56da-104">Occurs when the user releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="f56da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f56da-105">Syntax</span></span>


```C++
HRESULT KeyUp(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="f56da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f56da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f56da-107">*pKey*</span><span class="sxs-lookup"><span data-stu-id="f56da-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="f56da-108">Codice della chiave virtuale del tasto premuto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f56da-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="f56da-109">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="f56da-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="f56da-110">Membro dell'enumerazione [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) che indica i tasti di modifica che vengono depressi al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f56da-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="f56da-111">Valore</span><span class="sxs-lookup"><span data-stu-id="f56da-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="f56da-112">Significato</span><span class="sxs-lookup"><span data-stu-id="f56da-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="f56da-113"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="f56da-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="f56da-114">Specifica che il tasto MAIUSC è stato utilizzato come modificatore.</span><span class="sxs-lookup"><span data-stu-id="f56da-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="f56da-115"><dt>**IKM \_ Controllo** di</dt></span><span class="sxs-lookup"><span data-stu-id="f56da-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="f56da-116">Specifica che il tasto CTRL è stato utilizzato come modificatore.</span><span class="sxs-lookup"><span data-stu-id="f56da-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="f56da-117"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="f56da-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="f56da-118">Specifica che il tasto ALT è stato utilizzato come modificatore.</span><span class="sxs-lookup"><span data-stu-id="f56da-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f56da-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f56da-119">Return value</span></span>

<span data-ttu-id="f56da-120">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f56da-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f56da-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f56da-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f56da-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f56da-122">Remarks</span></span>

<span data-ttu-id="f56da-123">Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="f56da-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="f56da-124">L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeKeyUp.</span><span class="sxs-lookup"><span data-stu-id="f56da-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="f56da-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f56da-125">Requirements</span></span>



| <span data-ttu-id="f56da-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f56da-126">Requirement</span></span> | <span data-ttu-id="f56da-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f56da-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f56da-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f56da-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f56da-129">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f56da-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f56da-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f56da-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f56da-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f56da-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f56da-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f56da-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f56da-133"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="f56da-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f56da-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="f56da-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="f56da-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f56da-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f56da-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f56da-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f56da-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="f56da-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f56da-138">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="f56da-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="f56da-139">[**\[Controllo InkEdit evento KeyDown\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="f56da-139">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="f56da-140">[**\[Controllo InkEdit evento KeyPress\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="f56da-140">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> </dl>

 

