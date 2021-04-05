---
description: Indica a una finestra IME di ottenere la posizione della finestra di composizione. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: d2c60974-a602-4a42-8a45-870ee39df001
title: Comando IMC_GETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32b8f4414311d0727f622a1b552428cd31b0716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752343"
---
# <a name="imc_getcompositionwindow-command"></a><span data-ttu-id="ed35f-104">\_Comando GETCOMPOSITIONWINDOW IMC</span><span class="sxs-lookup"><span data-stu-id="ed35f-104">IMC\_GETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="ed35f-105">Indica a una finestra IME di ottenere la posizione della finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="ed35f-105">Instructs an IME window to get the position of the composition window.</span></span> <span data-ttu-id="ed35f-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="ed35f-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="ed35f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed35f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed35f-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed35f-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="ed35f-109">Impostare su IMC \_ GETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="ed35f-109">Set to IMC\_GETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="ed35f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed35f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ed35f-111">Puntatore a una struttura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) che contiene la posizione della finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="ed35f-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the position of the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed35f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed35f-112">Return Value</span></span>

<span data-ttu-id="ed35f-113">Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="ed35f-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed35f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed35f-114">Remarks</span></span>

<span data-ttu-id="ed35f-115">Poiché l'IME potrebbe modificare la posizione di una finestra di composizione, un'applicazione utilizza questo comando per ottenere la posizione effettiva per decidere se riposizionare la finestra.</span><span class="sxs-lookup"><span data-stu-id="ed35f-115">Because the IME might adjust the position of a composition window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="ed35f-116">La posizione recuperata è nelle coordinate della finestra rispetto alla finestra con lo stato attivo per l'input corrente.</span><span class="sxs-lookup"><span data-stu-id="ed35f-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed35f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed35f-117">Requirements</span></span>



| <span data-ttu-id="ed35f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed35f-118">Requirement</span></span> | <span data-ttu-id="ed35f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ed35f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed35f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed35f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed35f-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed35f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ed35f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed35f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed35f-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed35f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ed35f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed35f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed35f-125"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed35f-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed35f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed35f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed35f-127">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="ed35f-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="ed35f-128">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="ed35f-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="ed35f-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="ed35f-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> </dl>

 

 




