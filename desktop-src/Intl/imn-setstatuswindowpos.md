---
description: Notifica a un'applicazione quando viene aggiornata la posizione della finestra di stato nel contesto di input. L'applicazione riceve questo comando tramite il \_ messaggio di \_ notifica di WM IME con le impostazioni dei parametri come indicato di seguito.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: Codice di notifica IMN_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d76a962e9cc509a6f9ffaac900b761b868f960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311761"
---
# <a name="imn_setstatuswindowpos-notification-code"></a><span data-ttu-id="380c9-104">\_Codice di notifica SETSTATUSWINDOWPOS di IMN</span><span class="sxs-lookup"><span data-stu-id="380c9-104">IMN\_SETSTATUSWINDOWPOS notification code</span></span>

<span data-ttu-id="380c9-105">Notifica a un'applicazione quando viene aggiornata la posizione della finestra di stato nel contesto di input.</span><span class="sxs-lookup"><span data-stu-id="380c9-105">Notifies an application when the status window position in the input context is updated.</span></span> <span data-ttu-id="380c9-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica di WM IME**](wm-ime-notify.md) con le impostazioni dei parametri come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="380c9-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as follows.</span></span>


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="380c9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="380c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380c9-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="380c9-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="380c9-109">Impostare su IMN \_ SETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="380c9-109">Set to IMN\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="380c9-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="380c9-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="380c9-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="380c9-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="380c9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="380c9-112">Return Value</span></span>

<span data-ttu-id="380c9-113">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="380c9-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="380c9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="380c9-114">Remarks</span></span>

<span data-ttu-id="380c9-115">L'applicazione può ottenere informazioni sulla posizione della finestra di stato usando il comando [**IMC \_ GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) .</span><span class="sxs-lookup"><span data-stu-id="380c9-115">The application can get information about the status window position by using the [**IMC\_GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="380c9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="380c9-116">Requirements</span></span>



| <span data-ttu-id="380c9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="380c9-117">Requirement</span></span> | <span data-ttu-id="380c9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="380c9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="380c9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="380c9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="380c9-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="380c9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="380c9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="380c9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="380c9-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="380c9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="380c9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="380c9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="380c9-124"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="380c9-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="380c9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="380c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380c9-126">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="380c9-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="380c9-127">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="380c9-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="380c9-128">**\_GETSTATUSWINDOWPOS IMC**</span><span class="sxs-lookup"><span data-stu-id="380c9-128">**IMC\_GETSTATUSWINDOWPOS**</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="380c9-129">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="380c9-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




