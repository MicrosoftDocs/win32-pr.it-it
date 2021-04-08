---
title: Codice di notifica NM_KEYDOWN (COMmctrl. h)
description: Inviato da un controllo quando il controllo ha lo stato attivo della tastiera e l'utente preme un tasto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- Controlli di Windows per il codice di notifica NM_KEYDOWN
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 222a47733a60590e7d56ca0adba038164c430fab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873298"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="56442-105">\_Codice di notifica KeyDown di Nm</span><span class="sxs-lookup"><span data-stu-id="56442-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="56442-106">Inviato da un controllo quando il controllo ha lo stato attivo della tastiera e l'utente preme un tasto.</span><span class="sxs-lookup"><span data-stu-id="56442-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="56442-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="56442-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="56442-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="56442-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56442-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56442-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56442-110">Puntatore a una struttura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) che contiene informazioni aggiuntive sulla chiave che ha causato il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="56442-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56442-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56442-111">Return value</span></span>

<span data-ttu-id="56442-112">Restituisce un valore diverso da zero per impedire l'elaborazione della chiave da parte del controllo. in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="56442-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="56442-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56442-113">Requirements</span></span>



| <span data-ttu-id="56442-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="56442-114">Requirement</span></span> | <span data-ttu-id="56442-115">Valore</span><span class="sxs-lookup"><span data-stu-id="56442-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56442-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56442-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56442-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56442-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56442-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56442-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56442-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56442-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56442-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56442-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="56442-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56442-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





