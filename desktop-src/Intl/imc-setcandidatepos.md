---
description: Indica a una finestra IME di impostare la posizione della finestra candidati. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: Comando IMC_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752346"
---
# <a name="imc_setcandidatepos-command"></a><span data-ttu-id="9378d-104">\_Comando SETCANDIDATEPOS IMC</span><span class="sxs-lookup"><span data-stu-id="9378d-104">IMC\_SETCANDIDATEPOS command</span></span>

<span data-ttu-id="9378d-105">Indica a una finestra IME di impostare la posizione della finestra candidati.</span><span class="sxs-lookup"><span data-stu-id="9378d-105">Instructs an IME window to set the position of the candidates window.</span></span> <span data-ttu-id="9378d-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="9378d-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="9378d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9378d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9378d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="9378d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="9378d-109">Impostare su IMC \_ SETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="9378d-109">Set to IMC\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="9378d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="9378d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9378d-111">Puntatore a una struttura [**Campo CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) che contiene la coordinata x e la coordinata y per la finestra candidati.</span><span class="sxs-lookup"><span data-stu-id="9378d-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the x coordinate and y coordinate for the candidates window.</span></span> <span data-ttu-id="9378d-112">L'applicazione deve impostare il membro **dwIndex** della struttura.</span><span class="sxs-lookup"><span data-stu-id="9378d-112">The application should set the **dwIndex** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9378d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9378d-113">Return Value</span></span>

<span data-ttu-id="9378d-114">Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="9378d-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9378d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9378d-115">Remarks</span></span>

<span data-ttu-id="9378d-116">Questo comando è destinato alle applicazioni che visualizzano i caratteri di composizione autonomamente, ma usano la finestra IME per visualizzare i candidati.</span><span class="sxs-lookup"><span data-stu-id="9378d-116">This command is intended for applications that display composition characters on their own but use the IME window to display candidates.</span></span>

## <a name="requirements"></a><span data-ttu-id="9378d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9378d-117">Requirements</span></span>



| <span data-ttu-id="9378d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9378d-118">Requirement</span></span> | <span data-ttu-id="9378d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9378d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9378d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9378d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9378d-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9378d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9378d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9378d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9378d-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9378d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9378d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9378d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9378d-125"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9378d-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9378d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9378d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9378d-127">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="9378d-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="9378d-128">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="9378d-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="9378d-129">**Campo CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="9378d-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="9378d-130">**\_controllo IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="9378d-130">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




