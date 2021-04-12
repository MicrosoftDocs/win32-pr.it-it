---
title: Codice di notifica NM_RELEASEDCAPTURE (visualizzazione elenco) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: a43879d9-1465-4c25-936f-cda9b8b8b465
keywords:
- Codice di notifica NM_RELEASEDCAPTURE (visualizzazione elenco) controlli Windows
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42af9dddf6f9864251eff5e2f5a6aebbfa9cd20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478250"
---
# <a name="nm_releasedcapture-list-view-notification-code"></a><span data-ttu-id="29575-105">\_Codice di notifica di RELEASEDCAPTURE Nm (visualizzazione elenco)</span><span class="sxs-lookup"><span data-stu-id="29575-105">NM\_RELEASEDCAPTURE (list view) notification code</span></span>

<span data-ttu-id="29575-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che il controllo sta rilasciando l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="29575-106">Notifies a list-view control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="29575-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="29575-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="29575-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="29575-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29575-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29575-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29575-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="29575-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29575-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29575-111">Return value</span></span>

<span data-ttu-id="29575-112">Il controllo Ignora il valore restituito da questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="29575-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="29575-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29575-113">Requirements</span></span>



| <span data-ttu-id="29575-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="29575-114">Requirement</span></span> | <span data-ttu-id="29575-115">Valore</span><span class="sxs-lookup"><span data-stu-id="29575-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29575-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29575-116">Minimum supported client</span></span><br/> | <span data-ttu-id="29575-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29575-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29575-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29575-118">Minimum supported server</span></span><br/> | <span data-ttu-id="29575-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="29575-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29575-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29575-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="29575-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="29575-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





