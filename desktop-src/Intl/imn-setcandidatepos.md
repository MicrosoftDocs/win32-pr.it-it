---
description: Notifica a un'applicazione il completamento dell'elaborazione del candidato e l'IME sta per spostare la finestra candidata. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: Codice di notifica IMN_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312863"
---
# <a name="imn_setcandidatepos-notification-code"></a><span data-ttu-id="c2d7a-104">\_Codice di notifica SETCANDIDATEPOS di IMN</span><span class="sxs-lookup"><span data-stu-id="c2d7a-104">IMN\_SETCANDIDATEPOS notification code</span></span>

<span data-ttu-id="c2d7a-105">Notifica a un'applicazione il completamento dell'elaborazione del candidato e l'IME sta per spostare la finestra candidata.</span><span class="sxs-lookup"><span data-stu-id="c2d7a-105">Notifies an application when candidate processing has finished and the IME is about to move the candidate window.</span></span> <span data-ttu-id="c2d7a-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c2d7a-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="c2d7a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2d7a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2d7a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2d7a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="c2d7a-109">Impostare su IMN \_ SETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="c2d7a-109">Set to IMN\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="c2d7a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2d7a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="c2d7a-111">Flag elenco candidati.</span><span class="sxs-lookup"><span data-stu-id="c2d7a-111">Candidate list flag.</span></span> <span data-ttu-id="c2d7a-112">Ogni bit corrisponde a un elenco di candidati: bit 0 per il primo elenco, bit 1 al secondo e così via.</span><span class="sxs-lookup"><span data-stu-id="c2d7a-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="c2d7a-113">Se un bit specificato è 1, la finestra candidata corrispondente sta per essere spostata.</span><span class="sxs-lookup"><span data-stu-id="c2d7a-113">If a specified bit is 1, the corresponding candidate window is about to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2d7a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2d7a-114">Return Value</span></span>

<span data-ttu-id="c2d7a-115">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="c2d7a-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2d7a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2d7a-116">Remarks</span></span>

<span data-ttu-id="c2d7a-117">Un'applicazione deve elaborare questo comando se Visualizza la finestra candidata.</span><span class="sxs-lookup"><span data-stu-id="c2d7a-117">An application should process this command if it displays the candidate window itself.</span></span>

<span data-ttu-id="c2d7a-118">La finestra IME sposta la finestra candidata durante l'elaborazione del comando.</span><span class="sxs-lookup"><span data-stu-id="c2d7a-118">The IME window moves the candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2d7a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2d7a-119">Requirements</span></span>



| <span data-ttu-id="c2d7a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2d7a-120">Requirement</span></span> | <span data-ttu-id="c2d7a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c2d7a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d7a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2d7a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2d7a-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2d7a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c2d7a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2d7a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2d7a-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2d7a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c2d7a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2d7a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2d7a-127"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2d7a-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2d7a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2d7a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d7a-129">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="c2d7a-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="c2d7a-130">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="c2d7a-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="c2d7a-131">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="c2d7a-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




