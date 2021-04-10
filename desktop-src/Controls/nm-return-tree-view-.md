---
title: Codice di notifica di NM_RETURN (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e4a048ec-4643-458a-bf75-f5b08163d6c6
keywords:
- NM_RETURN (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0abf3152a9236103301f1c74acfcac69d43f07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964643"
---
# <a name="nm_return-tree-view-notification-code"></a><span data-ttu-id="5efe6-105">\_Codice di notifica restituito da Nm (visualizzazione albero)</span><span class="sxs-lookup"><span data-stu-id="5efe6-105">NM\_RETURN (tree view) notification code</span></span>

<span data-ttu-id="5efe6-106">Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto.</span><span class="sxs-lookup"><span data-stu-id="5efe6-106">Notifies a tree-view control's parent window that the control has the input focus and that the user has pressed the key.</span></span> <span data-ttu-id="5efe6-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5efe6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5efe6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5efe6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5efe6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5efe6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5efe6-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="5efe6-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5efe6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5efe6-111">Return value</span></span>

<span data-ttu-id="5efe6-112">Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5efe6-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5efe6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5efe6-113">Requirements</span></span>



| <span data-ttu-id="5efe6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5efe6-114">Requirement</span></span> | <span data-ttu-id="5efe6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5efe6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5efe6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5efe6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5efe6-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5efe6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5efe6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5efe6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5efe6-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5efe6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5efe6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5efe6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5efe6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5efe6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





