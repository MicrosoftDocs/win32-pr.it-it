---
title: Codice di notifica TBN_DUPACCELERATOR (COMmctrl. h)
description: Verifica se un tasto di scelta rapida può essere utilizzato su due o più barre degli strumenti attive. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- Controlli di Windows per il codice di notifica TBN_DUPACCELERATOR
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048593"
---
# <a name="tbn_dupaccelerator-notification-code"></a><span data-ttu-id="8cd3b-105">\_Codice di notifica DUPACCELERATOR di TBN</span><span class="sxs-lookup"><span data-stu-id="8cd3b-105">TBN\_DUPACCELERATOR notification code</span></span>

<span data-ttu-id="8cd3b-106">Verifica se un tasto di scelta rapida può essere utilizzato su due o più barre degli strumenti attive.</span><span class="sxs-lookup"><span data-stu-id="8cd3b-106">Ascertains whether an accelerator key can be used on two or more active toolbars.</span></span> <span data-ttu-id="8cd3b-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd3b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8cd3b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8cd3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cd3b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cd3b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cd3b-110">Puntatore a una struttura che fornisce un tasto di scelta rapida e che riceve un valore che specifica se più barre degli strumenti rispondono allo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="8cd3b-110">A pointer to a structure that provides an accelerator and that receives a value specifying whether multiple toolbars respond to the same character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cd3b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8cd3b-111">Return value</span></span>

<span data-ttu-id="8cd3b-112">Restituisce **true** se ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8cd3b-112">Returns **TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cd3b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cd3b-113">Remarks</span></span>

<span data-ttu-id="8cd3b-114">L'applicazione deve dichiarare la struttura **NMTBDUPACCELERATOR** come segue:</span><span class="sxs-lookup"><span data-stu-id="8cd3b-114">The application must declare the **NMTBDUPACCELERATOR** structure as follows:</span></span>

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="8cd3b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cd3b-115">Requirements</span></span>



| <span data-ttu-id="8cd3b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cd3b-116">Requirement</span></span> | <span data-ttu-id="8cd3b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8cd3b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd3b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cd3b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8cd3b-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cd3b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cd3b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cd3b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8cd3b-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cd3b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cd3b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8cd3b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cd3b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cd3b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





