---
description: Invia una notifica all'applicazione quando un IME sta per modificare il contenuto della finestra candidata. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: Codice di notifica IMN_CHANGECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131739"
---
# <a name="imn_changecandidate-notification-code"></a><span data-ttu-id="d2439-104">\_Codice di notifica CHANGECANDIDATE di IMN</span><span class="sxs-lookup"><span data-stu-id="d2439-104">IMN\_CHANGECANDIDATE notification code</span></span>

<span data-ttu-id="d2439-105">Invia una notifica all'applicazione quando un IME sta per modificare il contenuto della finestra candidata.</span><span class="sxs-lookup"><span data-stu-id="d2439-105">Notifies the application when an IME is about to change the content of the candidate window.</span></span> <span data-ttu-id="d2439-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d2439-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="d2439-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2439-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2439-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2439-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d2439-109">Impostare su IMN \_ CHANGECANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="d2439-109">Set to IMN\_CHANGECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="d2439-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2439-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d2439-111">Flag elenco candidati.</span><span class="sxs-lookup"><span data-stu-id="d2439-111">Candidate list flag.</span></span> <span data-ttu-id="d2439-112">Ogni bit corrisponde a un elenco di candidati: bit 0 per il primo elenco, bit 1 nel secondo elenco e così via.</span><span class="sxs-lookup"><span data-stu-id="d2439-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second list, and so on.</span></span> <span data-ttu-id="d2439-113">Se un bit specificato è 1, la finestra candidata corrispondente sta per essere modificata.</span><span class="sxs-lookup"><span data-stu-id="d2439-113">If a specified bit is 1, the corresponding candidate window is about to be changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2439-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2439-114">Return Value</span></span>

<span data-ttu-id="d2439-115">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="d2439-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2439-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2439-116">Remarks</span></span>

<span data-ttu-id="d2439-117">Un'applicazione deve elaborare questo comando se Visualizza i candidati stessi.</span><span class="sxs-lookup"><span data-stu-id="d2439-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="d2439-118">La finestra IME modifica l'aspetto della finestra candidata durante l'elaborazione del comando.</span><span class="sxs-lookup"><span data-stu-id="d2439-118">The IME window changes the appearance of the candidate window when it processes this command.</span></span> <span data-ttu-id="d2439-119">Un'applicazione può ottenere informazioni sulla finestra di sistema con [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) e [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span><span class="sxs-lookup"><span data-stu-id="d2439-119">An application can get information about the system window with the [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) and [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span></span>

## <a name="requirements"></a><span data-ttu-id="d2439-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2439-120">Requirements</span></span>



| <span data-ttu-id="d2439-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2439-121">Requirement</span></span> | <span data-ttu-id="d2439-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d2439-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2439-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2439-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d2439-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2439-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d2439-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2439-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d2439-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2439-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d2439-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2439-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2439-128"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2439-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2439-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2439-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2439-130">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="d2439-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d2439-131">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="d2439-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d2439-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="d2439-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="d2439-133">**ImmGetCandidateListCount**</span><span class="sxs-lookup"><span data-stu-id="d2439-133">**ImmGetCandidateListCount**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[<span data-ttu-id="d2439-134">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d2439-134">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




