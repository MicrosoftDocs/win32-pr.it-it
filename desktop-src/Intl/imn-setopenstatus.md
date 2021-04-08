---
description: Notifica a un'applicazione quando viene aggiornato lo stato aperto del contesto di input. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: Codice di notifica IMN_SETOPENSTATUS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3598d7415cf415de3279e016d81a6d14b767d5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049994"
---
# <a name="imn_setopenstatus-notification-code"></a><span data-ttu-id="b72ac-104">\_Codice di notifica SETOPENSTATUS di IMN</span><span class="sxs-lookup"><span data-stu-id="b72ac-104">IMN\_SETOPENSTATUS notification code</span></span>

<span data-ttu-id="b72ac-105">Notifica a un'applicazione quando viene aggiornato lo stato aperto del contesto di input.</span><span class="sxs-lookup"><span data-stu-id="b72ac-105">Notifies an application when the open status of the input context is updated.</span></span> <span data-ttu-id="b72ac-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b72ac-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a><span data-ttu-id="b72ac-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b72ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b72ac-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b72ac-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b72ac-109">Impostare su IMN \_ SETOPENSTATUS.</span><span class="sxs-lookup"><span data-stu-id="b72ac-109">Set to IMN\_SETOPENSTATUS.</span></span>

</dd> <dt>

<span data-ttu-id="b72ac-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b72ac-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b72ac-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b72ac-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b72ac-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b72ac-112">Return Value</span></span>

<span data-ttu-id="b72ac-113">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="b72ac-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b72ac-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b72ac-114">Remarks</span></span>

<span data-ttu-id="b72ac-115">L'applicazione può ottenere informazioni sullo stato aperto tramite la funzione [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) .</span><span class="sxs-lookup"><span data-stu-id="b72ac-115">The application can get information about the open status by using the [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b72ac-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b72ac-116">Requirements</span></span>



| <span data-ttu-id="b72ac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b72ac-117">Requirement</span></span> | <span data-ttu-id="b72ac-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b72ac-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b72ac-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b72ac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b72ac-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b72ac-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b72ac-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b72ac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b72ac-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b72ac-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b72ac-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b72ac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b72ac-124"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b72ac-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b72ac-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b72ac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72ac-126">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="b72ac-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b72ac-127">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="b72ac-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="b72ac-128">**ImmGetOpenStatus**</span><span class="sxs-lookup"><span data-stu-id="b72ac-128">**ImmGetOpenStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[<span data-ttu-id="b72ac-129">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="b72ac-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




