---
description: Notifica a un'applicazione quando un IME sta per aprire la finestra candidata. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: Evento IMN_OPENCANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f8f412c60cc6b62904e562d450479af642de0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882137"
---
# <a name="imn_opencandidate-event"></a><span data-ttu-id="70eb5-104">\_Evento OPENCANDIDATE IMN</span><span class="sxs-lookup"><span data-stu-id="70eb5-104">IMN\_OPENCANDIDATE event</span></span>

<span data-ttu-id="70eb5-105">Notifica a un'applicazione quando un IME sta per aprire la finestra candidata.</span><span class="sxs-lookup"><span data-stu-id="70eb5-105">Notifies an application when an IME is about to open the candidate window.</span></span> <span data-ttu-id="70eb5-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="70eb5-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="70eb5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="70eb5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70eb5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="70eb5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="70eb5-109">Impostare su IMN \_ OPENCANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="70eb5-109">Set to IMN\_OPENCANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="70eb5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="70eb5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="70eb5-111">Flag elenco candidati.</span><span class="sxs-lookup"><span data-stu-id="70eb5-111">Candidate list flag.</span></span> <span data-ttu-id="70eb5-112">Ogni bit corrisponde a un elenco di candidati: bit 0 per il primo elenco, bit 1 al secondo e così via.</span><span class="sxs-lookup"><span data-stu-id="70eb5-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="70eb5-113">Se un bit specificato è 1, la finestra candidata corrispondente sta per essere aperta.</span><span class="sxs-lookup"><span data-stu-id="70eb5-113">If a specified bit is 1, the corresponding candidate window is about to be opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70eb5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70eb5-114">Return Value</span></span>

<span data-ttu-id="70eb5-115">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="70eb5-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70eb5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="70eb5-116">Remarks</span></span>

<span data-ttu-id="70eb5-117">Un'applicazione deve elaborare questo comando se Visualizza i candidati stessi.</span><span class="sxs-lookup"><span data-stu-id="70eb5-117">An application should process this command if it displays candidates itself.</span></span> <span data-ttu-id="70eb5-118">L'applicazione può recuperare un elenco di candidati da visualizzare tramite la funzione [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .</span><span class="sxs-lookup"><span data-stu-id="70eb5-118">The application can retrieve a list of candidates to display by using the [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) function.</span></span>

<span data-ttu-id="70eb5-119">Per impostazione predefinita, la finestra IME crea una finestra candidata durante l'elaborazione del comando.</span><span class="sxs-lookup"><span data-stu-id="70eb5-119">By default, the IME window creates a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="70eb5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70eb5-120">Requirements</span></span>



| <span data-ttu-id="70eb5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="70eb5-121">Requirement</span></span> | <span data-ttu-id="70eb5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="70eb5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70eb5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70eb5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="70eb5-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70eb5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="70eb5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70eb5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="70eb5-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70eb5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70eb5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70eb5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="70eb5-128"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70eb5-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70eb5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70eb5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70eb5-130">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="70eb5-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="70eb5-131">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="70eb5-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="70eb5-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="70eb5-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="70eb5-133">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="70eb5-133">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




