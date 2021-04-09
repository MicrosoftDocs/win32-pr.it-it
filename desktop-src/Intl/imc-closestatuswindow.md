---
description: Indica alla finestra IME di nascondere la finestra di stato. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: Comando IMC_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885859"
---
# <a name="imc_closestatuswindow-command"></a><span data-ttu-id="d2440-104">\_Comando CLOSESTATUSWINDOW IMC</span><span class="sxs-lookup"><span data-stu-id="d2440-104">IMC\_CLOSESTATUSWINDOW command</span></span>

<span data-ttu-id="d2440-105">Indica alla finestra IME di nascondere la finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="d2440-105">Instructs the IME window to hide the status window.</span></span> <span data-ttu-id="d2440-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="d2440-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="d2440-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2440-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2440-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2440-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d2440-109">Impostare su IMC \_ CLOSESTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="d2440-109">Set to IMC\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="d2440-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2440-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d2440-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d2440-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2440-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2440-112">Return Value</span></span>

<span data-ttu-id="d2440-113">Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="d2440-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2440-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2440-114">Remarks</span></span>

<span data-ttu-id="d2440-115">Quando la finestra di stato IME è già nascosta, questo comando non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="d2440-115">When the IME status window is already hidden, this command does nothing.</span></span> <span data-ttu-id="d2440-116">Sebbene un'applicazione possa inviare questo comando alla finestra IME, l'applicazione non riceve il corrispondente comando [IMN \_ CLOSESTATUSWINDOW](imn-closestatuswindow.md) .</span><span class="sxs-lookup"><span data-stu-id="d2440-116">Although an application can send this command to the IME window, the application does not receive the corresponding [IMN\_CLOSESTATUSWINDOW](imn-closestatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2440-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2440-117">Requirements</span></span>



| <span data-ttu-id="d2440-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2440-118">Requirement</span></span> | <span data-ttu-id="d2440-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d2440-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2440-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2440-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2440-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2440-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d2440-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2440-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2440-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2440-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d2440-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2440-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2440-125"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2440-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2440-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2440-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2440-127">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="d2440-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d2440-128">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="d2440-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 




