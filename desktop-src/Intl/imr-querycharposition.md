---
description: Notifica a un'applicazione quando l'IME selezionato richiede informazioni sulle coordinate di un carattere nella stringa di composizione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: Codice di notifica IMR_QUERYCHARPOSITION (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311755"
---
# <a name="imr_querycharposition-notification-code"></a><span data-ttu-id="2d567-104">\_Codice di notifica QUERYCHARPOSITION di IMR</span><span class="sxs-lookup"><span data-stu-id="2d567-104">IMR\_QUERYCHARPOSITION notification code</span></span>

<span data-ttu-id="2d567-105">Notifica a un'applicazione quando l'IME selezionato richiede informazioni sulle coordinate di un carattere nella stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="2d567-105">Notifies an application when the selected IME needs information about the coordinates of a character in the composition string.</span></span> <span data-ttu-id="2d567-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="2d567-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a><span data-ttu-id="2d567-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d567-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d567-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d567-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2d567-109">Impostare su IMR \_ QUERYCHARPOSITION.</span><span class="sxs-lookup"><span data-stu-id="2d567-109">Set to IMR\_QUERYCHARPOSITION.</span></span>

</dd> <dt>

<span data-ttu-id="2d567-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d567-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2d567-111">Puntatore a una struttura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) che contiene la posizione del carattere nella finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="2d567-111">Pointer to an [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure that contains the position of the character in the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d567-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d567-112">Return Value</span></span>

<span data-ttu-id="2d567-113">Restituisce un valore diverso da zero se l'applicazione riempie la struttura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="2d567-113">Returns a nonzero value if the application fills the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="2d567-114">In caso contrario, il comando restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="2d567-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d567-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d567-115">Remarks</span></span>

<span data-ttu-id="2d567-116">Un'applicazione che disegna la stringa di composizione, anziché basarsi sull'IME, è responsabile del riempimento di tutti i membri della struttura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="2d567-116">An application that draws the composition string itself, instead of relying on the IME, is responsible for filling in all the members of the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="2d567-117">In caso contrario, l'applicazione deve passare il comando a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) se dispone di una propria finestra dell'interfaccia utente IME.</span><span class="sxs-lookup"><span data-stu-id="2d567-117">Otherwise, the application should pass the command to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) if it has its own IME user interface window.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d567-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d567-118">Requirements</span></span>



| <span data-ttu-id="2d567-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d567-119">Requirement</span></span> | <span data-ttu-id="2d567-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2d567-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d567-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d567-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2d567-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d567-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2d567-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d567-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2d567-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d567-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d567-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d567-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d567-126"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d567-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d567-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d567-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d567-128">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="2d567-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2d567-129">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="2d567-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2d567-130">**IMECHARPOSITION**</span><span class="sxs-lookup"><span data-stu-id="2d567-130">**IMECHARPOSITION**</span></span>](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[<span data-ttu-id="2d567-131">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="2d567-131">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[<span data-ttu-id="2d567-132">**\_richiesta IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="2d567-132">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 
