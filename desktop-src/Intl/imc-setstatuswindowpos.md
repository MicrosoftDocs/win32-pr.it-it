---
description: Indica a una finestra IME di impostare la posizione della finestra di stato. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Comando IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049561"
---
# <a name="imc_setstatuswindowpos-command"></a><span data-ttu-id="16658-104">\_Comando SETSTATUSWINDOWPOS IMC</span><span class="sxs-lookup"><span data-stu-id="16658-104">IMC\_SETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="16658-105">Indica a una finestra IME di impostare la posizione della finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="16658-105">Instructs an IME window to set the position of the status window.</span></span> <span data-ttu-id="16658-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="16658-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="16658-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="16658-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16658-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="16658-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="16658-109">Impostare su IMC \_ SETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="16658-109">Set to IMC\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="16658-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="16658-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="16658-111">Puntatore a una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene la coordinata x e la coordinata y della posizione della finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="16658-111">Pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the position of the status window.</span></span> <span data-ttu-id="16658-112">Le coordinate sono espresse in coordinate dello schermo, rispetto all'angolo superiore sinistro della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="16658-112">The coordinates are in screen coordinates, relative to the upper left corner of the display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16658-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16658-113">Return Value</span></span>

<span data-ttu-id="16658-114">Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="16658-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="16658-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16658-115">Requirements</span></span>



| <span data-ttu-id="16658-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="16658-116">Requirement</span></span> | <span data-ttu-id="16658-117">Valore</span><span class="sxs-lookup"><span data-stu-id="16658-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16658-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16658-118">Minimum supported client</span></span><br/> | <span data-ttu-id="16658-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="16658-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="16658-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16658-120">Minimum supported server</span></span><br/> | <span data-ttu-id="16658-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="16658-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="16658-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16658-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="16658-123"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16658-123"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16658-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16658-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16658-125">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="16658-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="16658-126">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="16658-126">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="16658-127">**\_controllo IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="16658-127">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
