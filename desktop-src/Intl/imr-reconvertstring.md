---
description: Notifica a un'applicazione quando per un IME selezionato è necessaria una stringa per la riconversione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: Codice di notifica IMR_RECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881526"
---
# <a name="imr_reconvertstring-notification-code"></a><span data-ttu-id="7a176-104">\_Codice di notifica RECONVERTSTRING di IMR</span><span class="sxs-lookup"><span data-stu-id="7a176-104">IMR\_RECONVERTSTRING notification code</span></span>

<span data-ttu-id="7a176-105">Notifica a un'applicazione quando per un IME selezionato è necessaria una stringa per la riconversione.</span><span class="sxs-lookup"><span data-stu-id="7a176-105">Notifies an application when a selected IME needs a string for reconversion.</span></span> <span data-ttu-id="7a176-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="7a176-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="7a176-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a176-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a176-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a176-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="7a176-109">Impostare su IMR \_ RECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="7a176-109">Set to IMR\_RECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="7a176-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a176-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7a176-111">Puntatore a un buffer contenente la struttura e le stringhe [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="7a176-111">Pointer to a buffer containing the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure and strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a176-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a176-112">Return Value</span></span>

<span data-ttu-id="7a176-113">Restituisce la struttura della stringa di riconversione corrente.</span><span class="sxs-lookup"><span data-stu-id="7a176-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="7a176-114">Se *lParam* è impostato su **null**, l'applicazione restituisce la dimensione per il buffer necessario per mantenere la struttura.</span><span class="sxs-lookup"><span data-stu-id="7a176-114">If *lParam* is set to **NULL**, the application returns the size for the buffer required to hold the structure.</span></span> <span data-ttu-id="7a176-115">Se l'operazione non riesce, il comando restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="7a176-115">The command returns 0 if it does not succeed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a176-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a176-116">Requirements</span></span>



| <span data-ttu-id="7a176-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a176-117">Requirement</span></span> | <span data-ttu-id="7a176-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7a176-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a176-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a176-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a176-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7a176-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7a176-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a176-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a176-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7a176-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7a176-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a176-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a176-124"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a176-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a176-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a176-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a176-126">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="7a176-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="7a176-127">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="7a176-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="7a176-128">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="7a176-128">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="7a176-129">**\_richiesta IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="7a176-129">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




