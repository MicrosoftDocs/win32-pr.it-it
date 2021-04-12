---
description: Notifica a un'applicazione quando un IME sta per visualizzare un messaggio di errore o altre informazioni. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: Codice di notifica IMN_GUIDELINE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4efc222f7bfceadecce0f14573cab66471b119d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345766"
---
# <a name="imn_guideline-notification-code"></a><span data-ttu-id="75f07-104">\_Codice di notifica linee guida IMN</span><span class="sxs-lookup"><span data-stu-id="75f07-104">IMN\_GUIDELINE notification code</span></span>

<span data-ttu-id="75f07-105">Notifica a un'applicazione quando un IME sta per visualizzare un messaggio di errore o altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="75f07-105">Notifies an application when an IME is about to show an error message or other information.</span></span> <span data-ttu-id="75f07-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="75f07-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a><span data-ttu-id="75f07-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="75f07-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f07-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="75f07-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="75f07-109">Impostare sulla \_ linea guida IMN.</span><span class="sxs-lookup"><span data-stu-id="75f07-109">Set to IMN\_GUIDELINE.</span></span>

</dd> <dt>

<span data-ttu-id="75f07-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="75f07-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="75f07-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="75f07-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f07-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75f07-112">Return Value</span></span>

<span data-ttu-id="75f07-113">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="75f07-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75f07-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="75f07-114">Remarks</span></span>

<span data-ttu-id="75f07-115">Un'applicazione elabora questo comando chiamando la funzione [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) per recuperare il messaggio di errore o le informazioni dall'IME.</span><span class="sxs-lookup"><span data-stu-id="75f07-115">An application processes this command by calling the [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) function to retrieve the error message or information from the IME.</span></span>

<span data-ttu-id="75f07-116">Nella finestra IME viene visualizzato il messaggio di errore o la stringa di informazioni in una finestra informazioni.</span><span class="sxs-lookup"><span data-stu-id="75f07-116">The IME window displays the error message or information string in an information window.</span></span>

## <a name="requirements"></a><span data-ttu-id="75f07-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75f07-117">Requirements</span></span>



| <span data-ttu-id="75f07-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75f07-118">Requirement</span></span> | <span data-ttu-id="75f07-119">Valore</span><span class="sxs-lookup"><span data-stu-id="75f07-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75f07-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75f07-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75f07-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75f07-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="75f07-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75f07-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75f07-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75f07-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75f07-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75f07-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75f07-125"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75f07-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f07-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75f07-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f07-127">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="75f07-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="75f07-128">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="75f07-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="75f07-129">**ImmGetGuideLine**</span><span class="sxs-lookup"><span data-stu-id="75f07-129">**ImmGetGuideLine**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[<span data-ttu-id="75f07-130">**\_notifica IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="75f07-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




