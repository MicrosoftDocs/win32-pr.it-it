---
description: Notifica a un'applicazione quando viene aggiornata la modalità di conversione del contesto di input. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: Codice di notifica IMN_SETCONVERSIONMODE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c0ba945b9988ddb32d86c2005ec240c16f82ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317147"
---
# <a name="imn_setconversionmode-notification-code"></a><span data-ttu-id="65ac8-104">\_Codice di notifica SETCONVERSIONMODE di IMN</span><span class="sxs-lookup"><span data-stu-id="65ac8-104">IMN\_SETCONVERSIONMODE notification code</span></span>

<span data-ttu-id="65ac8-105">Notifica a un'applicazione quando viene aggiornata la modalità di conversione del contesto di input.</span><span class="sxs-lookup"><span data-stu-id="65ac8-105">Notifies an application when the conversion mode of the input context is updated.</span></span> <span data-ttu-id="65ac8-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="65ac8-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a><span data-ttu-id="65ac8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="65ac8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ac8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="65ac8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="65ac8-109">Impostare su IMN \_ SETCONVERSIONMODE.</span><span class="sxs-lookup"><span data-stu-id="65ac8-109">Set to IMN\_SETCONVERSIONMODE.</span></span>

</dd> <dt>

<span data-ttu-id="65ac8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="65ac8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="65ac8-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="65ac8-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ac8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65ac8-112">Return Value</span></span>

<span data-ttu-id="65ac8-113">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="65ac8-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65ac8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="65ac8-114">Remarks</span></span>

<span data-ttu-id="65ac8-115">L'applicazione può ottenere informazioni sulla modalità di conversione tramite la funzione [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="65ac8-115">The application can get information about the conversion mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ac8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65ac8-116">Requirements</span></span>



| <span data-ttu-id="65ac8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65ac8-117">Requirement</span></span> | <span data-ttu-id="65ac8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="65ac8-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ac8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65ac8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65ac8-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65ac8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="65ac8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65ac8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65ac8-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65ac8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="65ac8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65ac8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ac8-124"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65ac8-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ac8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65ac8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ac8-126">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="65ac8-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="65ac8-127">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="65ac8-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="65ac8-128">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="65ac8-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="65ac8-129">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="65ac8-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




