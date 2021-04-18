---
description: Notifica a un'applicazione quando un IME sta per creare la finestra di stato. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: Codice di notifica IMN_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312864"
---
# <a name="imn_openstatuswindow-notification-code"></a><span data-ttu-id="f8cd1-104">\_Codice di notifica OPENSTATUSWINDOW di IMN</span><span class="sxs-lookup"><span data-stu-id="f8cd1-104">IMN\_OPENSTATUSWINDOW notification code</span></span>

<span data-ttu-id="f8cd1-105">Notifica a un'applicazione quando un IME sta per creare la finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="f8cd1-105">Notifies an application when an IME is about to create the status window.</span></span> <span data-ttu-id="f8cd1-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f8cd1-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="f8cd1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8cd1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8cd1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8cd1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f8cd1-109">Impostare su IMN \_ OPENSTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="f8cd1-109">Set to IMN\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="f8cd1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8cd1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f8cd1-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f8cd1-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8cd1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8cd1-112">Return Value</span></span>

<span data-ttu-id="f8cd1-113">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="f8cd1-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8cd1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8cd1-114">Remarks</span></span>

<span data-ttu-id="f8cd1-115">Un'applicazione elabora questo comando per visualizzare la finestra di stato per l'IME.</span><span class="sxs-lookup"><span data-stu-id="f8cd1-115">An application processes this command to display the status window for the IME by itself.</span></span>

<span data-ttu-id="f8cd1-116">La finestra IME crea una finestra di stato durante l'elaborazione del comando e imposta le stringhe da visualizzare nella finestra di nel contesto di input.</span><span class="sxs-lookup"><span data-stu-id="f8cd1-116">The IME window creates a status window when it processes this command and sets the strings to display in the window into the input context.</span></span> <span data-ttu-id="f8cd1-117">Le applicazioni possono ottenere informazioni sulla finestra di stato tramite la funzione [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="f8cd1-117">Applications can get information about the status window by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8cd1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8cd1-118">Requirements</span></span>



| <span data-ttu-id="f8cd1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8cd1-119">Requirement</span></span> | <span data-ttu-id="f8cd1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f8cd1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8cd1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8cd1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f8cd1-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8cd1-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f8cd1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8cd1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f8cd1-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8cd1-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f8cd1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8cd1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8cd1-126"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8cd1-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8cd1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8cd1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8cd1-128">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="f8cd1-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f8cd1-129">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="f8cd1-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="f8cd1-130">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="f8cd1-130">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="f8cd1-131">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f8cd1-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




