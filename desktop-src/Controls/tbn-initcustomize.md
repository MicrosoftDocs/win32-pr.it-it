---
title: Codice di notifica TBN_INITCUSTOMIZE (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che la personalizzazione è stata avviata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- Controlli di Windows per il codice di notifica TBN_INITCUSTOMIZE
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300972"
---
# <a name="tbn_initcustomize-notification-code"></a><span data-ttu-id="aa30d-105">\_Codice di notifica INITCUSTOMIZE di TBN</span><span class="sxs-lookup"><span data-stu-id="aa30d-105">TBN\_INITCUSTOMIZE notification code</span></span>

<span data-ttu-id="aa30d-106">Notifica alla finestra padre di una barra degli strumenti che la personalizzazione è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="aa30d-106">Notifies a toolbar's parent window that customizing has started.</span></span> <span data-ttu-id="aa30d-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aa30d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="aa30d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa30d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa30d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa30d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa30d-110">Puntatore alla struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="aa30d-110">Pointer to the toolbar's [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa30d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa30d-111">Return value</span></span>

<span data-ttu-id="aa30d-112">Restituisce TBNRF \_ HIDEHELP per disattivare il pulsante della guida.</span><span class="sxs-lookup"><span data-stu-id="aa30d-112">Returns TBNRF\_HIDEHELP to suppress the Help button.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa30d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa30d-113">Requirements</span></span>



| <span data-ttu-id="aa30d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa30d-114">Requirement</span></span> | <span data-ttu-id="aa30d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="aa30d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa30d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa30d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aa30d-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa30d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa30d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa30d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aa30d-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa30d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa30d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa30d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa30d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa30d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





