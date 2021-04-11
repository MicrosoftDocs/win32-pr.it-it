---
description: Indica a una finestra IME di recuperare il tipo di carattere logico utilizzato per la visualizzazione dei caratteri intermedi nella finestra di composizione. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: Comando IMC_GETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226256"
---
# <a name="imc_getcompositionfont-command"></a><span data-ttu-id="8279a-104">\_Comando GETCOMPOSITIONFONT IMC</span><span class="sxs-lookup"><span data-stu-id="8279a-104">IMC\_GETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="8279a-105">Indica a una finestra IME di recuperare il tipo di carattere logico utilizzato per la visualizzazione dei caratteri intermedi nella finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="8279a-105">Instructs an IME window to retrieve the logical font used for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="8279a-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="8279a-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="8279a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8279a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8279a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="8279a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="8279a-109">Impostare su IMC \_ GETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="8279a-109">Set to IMC\_GETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="8279a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8279a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8279a-111">Puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che riceve informazioni sul tipo di carattere logico.</span><span class="sxs-lookup"><span data-stu-id="8279a-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8279a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8279a-112">Return Value</span></span>

<span data-ttu-id="8279a-113">Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="8279a-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8279a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8279a-114">Requirements</span></span>



| <span data-ttu-id="8279a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8279a-115">Requirement</span></span> | <span data-ttu-id="8279a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8279a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8279a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8279a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8279a-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8279a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8279a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8279a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8279a-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8279a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8279a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8279a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8279a-122"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8279a-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8279a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8279a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8279a-124">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="8279a-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="8279a-125">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="8279a-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 
