---
description: Notifica a un'applicazione quando un IME sta per chiudere la finestra candidati. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: Codice di notifica IMN_CLOSECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3414d2aa37a50b7f35f0dfb936b641b7c86a932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312871"
---
# <a name="imn_closecandidate-notification-code"></a><span data-ttu-id="46066-104">\_Codice di notifica CLOSECANDIDATE di IMN</span><span class="sxs-lookup"><span data-stu-id="46066-104">IMN\_CLOSECANDIDATE notification code</span></span>

<span data-ttu-id="46066-105">Notifica a un'applicazione quando un IME sta per chiudere la finestra candidati.</span><span class="sxs-lookup"><span data-stu-id="46066-105">Notifies an application when an IME is about to close the candidates window.</span></span> <span data-ttu-id="46066-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="46066-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="46066-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="46066-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46066-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="46066-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="46066-109">Impostare su IMN \_ CLOSECANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="46066-109">Set to IMN\_CLOSECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="46066-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="46066-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="46066-111">Flag elenco candidati.</span><span class="sxs-lookup"><span data-stu-id="46066-111">Candidate list flag.</span></span> <span data-ttu-id="46066-112">Ogni bit corrisponde a un elenco di candidati: bit 0 per il primo elenco, bit 1 al secondo e così via.</span><span class="sxs-lookup"><span data-stu-id="46066-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="46066-113">Se un bit specificato è 1, la finestra candidati corrispondente sta per essere chiusa.</span><span class="sxs-lookup"><span data-stu-id="46066-113">If a specified bit is 1, the corresponding candidates window is about to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46066-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46066-114">Return Value</span></span>

<span data-ttu-id="46066-115">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="46066-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46066-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="46066-116">Remarks</span></span>

<span data-ttu-id="46066-117">Un'applicazione deve elaborare questo comando se Visualizza i candidati stessi.</span><span class="sxs-lookup"><span data-stu-id="46066-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="46066-118">Per impostazione predefinita, la finestra IME Elimina una finestra candidata durante l'elaborazione del comando.</span><span class="sxs-lookup"><span data-stu-id="46066-118">By default, the IME window destroys a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="46066-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46066-119">Requirements</span></span>



| <span data-ttu-id="46066-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="46066-120">Requirement</span></span> | <span data-ttu-id="46066-121">Valore</span><span class="sxs-lookup"><span data-stu-id="46066-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46066-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46066-122">Minimum supported client</span></span><br/> | <span data-ttu-id="46066-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46066-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="46066-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46066-124">Minimum supported server</span></span><br/> | <span data-ttu-id="46066-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46066-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="46066-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46066-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="46066-127"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46066-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46066-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46066-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46066-129">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="46066-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="46066-130">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="46066-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="46066-131">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="46066-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




