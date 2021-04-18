---
description: Indica a una finestra IME di ottenere la posizione della finestra di stato. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: Comando IMC_GETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd17c5787d9ef8c787e62a556afa2f136bd65c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307863"
---
# <a name="imc_getstatuswindowpos-command"></a><span data-ttu-id="63703-104">\_Comando GETSTATUSWINDOWPOS IMC</span><span class="sxs-lookup"><span data-stu-id="63703-104">IMC\_GETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="63703-105">Indica a una finestra IME di ottenere la posizione della finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="63703-105">Instructs an IME window to get the position of the status window.</span></span> <span data-ttu-id="63703-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="63703-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="63703-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="63703-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63703-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="63703-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="63703-109">Impostare su IMC \_ GETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="63703-109">Set to IMC\_GETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="63703-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="63703-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="63703-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="63703-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63703-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63703-112">Return Value</span></span>

<span data-ttu-id="63703-113">Restituisce una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene la coordinata x e la coordinata y della posizione della finestra di stato nelle coordinate dello schermo, rispetto all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="63703-113">Returns a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the status window position in screen coordinates, relative to the upper left corner of the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="63703-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63703-114">Requirements</span></span>



| <span data-ttu-id="63703-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="63703-115">Requirement</span></span> | <span data-ttu-id="63703-116">Valore</span><span class="sxs-lookup"><span data-stu-id="63703-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63703-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63703-117">Minimum supported client</span></span><br/> | <span data-ttu-id="63703-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63703-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="63703-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63703-119">Minimum supported server</span></span><br/> | <span data-ttu-id="63703-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63703-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="63703-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63703-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="63703-122"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63703-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63703-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63703-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63703-124">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="63703-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="63703-125">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="63703-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="63703-126">**\_controllo IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="63703-126">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
