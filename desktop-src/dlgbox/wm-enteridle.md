---
title: Messaggio WM_ENTERIDLE (winuser. h)
description: Inviato alla finestra proprietaria di una finestra di dialogo modale o di un menu che entra in uno stato di inattività. Una finestra di dialogo o un menu modale entra in uno stato di inattività quando nessun messaggio è in attesa nella coda dopo l'elaborazione di uno o più messaggi precedenti.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- Finestre di dialogo WM_ENTERIDLE messaggio
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400813"
---
# <a name="wm_enteridle-message"></a><span data-ttu-id="0aadb-105">\_Messaggio ENTERIDLE WM</span><span class="sxs-lookup"><span data-stu-id="0aadb-105">WM\_ENTERIDLE message</span></span>

<span data-ttu-id="0aadb-106">Inviato alla finestra proprietaria di una finestra di dialogo modale o di un menu che entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="0aadb-106">Sent to the owner window of a modal dialog box or menu that is entering an idle state.</span></span> <span data-ttu-id="0aadb-107">Una finestra di dialogo o un menu modale entra in uno stato di inattività quando nessun messaggio è in attesa nella coda dopo l'elaborazione di uno o più messaggi precedenti.</span><span class="sxs-lookup"><span data-stu-id="0aadb-107">A modal dialog box or menu enters an idle state when no messages are waiting in its queue after it has processed one or more previous messages.</span></span>


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a><span data-ttu-id="0aadb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0aadb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aadb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0aadb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0aadb-110">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0aadb-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0aadb-111">Valore</span><span class="sxs-lookup"><span data-stu-id="0aadb-111">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="0aadb-112">Significato</span><span class="sxs-lookup"><span data-stu-id="0aadb-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <span data-ttu-id="0aadb-113"><dt>**MSGF \_ DIALOGBOX**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0aadb-113"><dt>**MSGF\_DIALOGBOX**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="0aadb-114">Il sistema è inattivo perché viene visualizzata una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="0aadb-114">The system is idle because a dialog box is displayed.</span></span><br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <span data-ttu-id="0aadb-115"><dt>**MSGF \_ MENU**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0aadb-115"><dt>**MSGF\_MENU**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="0aadb-116">Il sistema è inattivo perché viene visualizzato un menu.</span><span class="sxs-lookup"><span data-stu-id="0aadb-116">The system is idle because a menu is displayed.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="0aadb-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0aadb-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0aadb-118">Handle per la finestra di dialogo (se *wParam* è **MSGF \_ DialogBox**) o finestra contenente il menu visualizzato (se *wParam* è **il \_ menu MSGF**).</span><span class="sxs-lookup"><span data-stu-id="0aadb-118">A handle to the dialog box (if *wParam* is **MSGF\_DIALOGBOX**) or window containing the displayed menu (if *wParam* is **MSGF\_MENU**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aadb-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0aadb-119">Return value</span></span>

<span data-ttu-id="0aadb-120">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="0aadb-120">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aadb-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0aadb-121">Remarks</span></span>

<span data-ttu-id="0aadb-122">È possibile disattivare il messaggio **WM \_ ENTERIDLE** per una finestra di dialogo creando la finestra di dialogo con lo stile **DS \_ NOIDLEMSG** .</span><span class="sxs-lookup"><span data-stu-id="0aadb-122">You can suppress the **WM\_ENTERIDLE** message for a dialog box by creating the dialog box with the **DS\_NOIDLEMSG** style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aadb-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aadb-123">Requirements</span></span>



| <span data-ttu-id="0aadb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aadb-124">Requirement</span></span> | <span data-ttu-id="0aadb-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0aadb-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aadb-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aadb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0aadb-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0aadb-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0aadb-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aadb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0aadb-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0aadb-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0aadb-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0aadb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aadb-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aadb-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aadb-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0aadb-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="0aadb-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0aadb-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0aadb-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="0aadb-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="0aadb-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0aadb-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0aadb-136">Finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="0aadb-136">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

