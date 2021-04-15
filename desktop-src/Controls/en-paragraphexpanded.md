---
title: Codice di notifica EN_PARAGRAPHEXPANDED (RichEdit. h)
description: Notifica all'elemento padre di un controllo Rich Edit che è stata espansa una struttura. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- Controlli di Windows per il codice di notifica EN_PARAGRAPHEXPANDED
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f862260c0653d23b0b53649a2c05e59820e3808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476979"
---
# <a name="en_paragraphexpanded-notification-code"></a><span data-ttu-id="fe044-105">\_Codice di notifica en PARAGRAPHEXPANDED</span><span class="sxs-lookup"><span data-stu-id="fe044-105">EN\_PARAGRAPHEXPANDED notification code</span></span>

<span data-ttu-id="fe044-106">Notifica all'elemento padre di un controllo Rich Edit che è stata espansa una struttura.</span><span class="sxs-lookup"><span data-stu-id="fe044-106">Notifies a rich edit control's parent that an outline has been expanded.</span></span> <span data-ttu-id="fe044-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fe044-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fe044-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe044-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe044-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe044-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe044-110">Struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="fe044-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe044-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe044-111">Requirements</span></span>



| <span data-ttu-id="fe044-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe044-112">Requirement</span></span> | <span data-ttu-id="fe044-113">Valore</span><span class="sxs-lookup"><span data-stu-id="fe044-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe044-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe044-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fe044-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe044-115">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe044-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe044-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fe044-117">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe044-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe044-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe044-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe044-119"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe044-119"><dt>Richedit.h</dt></span></span> </dl> |



 

 





