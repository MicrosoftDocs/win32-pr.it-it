---
title: Codice di notifica TBN_WRAPACCELERATOR (COMmctrl. h)
description: Richiede l'indice del pulsante in una o più barre degli strumenti corrispondenti al carattere dell'acceleratore specificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- Controlli di Windows per il codice di notifica TBN_WRAPACCELERATOR
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301177"
---
# <a name="tbn_wrapaccelerator-notification-code"></a><span data-ttu-id="bb40c-105">\_Codice di notifica WRAPACCELERATOR di TBN</span><span class="sxs-lookup"><span data-stu-id="bb40c-105">TBN\_WRAPACCELERATOR notification code</span></span>

<span data-ttu-id="bb40c-106">Richiede l'indice del pulsante in una o più barre degli strumenti corrispondenti al carattere dell'acceleratore specificato.</span><span class="sxs-lookup"><span data-stu-id="bb40c-106">Requests the index of the button in one or more toolbars corresponding to the specified accelerator character.</span></span> <span data-ttu-id="bb40c-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bb40c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bb40c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb40c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb40c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb40c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb40c-110">Puntatore a una struttura che contiene il carattere del tasto di scelta rapida e che riceve l'indice del pulsante corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bb40c-110">A pointer to a structure that contains the accelerator key character, and that receives the index of the corresponding button.</span></span> <span data-ttu-id="bb40c-111">L'indice è-1 se il tasto di scelta rapida non corrisponde a un comando.</span><span class="sxs-lookup"><span data-stu-id="bb40c-111">The index is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb40c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb40c-112">Return value</span></span>

<span data-ttu-id="bb40c-113">**True** se viene restituito un indice, in caso contrario **false**.</span><span class="sxs-lookup"><span data-stu-id="bb40c-113">**TRUE** if an index is returned, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb40c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb40c-114">Remarks</span></span>

<span data-ttu-id="bb40c-115">Le applicazioni con una o più barre degli strumenti possono ricevere questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="bb40c-115">Applications with one or more toolbars may receive this notification code.</span></span>

<span data-ttu-id="bb40c-116">La struttura **NMTBWRAPACCELERATOR** deve essere definita dall'applicazione come segue:</span><span class="sxs-lookup"><span data-stu-id="bb40c-116">The **NMTBWRAPACCELERATOR** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="bb40c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb40c-117">Requirements</span></span>



| <span data-ttu-id="bb40c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb40c-118">Requirement</span></span> | <span data-ttu-id="bb40c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bb40c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb40c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb40c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb40c-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb40c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb40c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb40c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb40c-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb40c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb40c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb40c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb40c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb40c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





