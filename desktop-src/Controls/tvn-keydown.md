---
title: Codice di notifica TVN_KEYDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha premuto una chiave e che il controllo di visualizzazione albero ha lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- Controlli di Windows per il codice di notifica TVN_KEYDOWN
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475124"
---
# <a name="tvn_keydown-notification-code"></a><span data-ttu-id="a0ce8-105">Codice di notifica di TVN \_ KeyDown</span><span class="sxs-lookup"><span data-stu-id="a0ce8-105">TVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="a0ce8-106">Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha premuto una chiave e che il controllo di visualizzazione albero ha lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-106">Notifies a tree-view control's parent window that the user pressed a key and the tree-view control has the input focus.</span></span> <span data-ttu-id="a0ce8-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a0ce8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a><span data-ttu-id="a0ce8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0ce8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ce8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0ce8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0ce8-110">Puntatore a una struttura [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="a0ce8-110">Pointer to an [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) structure.</span></span> <span data-ttu-id="a0ce8-111">Il membro **wVKey** specifica il codice della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-111">The **wVKey** member specifies the virtual key code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0ce8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0ce8-112">Return value</span></span>

<span data-ttu-id="a0ce8-113">Se il membro **wVKey** di *lParam* è un codice del tasto carattere, il carattere verrà utilizzato come parte di una ricerca incrementale.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-113">If the **wVKey** member of *lParam* is a character key code, the character will be used as part of an incremental search.</span></span> <span data-ttu-id="a0ce8-114">Restituisce un valore diverso da zero per escludere il carattere dalla ricerca incrementale oppure zero per includere il carattere nella ricerca.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-114">Return nonzero to exclude the character from the incremental search, or zero to include the character in the search.</span></span> <span data-ttu-id="a0ce8-115">Per tutte le altre chiavi, il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-115">For all other keys, the return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0ce8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0ce8-116">Requirements</span></span>



| <span data-ttu-id="a0ce8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0ce8-117">Requirement</span></span> | <span data-ttu-id="a0ce8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a0ce8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ce8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0ce8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ce8-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0ce8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0ce8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0ce8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ce8-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0ce8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0ce8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0ce8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0ce8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0ce8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





