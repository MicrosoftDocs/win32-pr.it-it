---
description: Notifica a un'applicazione l'aggiornamento dello stile o della posizione della finestra di composizione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: Codice di notifica IMN_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a1a4e989fb36049168359f86f85ee7a58103a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968318"
---
# <a name="imn_setcompositionwindow-notification-code"></a><span data-ttu-id="4f744-104">\_Codice di notifica SETCOMPOSITIONWINDOW di IMN</span><span class="sxs-lookup"><span data-stu-id="4f744-104">IMN\_SETCOMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="4f744-105">Notifica a un'applicazione l'aggiornamento dello stile o della posizione della finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="4f744-105">Notifies an application when the style or position of the composition window is updated.</span></span> <span data-ttu-id="4f744-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4f744-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="4f744-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f744-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f744-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f744-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="4f744-109">Impostare su IMN \_ SETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="4f744-109">Set to IMN\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="4f744-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f744-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4f744-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4f744-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f744-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f744-112">Return Value</span></span>

<span data-ttu-id="4f744-113">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="4f744-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f744-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f744-114">Remarks</span></span>

<span data-ttu-id="4f744-115">L'applicazione può ottenere informazioni sul form di composizione usando il comando [**IMC \_ GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) .</span><span class="sxs-lookup"><span data-stu-id="4f744-115">The application can get information about the composition form by using the [**IMC\_GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f744-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f744-116">Requirements</span></span>



| <span data-ttu-id="4f744-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f744-117">Requirement</span></span> | <span data-ttu-id="4f744-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4f744-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f744-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f744-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4f744-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f744-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4f744-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f744-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4f744-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f744-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4f744-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f744-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f744-124"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f744-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f744-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f744-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f744-126">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="4f744-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4f744-127">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="4f744-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="4f744-128">**\_GETCOMPOSITIONWINDOW IMC**</span><span class="sxs-lookup"><span data-stu-id="4f744-128">**IMC\_GETCOMPOSITIONWINDOW**</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="4f744-129">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="4f744-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




