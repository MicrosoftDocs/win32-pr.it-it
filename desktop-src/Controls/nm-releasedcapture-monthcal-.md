---
title: Codice di notifica di NM_RELEASEDCAPTURE (monthcal) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo monthcal che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: c05d3331-26f3-41f4-8032-36ed38d47917
keywords:
- NM_RELEASEDCAPTURE (monthcal) (codice di notifica) controlli Windows
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
ms.openlocfilehash: 0b9c743a076c8046aa57ba4306145248ed00f0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739919"
---
# <a name="nm_releasedcapture-monthcal-notification-code"></a><span data-ttu-id="e29e7-105">Codice di notifica di NM \_ RELEASEDCAPTURE (monthcal)</span><span class="sxs-lookup"><span data-stu-id="e29e7-105">NM\_RELEASEDCAPTURE (monthcal) notification code</span></span>

<span data-ttu-id="e29e7-106">Notifica alla finestra padre di un controllo monthcal che il controllo sta rilasciando l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="e29e7-106">Notifies a monthcal control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="e29e7-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e29e7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e29e7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e29e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e29e7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e29e7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e29e7-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="e29e7-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e29e7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e29e7-111">Return value</span></span>

<span data-ttu-id="e29e7-112">Il controllo Ignora il valore restituito da questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="e29e7-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e29e7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e29e7-113">Requirements</span></span>



| <span data-ttu-id="e29e7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e29e7-114">Requirement</span></span> | <span data-ttu-id="e29e7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e29e7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e29e7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e29e7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e29e7-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e29e7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e29e7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e29e7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e29e7-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e29e7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e29e7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e29e7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e29e7-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e29e7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





