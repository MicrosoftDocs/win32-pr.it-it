---
title: Codice di notifica TCN_KEYDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo struttura a schede che è stato premuto un tasto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- Controlli di Windows per il codice di notifica TCN_KEYDOWN
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300964"
---
# <a name="tcn_keydown-notification-code"></a><span data-ttu-id="d8e8e-105">\_Codice di notifica KeyDown TCN</span><span class="sxs-lookup"><span data-stu-id="d8e8e-105">TCN\_KEYDOWN notification code</span></span>

<span data-ttu-id="d8e8e-106">Notifica alla finestra padre di un controllo struttura a schede che è stato premuto un tasto.</span><span class="sxs-lookup"><span data-stu-id="d8e8e-106">Notifies a tab control's parent window that a key has been pressed.</span></span> <span data-ttu-id="d8e8e-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8e8e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d8e8e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8e8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8e8e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8e8e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8e8e-110">Puntatore a una struttura [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) .</span><span class="sxs-lookup"><span data-stu-id="d8e8e-110">Pointer to an [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8e8e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8e8e-111">Return value</span></span>

<span data-ttu-id="d8e8e-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d8e8e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e8e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8e8e-113">Requirements</span></span>



| <span data-ttu-id="d8e8e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8e8e-114">Requirement</span></span> | <span data-ttu-id="d8e8e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d8e8e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e8e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8e8e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d8e8e-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8e8e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8e8e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8e8e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d8e8e-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8e8e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8e8e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8e8e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8e8e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8e8e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





