---
title: Codice di notifica NM_OUTOFMEMORY (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che il controllo non è stato in grado di completare un'operazione perché la memoria disponibile non è sufficiente. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- Controlli di Windows per il codice di notifica NM_OUTOFMEMORY
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047924"
---
# <a name="nm_outofmemory-notification-code"></a><span data-ttu-id="441e2-105">\_Codice di notifica OutOfMemory Nm</span><span class="sxs-lookup"><span data-stu-id="441e2-105">NM\_OUTOFMEMORY notification code</span></span>

<span data-ttu-id="441e2-106">Notifica alla finestra padre di un controllo che il controllo non è stato in grado di completare un'operazione perché la memoria disponibile non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="441e2-106">Notifies a control's parent window that the control could not complete an operation because there was not enough memory available.</span></span> <span data-ttu-id="441e2-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="441e2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="441e2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="441e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="441e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="441e2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="441e2-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="441e2-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="441e2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="441e2-111">Return value</span></span>

<span data-ttu-id="441e2-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="441e2-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="441e2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="441e2-113">Requirements</span></span>



| <span data-ttu-id="441e2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="441e2-114">Requirement</span></span> | <span data-ttu-id="441e2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="441e2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="441e2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="441e2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="441e2-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="441e2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="441e2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="441e2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="441e2-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="441e2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="441e2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="441e2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="441e2-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="441e2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





