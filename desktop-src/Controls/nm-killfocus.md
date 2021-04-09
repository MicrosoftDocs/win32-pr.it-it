---
title: Codice di notifica NM_KILLFOCUS (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che il controllo ha perso lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d7538697-8b4c-4bbd-8b06-02cbc8069a22
keywords:
- Controlli di Windows per il codice di notifica NM_KILLFOCUS
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
ms.openlocfilehash: 873af3315dd58a12a61249ca59a317ca5af4b105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118982"
---
# <a name="nm_killfocus-notification-code"></a><span data-ttu-id="5fbb1-105">\_Codice di notifica KILLFOCUS Nm</span><span class="sxs-lookup"><span data-stu-id="5fbb1-105">NM\_KILLFOCUS notification code</span></span>

<span data-ttu-id="5fbb1-106">Notifica alla finestra padre di un controllo che il controllo ha perso lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-106">Notifies a control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="5fbb1-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5fbb1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5fbb1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fbb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fbb1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fbb1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fbb1-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fbb1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fbb1-111">Return value</span></span>

<span data-ttu-id="5fbb1-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fbb1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fbb1-113">Requirements</span></span>



| <span data-ttu-id="5fbb1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fbb1-114">Requirement</span></span> | <span data-ttu-id="5fbb1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5fbb1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbb1-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fbb1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5fbb1-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fbb1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fbb1-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fbb1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5fbb1-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5fbb1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5fbb1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fbb1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fbb1-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fbb1-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





