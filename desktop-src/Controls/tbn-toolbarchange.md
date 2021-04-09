---
title: Codice di notifica TBN_TOOLBARCHANGE (COMmctrl. h)
description: Notifica alla finestra padre della barra degli strumenti che l'utente ha personalizzato una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 6c5127e6-391f-4592-8547-4cc3d3ed6cf0
keywords:
- Controlli di Windows per il codice di notifica TBN_TOOLBARCHANGE
topic_type:
- apiref
api_name:
- TBN_TOOLBARCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9c533a7a26dd1ed0f1938e6c5138bbae13c31f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964624"
---
# <a name="tbn_toolbarchange-notification-code"></a><span data-ttu-id="c01fd-105">\_Codice di notifica TOOLBARCHANGE di TBN</span><span class="sxs-lookup"><span data-stu-id="c01fd-105">TBN\_TOOLBARCHANGE notification code</span></span>

<span data-ttu-id="c01fd-106">Notifica alla finestra padre della barra degli strumenti che l'utente ha personalizzato una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="c01fd-106">Notifies the toolbar's parent window that the user has customized a toolbar.</span></span> <span data-ttu-id="c01fd-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c01fd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_TOOLBARCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c01fd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c01fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c01fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c01fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c01fd-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="c01fd-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c01fd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c01fd-111">Return value</span></span>

<span data-ttu-id="c01fd-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c01fd-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c01fd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c01fd-113">Requirements</span></span>



| <span data-ttu-id="c01fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c01fd-114">Requirement</span></span> | <span data-ttu-id="c01fd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c01fd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c01fd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c01fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c01fd-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c01fd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c01fd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c01fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c01fd-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c01fd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c01fd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c01fd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c01fd-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c01fd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





