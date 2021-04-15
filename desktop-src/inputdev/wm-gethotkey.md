---
title: Messaggio WM_GETHOTKEY (winuser. h)
description: Inviato per determinare il tasto di scelta rapida associato a una finestra.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- Input della tastiera e del mouse WM_GETHOTKEY messaggio
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476157"
---
# <a name="wm_gethotkey-message"></a><span data-ttu-id="be2c8-104">\_Messaggio WM GEThotkey</span><span class="sxs-lookup"><span data-stu-id="be2c8-104">WM\_GETHOTKEY message</span></span>

<span data-ttu-id="be2c8-105">Inviato per determinare il tasto di scelta rapida associato a una finestra.</span><span class="sxs-lookup"><span data-stu-id="be2c8-105">Sent to determine the hot key associated with a window.</span></span>


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a><span data-ttu-id="be2c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be2c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be2c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be2c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be2c8-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="be2c8-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="be2c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be2c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be2c8-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="be2c8-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be2c8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be2c8-111">Return value</span></span>

<span data-ttu-id="be2c8-112">Il valore restituito è il codice della chiave virtuale e i modificatori per il tasto di scelta o **null** se alla finestra non è associato alcun tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="be2c8-112">The return value is the virtual-key code and modifiers for the hot key, or **NULL** if no hot key is associated with the window.</span></span> <span data-ttu-id="be2c8-113">Il codice della chiave virtuale si trova nel byte minimo del valore restituito e i modificatori sono nel byte massimo.</span><span class="sxs-lookup"><span data-stu-id="be2c8-113">The virtual-key code is in the low byte of the return value and the modifiers are in the high byte.</span></span> <span data-ttu-id="be2c8-114">I modificatori possono essere una combinazione dei flag seguenti di CommCtrl. h.</span><span class="sxs-lookup"><span data-stu-id="be2c8-114">The modifiers can be a combination of the following flags from CommCtrl.h.</span></span>



| <span data-ttu-id="be2c8-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="be2c8-115">Return code/value</span></span>                                                                                                                                         | <span data-ttu-id="be2c8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be2c8-116">Description</span></span>             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="be2c8-117"><dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="be2c8-117"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>     | <span data-ttu-id="be2c8-118">ALT (tasto)</span><span class="sxs-lookup"><span data-stu-id="be2c8-118">ALT key</span></span><br/>      |
| <dl> <span data-ttu-id="be2c8-119"><dt>**HOTKEYF \_**</dt> <dt>0x02</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="be2c8-119"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="be2c8-120">Tasto CTRL</span><span class="sxs-lookup"><span data-stu-id="be2c8-120">CTRL key</span></span><br/>     |
| <dl> <span data-ttu-id="be2c8-121"><dt>**HOTKEYF \_**</dt> <dt>0x08</dt> EXT</span><span class="sxs-lookup"><span data-stu-id="be2c8-121"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>     | <span data-ttu-id="be2c8-122">Chiave estesa</span><span class="sxs-lookup"><span data-stu-id="be2c8-122">Extended key</span></span><br/> |
| <dl> <span data-ttu-id="be2c8-123"><dt>**HOTKEYF \_ MAIUSC**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="be2c8-123"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>   | <span data-ttu-id="be2c8-124">Tasto MAIUSC</span><span class="sxs-lookup"><span data-stu-id="be2c8-124">SHIFT key</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="be2c8-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="be2c8-125">Remarks</span></span>

<span data-ttu-id="be2c8-126">Questi tasti di scelta rapida non sono correlati ai tasti di scelta rapida impostati dalla funzione [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) .</span><span class="sxs-lookup"><span data-stu-id="be2c8-126">These hot keys are unrelated to the hot keys set by the [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="be2c8-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be2c8-127">Requirements</span></span>



| <span data-ttu-id="be2c8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="be2c8-128">Requirement</span></span> | <span data-ttu-id="be2c8-129">Valore</span><span class="sxs-lookup"><span data-stu-id="be2c8-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2c8-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be2c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="be2c8-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="be2c8-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be2c8-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be2c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="be2c8-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="be2c8-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be2c8-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be2c8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="be2c8-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be2c8-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be2c8-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be2c8-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="be2c8-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="be2c8-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="be2c8-138">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="be2c8-138">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="be2c8-139">**sehotkey WM \_**</span><span class="sxs-lookup"><span data-stu-id="be2c8-139">**WM\_SETHOTKEY**</span></span>](wm-sethotkey.md)
</dt> <dt>

<span data-ttu-id="be2c8-140">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="be2c8-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="be2c8-141">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="be2c8-141">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

