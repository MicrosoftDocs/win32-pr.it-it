---
title: Codice di notifica di NM_SETFOCUS (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo ha ricevuto lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 4bdd6cd2-afd3-4c0b-914b-8fff55e474a9
keywords:
- NM_SETFOCUS (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e24d95b95b3c66fe43920f780b2e8d0f66679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873929"
---
# <a name="nm_setfocus-tree-view-notification-code"></a><span data-ttu-id="a7cfd-105">\_Codice di notifica del SEFOCUS Nm (visualizzazione albero)</span><span class="sxs-lookup"><span data-stu-id="a7cfd-105">NM\_SETFOCUS (tree view) notification code</span></span>

<span data-ttu-id="a7cfd-106">Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo ha ricevuto lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="a7cfd-106">Notifies a tree-view control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="a7cfd-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a7cfd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a7cfd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7cfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7cfd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7cfd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cfd-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="a7cfd-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7cfd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7cfd-111">Return value</span></span>

<span data-ttu-id="a7cfd-112">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a7cfd-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7cfd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7cfd-113">Requirements</span></span>



| <span data-ttu-id="a7cfd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7cfd-114">Requirement</span></span> | <span data-ttu-id="a7cfd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a7cfd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cfd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7cfd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a7cfd-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7cfd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7cfd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7cfd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a7cfd-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7cfd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7cfd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7cfd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7cfd-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7cfd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





