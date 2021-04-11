---
title: Codice di notifica RBN_HEIGHTCHANGE (COMmctrl. h)
description: Inviato da un controllo Rebar quando l'altezza è cambiata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- Controlli di Windows per il codice di notifica RBN_HEIGHTCHANGE
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964158"
---
# <a name="rbn_heightchange-notification-code"></a><span data-ttu-id="484c5-105">\_Codice di notifica HEIGHTCHANGE di RBN</span><span class="sxs-lookup"><span data-stu-id="484c5-105">RBN\_HEIGHTCHANGE notification code</span></span>

<span data-ttu-id="484c5-106">Inviato da un controllo Rebar quando l'altezza è cambiata.</span><span class="sxs-lookup"><span data-stu-id="484c5-106">Sent by a rebar control when its height has changed.</span></span> <span data-ttu-id="484c5-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="484c5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="484c5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="484c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="484c5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="484c5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="484c5-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="484c5-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="484c5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="484c5-111">Return value</span></span>

<span data-ttu-id="484c5-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="484c5-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="484c5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="484c5-113">Remarks</span></span>

<span data-ttu-id="484c5-114">I controlli Rebar che usano lo stile [**CCS \_ Vert**](common-control-styles.md) inviano questo codice di notifica quando cambiano la larghezza.</span><span class="sxs-lookup"><span data-stu-id="484c5-114">Rebar controls that use the [**CCS\_VERT**](common-control-styles.md) style send this notification code when their width changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="484c5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="484c5-115">Requirements</span></span>



| <span data-ttu-id="484c5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="484c5-116">Requirement</span></span> | <span data-ttu-id="484c5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="484c5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="484c5-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="484c5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="484c5-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="484c5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="484c5-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="484c5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="484c5-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="484c5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="484c5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="484c5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="484c5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="484c5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





