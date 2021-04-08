---
description: Inviato a tutte le finestre dopo che l'utente ha effettuato l'accesso o la disconnessione. Quando l'utente effettua l'accesso o la disattivazione, il sistema aggiorna le impostazioni specifiche dell'utente. Il sistema invia questo messaggio immediatamente dopo l'aggiornamento delle impostazioni.
title: Messaggio WM_USERCHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968408"
---
# <a name="wm_userchanged-message"></a><span data-ttu-id="3b8da-105">\_Messaggio USERCHANGED WM</span><span class="sxs-lookup"><span data-stu-id="3b8da-105">WM\_USERCHANGED message</span></span>

<span data-ttu-id="3b8da-106">Inviato a tutte le finestre dopo che l'utente ha effettuato l'accesso o la disconnessione.</span><span class="sxs-lookup"><span data-stu-id="3b8da-106">Sent to all windows after the user has logged on or off.</span></span> <span data-ttu-id="3b8da-107">Quando l'utente effettua l'accesso o la disattivazione, il sistema aggiorna le impostazioni specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3b8da-107">When the user logs on or off, the system updates the user-specific settings.</span></span> <span data-ttu-id="3b8da-108">Il sistema invia questo messaggio immediatamente dopo l'aggiornamento delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="3b8da-108">The system sends this message immediately after updating the settings.</span></span>

<span data-ttu-id="3b8da-109">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3b8da-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="3b8da-110">Questo messaggio non è supportato in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3b8da-110">This message is not supported as of Windows Vista.</span></span>

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a><span data-ttu-id="3b8da-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b8da-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b8da-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b8da-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b8da-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="3b8da-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b8da-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b8da-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b8da-115">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="3b8da-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b8da-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b8da-116">Return value</span></span>

<span data-ttu-id="3b8da-117">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="3b8da-117">Type: **LRESULT**</span></span>

<span data-ttu-id="3b8da-118">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="3b8da-118">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b8da-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b8da-119">Requirements</span></span>



| <span data-ttu-id="3b8da-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b8da-120">Requirement</span></span> | <span data-ttu-id="3b8da-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3b8da-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8da-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b8da-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b8da-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3b8da-123">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3b8da-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b8da-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b8da-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3b8da-125">None supported</span></span><br/>                                                                                |
| <span data-ttu-id="3b8da-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b8da-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b8da-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b8da-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8da-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b8da-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8da-129">Panoramica di Windows</span><span class="sxs-lookup"><span data-stu-id="3b8da-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
