---
description: Notifica a un'applicazione quando un IME selezionato richiede informazioni sul tipo di carattere utilizzato dalla finestra di composizione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con i parametri, come illustrato di seguito.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: Codice di notifica IMR_COMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311758"
---
# <a name="imr_compositionfont-notification-code"></a><span data-ttu-id="3a228-104">\_Codice di notifica COMPOSITIONFONT di IMR</span><span class="sxs-lookup"><span data-stu-id="3a228-104">IMR\_COMPOSITIONFONT notification code</span></span>

<span data-ttu-id="3a228-105">Notifica a un'applicazione quando un IME selezionato richiede informazioni sul tipo di carattere utilizzato dalla finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="3a228-105">Notifies an application when a selected IME needs information about the font used by the composition window.</span></span> <span data-ttu-id="3a228-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con i parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3a228-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="3a228-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a228-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a228-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a228-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="3a228-109">Impostare su IMR \_ COMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="3a228-109">Set to IMR\_COMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="3a228-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a228-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3a228-111">Puntatore a un buffer contenente una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="3a228-111">Pointer to a buffer containing a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="3a228-112">L'applicazione compila i valori per la finestra di composizione corrente.</span><span class="sxs-lookup"><span data-stu-id="3a228-112">The application fills in the values for the current composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a228-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a228-113">Return Value</span></span>

<span data-ttu-id="3a228-114">Restituisce un valore diverso da zero se l'applicazione compila la struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="3a228-114">Returns a nonzero value if the application fills in the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="3a228-115">In caso contrario, il comando restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="3a228-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a228-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a228-116">Remarks</span></span>

<span data-ttu-id="3a228-117">Questo comando può essere inviato dall'IME a una finestra che ha cancellato il \_ flag SHOWUICOMPOSITIONWINDOW di ISC nel gestore di messaggi di [**contesto di WM \_ IME \_**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="3a228-117">This command can be sent by the IME to a window that cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a228-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a228-118">Requirements</span></span>



| <span data-ttu-id="3a228-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a228-119">Requirement</span></span> | <span data-ttu-id="3a228-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3a228-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a228-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a228-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a228-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a228-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3a228-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a228-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a228-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a228-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3a228-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a228-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a228-126"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a228-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a228-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a228-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a228-128">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="3a228-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="3a228-129">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="3a228-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="3a228-130">**\_richiesta IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="3a228-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="3a228-131">**\_CONtesting IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a228-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 
