---
description: Notifica a un'applicazione quando viene aggiornato il tipo di carattere del contesto di input. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: Codice di notifica IMN_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8373954e80e420004b347bf1b40021c86ddbb876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317150"
---
# <a name="imn_setcompositionfont-notification-code"></a><span data-ttu-id="1d1d5-104">\_Codice di notifica SETCOMPOSITIONFONT di IMN</span><span class="sxs-lookup"><span data-stu-id="1d1d5-104">IMN\_SETCOMPOSITIONFONT notification code</span></span>

<span data-ttu-id="1d1d5-105">Notifica a un'applicazione quando viene aggiornato il tipo di carattere del contesto di input.</span><span class="sxs-lookup"><span data-stu-id="1d1d5-105">Notifies an application when the font of the input context is updated.</span></span> <span data-ttu-id="1d1d5-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="1d1d5-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="1d1d5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d1d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d1d5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d1d5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="1d1d5-109">Impostare su IMN \_ SETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="1d1d5-109">Set to IMN\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="1d1d5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d1d5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1d1d5-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="1d1d5-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d1d5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d1d5-112">Return Value</span></span>

<span data-ttu-id="1d1d5-113">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="1d1d5-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d1d5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d1d5-114">Remarks</span></span>

<span data-ttu-id="1d1d5-115">L'applicazione può ottenere informazioni sul tipo di carattere tramite la funzione [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) .</span><span class="sxs-lookup"><span data-stu-id="1d1d5-115">The application can get information about the font by using the [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) function.</span></span> <span data-ttu-id="1d1d5-116">La finestra IME utilizza successivamente il tipo di carattere per creare la stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="1d1d5-116">The IME window subsequently uses the font to draw the composition string.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d1d5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d1d5-117">Requirements</span></span>



| <span data-ttu-id="1d1d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d1d5-118">Requirement</span></span> | <span data-ttu-id="1d1d5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1d1d5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d1d5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d1d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d1d5-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d1d5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1d1d5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d1d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d1d5-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d1d5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1d1d5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d1d5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d1d5-125"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d1d5-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d1d5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d1d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d1d5-127">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="1d1d5-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1d1d5-128">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="1d1d5-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="1d1d5-129">**ImmGetCompositionFont**</span><span class="sxs-lookup"><span data-stu-id="1d1d5-129">**ImmGetCompositionFont**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[<span data-ttu-id="1d1d5-130">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="1d1d5-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




