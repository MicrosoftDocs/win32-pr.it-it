---
title: Codice di notifica TTN_LINKCLICK (COMmctrl. h)
description: Inviato quando si fa clic su un collegamento di testo all'interno di una descrizione comandi a fumetto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- Controlli di Windows per il codice di notifica TTN_LINKCLICK
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301934"
---
# <a name="ttn_linkclick-notification-code"></a><span data-ttu-id="16005-105">\_Codice di notifica LINKCLICK di TTN</span><span class="sxs-lookup"><span data-stu-id="16005-105">TTN\_LINKCLICK notification code</span></span>

<span data-ttu-id="16005-106">Inviato quando si fa clic su un collegamento di testo all'interno di una descrizione comandi a fumetto.</span><span class="sxs-lookup"><span data-stu-id="16005-106">Sent when a text link inside a balloon tooltip is clicked.</span></span> <span data-ttu-id="16005-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="16005-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a><span data-ttu-id="16005-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="16005-108">Parameters</span></span>

<span data-ttu-id="16005-109">Questo codice di notifica non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="16005-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16005-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16005-110">Return value</span></span>

<span data-ttu-id="16005-111">Valore restituito non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="16005-111">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="16005-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="16005-112">Remarks</span></span>

<span data-ttu-id="16005-113">Di seguito è riportato un esempio di quando viene inviata la notifica.</span><span class="sxs-lookup"><span data-stu-id="16005-113">Following is an example of when this notification is sent.</span></span> <span data-ttu-id="16005-114">Si supponga che la descrizione comando del fumetto includa il testo seguente: "questo è un <A>collegamento</A>".</span><span class="sxs-lookup"><span data-stu-id="16005-114">Assume that your balloon tooltip contains the following text, "This is a <A>link</A>".</span></span> <span data-ttu-id="16005-115">Quando si fa clic su "link", il controllo tooltip Invia un \_ codice di notifica LINKCLICK TTN.</span><span class="sxs-lookup"><span data-stu-id="16005-115">When "link" is clicked, the tooltip control sends a TTN\_LINKCLICK notification code.</span></span>

> [!Note]  
> <span data-ttu-id="16005-116">Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="16005-116">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="16005-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="16005-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16005-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16005-118">Requirements</span></span>



| <span data-ttu-id="16005-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="16005-119">Requirement</span></span> | <span data-ttu-id="16005-120">Valore</span><span class="sxs-lookup"><span data-stu-id="16005-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16005-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16005-121">Minimum supported client</span></span><br/> | <span data-ttu-id="16005-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16005-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16005-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16005-123">Minimum supported server</span></span><br/> | <span data-ttu-id="16005-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="16005-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16005-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16005-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="16005-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="16005-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





