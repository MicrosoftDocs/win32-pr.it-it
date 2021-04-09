---
description: Indica alla finestra IME di visualizzare la finestra di stato. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: Comando IMC_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd0b5e19ef6a026459eedb050e9ac9587b5ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879569"
---
# <a name="imc_openstatuswindow-command"></a><span data-ttu-id="01c6d-104">\_Comando OPENSTATUSWINDOW IMC</span><span class="sxs-lookup"><span data-stu-id="01c6d-104">IMC\_OPENSTATUSWINDOW command</span></span>

<span data-ttu-id="01c6d-105">Indica alla finestra IME di visualizzare la finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="01c6d-105">Instructs the IME window to show the status window.</span></span> <span data-ttu-id="01c6d-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="01c6d-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="01c6d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="01c6d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01c6d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="01c6d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="01c6d-109">Impostare su IMC \_ OPENSTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="01c6d-109">Set to IMC\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="01c6d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="01c6d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="01c6d-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="01c6d-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01c6d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01c6d-112">Return Value</span></span>

<span data-ttu-id="01c6d-113">Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="01c6d-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="01c6d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="01c6d-114">Remarks</span></span>

<span data-ttu-id="01c6d-115">Questo comando viene ignorato se il sistema operativo non è nella modalità Mostra stato IME.</span><span class="sxs-lookup"><span data-stu-id="01c6d-115">This command is ignored if the operating system is not in the show IME status mode.</span></span> <span data-ttu-id="01c6d-116">L'utente può impostare o deselezionare la modalità Mostra stato IME dalla barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="01c6d-116">The user can set or clear the show IME status mode from the task bar.</span></span>

<span data-ttu-id="01c6d-117">Se la finestra di stato è già visualizzata, questo comando non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="01c6d-117">If the status window is already shown, this command does nothing.</span></span> <span data-ttu-id="01c6d-118">Sebbene l'applicazione possa inviare questo comando alla finestra IME, l'applicazione non riceve il corrispondente comando [**IMN \_ OPENSTATUSWINDOW**](imn-openstatuswindow.md) .</span><span class="sxs-lookup"><span data-stu-id="01c6d-118">Although the application can send this command to the IME window, the application does not receive the corresponding [**IMN\_OPENSTATUSWINDOW**](imn-openstatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c6d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01c6d-119">Requirements</span></span>



| <span data-ttu-id="01c6d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c6d-120">Requirement</span></span> | <span data-ttu-id="01c6d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="01c6d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c6d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01c6d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="01c6d-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01c6d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="01c6d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01c6d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="01c6d-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01c6d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="01c6d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01c6d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c6d-127"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01c6d-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c6d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01c6d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c6d-129">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="01c6d-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="01c6d-130">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="01c6d-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="01c6d-131">**\_controllo IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="01c6d-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




