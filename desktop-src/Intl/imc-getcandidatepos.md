---
description: Indica a una finestra IME di ottenere la posizione della finestra candidata. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: Comando IMC_GETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb5cd143bf45f9bdb37be4cbe3078a483f53db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319989"
---
# <a name="imc_getcandidatepos-command"></a><span data-ttu-id="9af66-104">\_Comando GETCANDIDATEPOS IMC</span><span class="sxs-lookup"><span data-stu-id="9af66-104">IMC\_GETCANDIDATEPOS command</span></span>

<span data-ttu-id="9af66-105">Indica a una finestra IME di ottenere la posizione della finestra candidata.</span><span class="sxs-lookup"><span data-stu-id="9af66-105">Instructs an IME window to get the position of the candidate window.</span></span> <span data-ttu-id="9af66-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="9af66-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="9af66-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9af66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af66-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="9af66-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="9af66-109">Impostare su IMC \_ GETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="9af66-109">Set to IMC\_GETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="9af66-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="9af66-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9af66-111">Puntatore a una struttura [**Campo CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) che contiene la posizione della finestra candidata.</span><span class="sxs-lookup"><span data-stu-id="9af66-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the position of the candidate window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af66-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9af66-112">Return Value</span></span>

<span data-ttu-id="9af66-113">Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="9af66-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9af66-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9af66-114">Remarks</span></span>

<span data-ttu-id="9af66-115">Poiché l'IME potrebbe modificare la posizione di una finestra candidata, un'applicazione utilizza questo comando per ottenere la posizione effettiva per decidere se riposizionare la finestra.</span><span class="sxs-lookup"><span data-stu-id="9af66-115">Because the IME might adjust the position of a candidate window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="9af66-116">La posizione recuperata è nelle coordinate della finestra rispetto alla finestra con lo stato attivo per l'input corrente.</span><span class="sxs-lookup"><span data-stu-id="9af66-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="9af66-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9af66-117">Requirements</span></span>



| <span data-ttu-id="9af66-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af66-118">Requirement</span></span> | <span data-ttu-id="9af66-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9af66-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af66-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9af66-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9af66-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9af66-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9af66-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9af66-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9af66-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9af66-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9af66-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9af66-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af66-125"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9af66-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af66-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9af66-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af66-127">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="9af66-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="9af66-128">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="9af66-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="9af66-129">**Campo CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="9af66-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




