---
title: Codice di notifica NM_KEYDOWN (barra degli strumenti) (COMmctrl. h)
description: Inviato da un controllo quando il controllo ha lo stato attivo della tastiera e l'utente preme un tasto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- Codice di notifica di NM_KEYDOWN (barra degli strumenti) controlli Windows
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
ms.openlocfilehash: e7326946a8234122c81b2fd057dab0ad313d49a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047850"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="af8ae-105">\_Codice di notifica della barra degli strumenti (Toolbar) Nm</span><span class="sxs-lookup"><span data-stu-id="af8ae-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="af8ae-106">Inviato da un controllo quando il controllo ha lo stato attivo della tastiera e l'utente preme un tasto.</span><span class="sxs-lookup"><span data-stu-id="af8ae-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="af8ae-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="af8ae-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="af8ae-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="af8ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af8ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af8ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af8ae-110">Puntatore a una struttura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) che contiene informazioni aggiuntive sulla chiave che ha causato il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="af8ae-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af8ae-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af8ae-111">Return value</span></span>

<span data-ttu-id="af8ae-112">Restituisce un valore diverso da zero per impedire l'elaborazione della chiave da parte del controllo. in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="af8ae-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="af8ae-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="af8ae-113">Remarks</span></span>

<span data-ttu-id="af8ae-114">Attualmente, solo il controllo Toolbar invia questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="af8ae-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af8ae-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af8ae-115">Requirements</span></span>



| <span data-ttu-id="af8ae-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af8ae-116">Requirement</span></span> | <span data-ttu-id="af8ae-117">Valore</span><span class="sxs-lookup"><span data-stu-id="af8ae-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af8ae-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af8ae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af8ae-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af8ae-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af8ae-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af8ae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af8ae-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af8ae-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af8ae-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af8ae-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af8ae-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8ae-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





