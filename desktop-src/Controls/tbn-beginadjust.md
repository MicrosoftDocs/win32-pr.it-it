---
title: Codice di notifica TBN_BEGINADJUST (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che l'utente ha iniziato a personalizzare una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 689aeda3-5051-4422-9e66-64557b263943
keywords:
- Controlli di Windows per il codice di notifica TBN_BEGINADJUST
topic_type:
- apiref
api_name:
- TBN_BEGINADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4708cd205461e3117432cec25e0e4256a6b0d87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873522"
---
# <a name="tbn_beginadjust-notification-code"></a><span data-ttu-id="5cf4d-105">\_Codice di notifica BEGINADJUST di TBN</span><span class="sxs-lookup"><span data-stu-id="5cf4d-105">TBN\_BEGINADJUST notification code</span></span>

<span data-ttu-id="5cf4d-106">Notifica alla finestra padre di una barra degli strumenti che l'utente ha iniziato a personalizzare una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="5cf4d-106">Notifies a toolbar's parent window that the user has begun customizing a toolbar.</span></span> <span data-ttu-id="5cf4d-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf4d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5cf4d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cf4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cf4d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cf4d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf4d-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="5cf4d-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cf4d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cf4d-111">Return value</span></span>

<span data-ttu-id="5cf4d-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="5cf4d-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf4d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cf4d-113">Requirements</span></span>



| <span data-ttu-id="5cf4d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cf4d-114">Requirement</span></span> | <span data-ttu-id="5cf4d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5cf4d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf4d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cf4d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf4d-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5cf4d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cf4d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cf4d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf4d-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5cf4d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cf4d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cf4d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cf4d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cf4d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





