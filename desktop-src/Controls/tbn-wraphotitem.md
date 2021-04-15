---
title: Codice di notifica TBN_WRAPHOTITEM (COMmctrl. h)
description: Notifica a un'applicazione due o più barre degli strumenti che l'elemento critico sta per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- Controlli di Windows per il codice di notifica TBN_WRAPHOTITEM
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476300"
---
# <a name="tbn_wraphotitem-notification-code"></a><span data-ttu-id="06296-105">\_Codice di notifica WRAPHOTITEM di TBN</span><span class="sxs-lookup"><span data-stu-id="06296-105">TBN\_WRAPHOTITEM notification code</span></span>

<span data-ttu-id="06296-106">Notifica a un'applicazione due o più barre degli strumenti che l'elemento critico sta per cambiare.</span><span class="sxs-lookup"><span data-stu-id="06296-106">Notifies an application with two or more toolbars that the hot item is about to change.</span></span> <span data-ttu-id="06296-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="06296-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="06296-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06296-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06296-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06296-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06296-110">Puntatore a una struttura che contiene il vecchio elemento attivo (**Tart**) e se il nuovo elemento attivo è precedente (**Idir** =-1) o dopo di esso (**Idir** = 1), nonché un motivo per cui l'elemento critico sta cambiando.</span><span class="sxs-lookup"><span data-stu-id="06296-110">A pointer to a structure that contains the old hot item (**iStart**) and whether the new hot item is before it (**iDir** = -1) or after it (**iDir** = 1), as well as a reason why the hot item is changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06296-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06296-111">Return value</span></span>

<span data-ttu-id="06296-112">**True** se l'applicazione sta gestendo la modifica dell'elemento critico; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="06296-112">**TRUE** if the application is handling the hot item change itself; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="06296-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="06296-113">Remarks</span></span>

<span data-ttu-id="06296-114">La struttura **NMTBWRAPHOTITEM** deve essere definita dall'applicazione come segue:</span><span class="sxs-lookup"><span data-stu-id="06296-114">The **NMTBWRAPHOTITEM** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a><span data-ttu-id="06296-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06296-115">Requirements</span></span>



| <span data-ttu-id="06296-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06296-116">Requirement</span></span> | <span data-ttu-id="06296-117">Valore</span><span class="sxs-lookup"><span data-stu-id="06296-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06296-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06296-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06296-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06296-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06296-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06296-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06296-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06296-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06296-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06296-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="06296-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="06296-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





