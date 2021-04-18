---
description: Notifica a un'applicazione quando un IME sta per chiudere la finestra di stato. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: Codice di notifica IMN_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0347fb4b0d83a9e3891b9aea59d82ab81e2183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312865"
---
# <a name="imn_closestatuswindow-notification-code"></a><span data-ttu-id="cc1c1-104">\_Codice di notifica CLOSESTATUSWINDOW di IMN</span><span class="sxs-lookup"><span data-stu-id="cc1c1-104">IMN\_CLOSESTATUSWINDOW notification code</span></span>

<span data-ttu-id="cc1c1-105">Notifica a un'applicazione quando un IME sta per chiudere la finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="cc1c1-105">Notifies an application when an IME is about to close the status window.</span></span> <span data-ttu-id="cc1c1-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="cc1c1-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="cc1c1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc1c1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc1c1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc1c1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="cc1c1-109">Impostare su IMN \_ CLOSESTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="cc1c1-109">Set to IMN\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="cc1c1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc1c1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="cc1c1-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="cc1c1-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc1c1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc1c1-112">Return Value</span></span>

<span data-ttu-id="cc1c1-113">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="cc1c1-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc1c1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc1c1-114">Remarks</span></span>

<span data-ttu-id="cc1c1-115">Un'applicazione deve elaborare questo comando se Visualizza la finestra di stato per l'IME.</span><span class="sxs-lookup"><span data-stu-id="cc1c1-115">An application should process this command if it displays the status window for the IME.</span></span>

<span data-ttu-id="cc1c1-116">La finestra IME chiude la finestra di stato durante l'elaborazione del comando.</span><span class="sxs-lookup"><span data-stu-id="cc1c1-116">The IME window closes the status window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc1c1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc1c1-117">Requirements</span></span>



| <span data-ttu-id="cc1c1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc1c1-118">Requirement</span></span> | <span data-ttu-id="cc1c1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="cc1c1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1c1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc1c1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cc1c1-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cc1c1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cc1c1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc1c1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cc1c1-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cc1c1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cc1c1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc1c1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc1c1-125"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c1-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc1c1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc1c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc1c1-127">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="cc1c1-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="cc1c1-128">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="cc1c1-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="cc1c1-129">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cc1c1-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




