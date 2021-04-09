---
description: Indica a una finestra IME di specificare il tipo di carattere logico da utilizzare per la visualizzazione dei caratteri intermedi nella finestra di composizione. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: Comando IMC_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb84c9e05ab19206064988a71b0ffc39b21a44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879566"
---
# <a name="imc_setcompositionfont-command"></a><span data-ttu-id="9a087-104">\_Comando SETCOMPOSITIONFONT IMC</span><span class="sxs-lookup"><span data-stu-id="9a087-104">IMC\_SETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="9a087-105">Indica a una finestra IME di specificare il tipo di carattere logico da utilizzare per la visualizzazione dei caratteri intermedi nella finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="9a087-105">Instructs an IME window to specify the logical font to use for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="9a087-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="9a087-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="9a087-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a087-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a087-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a087-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="9a087-109">Impostare su IMC \_ SETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="9a087-109">Set to IMC\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="9a087-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a087-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9a087-111">Puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che contiene informazioni sul tipo di carattere logico.</span><span class="sxs-lookup"><span data-stu-id="9a087-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a087-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a087-112">Return Value</span></span>

<span data-ttu-id="9a087-113">Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="9a087-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a087-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a087-114">Remarks</span></span>

<span data-ttu-id="9a087-115">Quando si elabora questo comando, la finestra IME modifica il tipo di carattere selezionato corrente nel contesto di input.</span><span class="sxs-lookup"><span data-stu-id="9a087-115">When processing this command, the IME window changes the current selected font in the input context.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a087-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a087-116">Requirements</span></span>



| <span data-ttu-id="9a087-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a087-117">Requirement</span></span> | <span data-ttu-id="9a087-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9a087-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a087-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a087-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9a087-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9a087-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9a087-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a087-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9a087-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9a087-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9a087-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a087-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a087-124"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a087-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a087-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a087-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a087-126">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="9a087-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="9a087-127">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="9a087-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="9a087-128">**\_controllo IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="9a087-128">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
