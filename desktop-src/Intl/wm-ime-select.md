---
description: Inviato a un'applicazione quando il sistema operativo sta per cambiare l'IME corrente. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Messaggio WM_IME_SELECT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307275"
---
# <a name="wm_ime_select-message"></a><span data-ttu-id="a0ce3-104">\_Messaggio di \_ selezione IME WM</span><span class="sxs-lookup"><span data-stu-id="a0ce3-104">WM\_IME\_SELECT message</span></span>

<span data-ttu-id="a0ce3-105">Inviato a un'applicazione quando il sistema operativo sta per cambiare l'IME corrente.</span><span class="sxs-lookup"><span data-stu-id="a0ce3-105">Sent to an application when the operating system is about to change the current IME.</span></span> <span data-ttu-id="a0ce3-106">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a0ce3-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="a0ce3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0ce3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ce3-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a0ce3-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a0ce3-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="a0ce3-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="a0ce3-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0ce3-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0ce3-111">Indicatore di selezione.</span><span class="sxs-lookup"><span data-stu-id="a0ce3-111">Selection indicator.</span></span> <span data-ttu-id="a0ce3-112">Questo parametro specifica **true** se l'IME indicato è selezionato.</span><span class="sxs-lookup"><span data-stu-id="a0ce3-112">This parameter specifies **TRUE** if the indicated IME is selected.</span></span> <span data-ttu-id="a0ce3-113">Il parametro è impostato su **false** se l'IME specificato non è più selezionato.</span><span class="sxs-lookup"><span data-stu-id="a0ce3-113">The parameter is set to **FALSE** if the specified IME is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="a0ce3-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0ce3-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0ce3-115">Identificatore delle impostazioni locali di input associato all'IME.</span><span class="sxs-lookup"><span data-stu-id="a0ce3-115">Input locale identifier associated with the IME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0ce3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0ce3-116">Return value</span></span>

<span data-ttu-id="a0ce3-117">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="a0ce3-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0ce3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0ce3-118">Remarks</span></span>

<span data-ttu-id="a0ce3-119">Un'applicazione che ha creato una finestra IME deve passare questo messaggio alla finestra in modo che sia in grado di recuperare l'handle di layout della tastiera per l'IME appena selezionato.</span><span class="sxs-lookup"><span data-stu-id="a0ce3-119">An application that has created an IME window should pass this message to that window so that it can retrieve the keyboard layout handle to the newly selected IME.</span></span>

<span data-ttu-id="a0ce3-120">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  elabora questo messaggio passando le informazioni alla finestra IME predefinita.</span><span class="sxs-lookup"><span data-stu-id="a0ce3-120">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing the information to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0ce3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0ce3-121">Requirements</span></span>



| <span data-ttu-id="a0ce3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0ce3-122">Requirement</span></span> | <span data-ttu-id="a0ce3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a0ce3-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ce3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0ce3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ce3-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0ce3-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a0ce3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0ce3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ce3-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0ce3-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0ce3-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0ce3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0ce3-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0ce3-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0ce3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0ce3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ce3-131">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="a0ce3-131">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a0ce3-132">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="a0ce3-132">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
