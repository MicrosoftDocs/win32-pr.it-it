---
title: Codice di notifica di NM_KILLFOCUS (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo ha perso lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: f6646a39-6480-4417-9c1c-ffd2417ca7dd
keywords:
- NM_KILLFOCUS (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7123f47469a02fcec92805a27d81e173c5e1d10a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963755"
---
# <a name="nm_killfocus-tree-view-notification-code"></a><span data-ttu-id="ef468-105">\_Codice di notifica di KILLFOCUS Nm (visualizzazione albero)</span><span class="sxs-lookup"><span data-stu-id="ef468-105">NM\_KILLFOCUS (tree view) notification code</span></span>

<span data-ttu-id="ef468-106">Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo ha perso lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="ef468-106">Notifies a tree-view control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="ef468-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ef468-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ef468-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef468-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef468-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef468-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef468-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="ef468-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef468-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef468-111">Return value</span></span>

<span data-ttu-id="ef468-112">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ef468-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef468-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef468-113">Requirements</span></span>



| <span data-ttu-id="ef468-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef468-114">Requirement</span></span> | <span data-ttu-id="ef468-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ef468-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef468-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef468-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef468-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef468-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef468-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef468-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef468-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef468-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef468-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef468-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef468-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef468-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





