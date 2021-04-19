---
description: Notfies un'applicazione quando un IME selezionato richiede informazioni sulla finestra candidata. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: Codice di notifica IMR_CANDIDATEWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311759"
---
# <a name="imr_candidatewindow-notification-code"></a><span data-ttu-id="7d8e3-104">\_Codice di notifica CANDIDATEWINDOW di IMR</span><span class="sxs-lookup"><span data-stu-id="7d8e3-104">IMR\_CANDIDATEWINDOW notification code</span></span>

<span data-ttu-id="7d8e3-105">Notfies un'applicazione quando un IME selezionato richiede informazioni sulla finestra candidata.</span><span class="sxs-lookup"><span data-stu-id="7d8e3-105">Notfies an application when a selected IME needs information about the candidate window.</span></span> <span data-ttu-id="7d8e3-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="7d8e3-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a><span data-ttu-id="7d8e3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d8e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8e3-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d8e3-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="7d8e3-109">Impostare su IMR \_ CANDIDATEWINDOW.</span><span class="sxs-lookup"><span data-stu-id="7d8e3-109">Set to IMR\_CANDIDATEWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="7d8e3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d8e3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7d8e3-111">Puntatore a un buffer contenente una struttura [**Campo CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="7d8e3-111">Pointer to a buffer containing a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="7d8e3-112">Il membro **dwIndex** contiene l'indice per la finestra candidata a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="7d8e3-112">Its **dwIndex** member contains the index to the candidate window referenced.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8e3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d8e3-113">Return Value</span></span>

<span data-ttu-id="7d8e3-114">Restituisce un valore diverso da zero se l'applicazione compila la struttura [**Campo CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="7d8e3-114">Returns a nonzero value if the application fills in the [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="7d8e3-115">In caso contrario, il comando restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="7d8e3-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d8e3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d8e3-116">Remarks</span></span>

<span data-ttu-id="7d8e3-117">Questo comando può essere inviato dall'IME a una finestra che ha cancellato il \_ flag SHOWUICANDIDATEWINDOW di ISC nel gestore di messaggi di [**contesto di WM \_ IME \_**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="7d8e3-117">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICANDIDATEWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8e3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d8e3-118">Requirements</span></span>



| <span data-ttu-id="7d8e3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d8e3-119">Requirement</span></span> | <span data-ttu-id="7d8e3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7d8e3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8e3-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d8e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d8e3-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7d8e3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7d8e3-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d8e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d8e3-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7d8e3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7d8e3-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d8e3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d8e3-126"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d8e3-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d8e3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d8e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8e3-128">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="7d8e3-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="7d8e3-129">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="7d8e3-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="7d8e3-130">**Campo CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="7d8e3-130">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="7d8e3-131">**\_richiesta IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="7d8e3-131">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="7d8e3-132">**\_CONtesting IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="7d8e3-132">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 




