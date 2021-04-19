---
description: Notifica a un'applicazione quando viene aggiornata la modalità di frase del contesto di input. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 72455193-cd17-45f8-b19c-a1f735ff81bf
title: Codice di notifica IMN_SETSENTENCEMODE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0130c5b3d7284112e64cca698b358650f51f3642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311762"
---
# <a name="imn_setsentencemode-notification-code"></a><span data-ttu-id="90ec4-104">\_Codice di notifica SETSENTENCEMODE di IMN</span><span class="sxs-lookup"><span data-stu-id="90ec4-104">IMN\_SETSENTENCEMODE notification code</span></span>

<span data-ttu-id="90ec4-105">Notifica a un'applicazione quando viene aggiornata la modalità di frase del contesto di input.</span><span class="sxs-lookup"><span data-stu-id="90ec4-105">Notifies an application when the sentence mode of the input context is updated.</span></span> <span data-ttu-id="90ec4-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="90ec4-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETSENTENCEMODE
```



## <a name="parameters"></a><span data-ttu-id="90ec4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="90ec4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ec4-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="90ec4-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="90ec4-109">Impostare su IMN \_ SETSENTENCEMODE.</span><span class="sxs-lookup"><span data-stu-id="90ec4-109">Set to IMN\_SETSENTENCEMODE.</span></span>

</dd> <dt>

<span data-ttu-id="90ec4-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="90ec4-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="90ec4-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="90ec4-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ec4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90ec4-112">Return Value</span></span>

<span data-ttu-id="90ec4-113">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="90ec4-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ec4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="90ec4-114">Remarks</span></span>

<span data-ttu-id="90ec4-115">L'applicazione può ottenere informazioni sulla modalità frase tramite la funzione [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="90ec4-115">The application can get information about the sentence mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="90ec4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90ec4-116">Requirements</span></span>



| <span data-ttu-id="90ec4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="90ec4-117">Requirement</span></span> | <span data-ttu-id="90ec4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="90ec4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ec4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90ec4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="90ec4-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90ec4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="90ec4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90ec4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="90ec4-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90ec4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="90ec4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90ec4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ec4-124"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90ec4-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ec4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90ec4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ec4-126">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="90ec4-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="90ec4-127">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="90ec4-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="90ec4-128">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="90ec4-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="90ec4-129">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="90ec4-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




