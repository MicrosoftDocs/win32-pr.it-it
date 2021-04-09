---
title: Codice di notifica NM_RETURN (visualizzazione elenco) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto INVIO. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- Codice di notifica NM_RETURN (visualizzazione elenco) controlli Windows
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
ms.openlocfilehash: 9b221189ced0e351f088493f00fa7b8849717668
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964644"
---
# <a name="nm_return-list-view-notification-code"></a><span data-ttu-id="d625a-105">\_Codice di notifica restituito da Nm (visualizzazione elenco)</span><span class="sxs-lookup"><span data-stu-id="d625a-105">NM\_RETURN (list view) notification code</span></span>

<span data-ttu-id="d625a-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto INVIO.</span><span class="sxs-lookup"><span data-stu-id="d625a-106">Notifies a list-view control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="d625a-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d625a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d625a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d625a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d625a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d625a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d625a-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="d625a-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d625a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d625a-111">Return value</span></span>

<span data-ttu-id="d625a-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d625a-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d625a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d625a-113">Requirements</span></span>



| <span data-ttu-id="d625a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d625a-114">Requirement</span></span> | <span data-ttu-id="d625a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d625a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d625a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d625a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d625a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d625a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d625a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d625a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d625a-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d625a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d625a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d625a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d625a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d625a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





