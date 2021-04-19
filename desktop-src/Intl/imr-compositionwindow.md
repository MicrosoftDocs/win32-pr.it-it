---
description: Notifica a un'applicazione quando un IME selezionato richiede informazioni sulla finestra di composizione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con i parametri impostati come illustrato di seguito.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: Codice di notifica IMR_COMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311757"
---
# <a name="imr_compositionwindow-notification-code"></a><span data-ttu-id="2363c-104">\_Codice di notifica COMPOSITIONWINDOW di IMR</span><span class="sxs-lookup"><span data-stu-id="2363c-104">IMR\_COMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="2363c-105">Notifica a un'applicazione quando un IME selezionato richiede informazioni sulla finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="2363c-105">Notifies an application when a selected IME needs information about the composition window.</span></span> <span data-ttu-id="2363c-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con i parametri impostati come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="2363c-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="2363c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2363c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2363c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2363c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2363c-109">Impostare su IMR \_ COMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="2363c-109">Set to IMR\_COMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="2363c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2363c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2363c-111">Puntatore a un buffer contenente una struttura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="2363c-111">Pointer to a buffer containing a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2363c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2363c-112">Return Value</span></span>

<span data-ttu-id="2363c-113">Restituisce un valore diverso da zero se l'applicazione compila la struttura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="2363c-113">Returns a nonzero value if the application fills in the [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span> <span data-ttu-id="2363c-114">In caso contrario, il comando restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="2363c-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="2363c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2363c-115">Remarks</span></span>

<span data-ttu-id="2363c-116">Questo comando può essere inviato dall'IME a una finestra che ha cancellato il \_ flag SHOWUICOMPOSITIONWINDOW di ISC nel gestore di messaggi di [**contesto di WM \_ IME \_**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="2363c-116">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="2363c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2363c-117">Requirements</span></span>



| <span data-ttu-id="2363c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2363c-118">Requirement</span></span> | <span data-ttu-id="2363c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2363c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2363c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2363c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2363c-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2363c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2363c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2363c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2363c-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2363c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2363c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2363c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2363c-125"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2363c-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2363c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2363c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2363c-127">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="2363c-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2363c-128">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="2363c-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2363c-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="2363c-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="2363c-130">**\_richiesta IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="2363c-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="2363c-131">**\_CONtesting IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="2363c-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 




