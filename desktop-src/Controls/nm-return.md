---
title: Codice di notifica NM_RETURN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto INVIO. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- Controlli di Windows per il codice di notifica NM_RETURN
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
ms.openlocfilehash: 4c6cebd089873df5471c9b25710efafaab4d246f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518454"
---
# <a name="nm_return-notification-code"></a><span data-ttu-id="6c057-105">\_Codice di notifica restituito da Nm</span><span class="sxs-lookup"><span data-stu-id="6c057-105">NM\_RETURN notification code</span></span>

<span data-ttu-id="6c057-106">Notifica alla finestra padre di un controllo che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto INVIO.</span><span class="sxs-lookup"><span data-stu-id="6c057-106">Notifies a control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="6c057-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6c057-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6c057-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c057-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c057-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c057-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c057-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="6c057-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c057-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c057-111">Return value</span></span>

<span data-ttu-id="6c057-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="6c057-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c057-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c057-113">Requirements</span></span>



| <span data-ttu-id="6c057-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c057-114">Requirement</span></span> | <span data-ttu-id="6c057-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6c057-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c057-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c057-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c057-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c057-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c057-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c057-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c057-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c057-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c057-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c057-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c057-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c057-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





