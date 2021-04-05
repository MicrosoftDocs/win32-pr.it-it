---
title: Codice di notifica TTN_NEEDTEXT (COMmctrl. h)
description: Inviato da un controllo ToolTip per recuperare le informazioni necessarie per visualizzare una finestra di descrizione comando. Questo codice di notifica è identico a TTN \_ GETDISPINFO. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- Controlli di Windows per il codice di notifica TTN_NEEDTEXT
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120267"
---
# <a name="ttn_needtext-notification-code"></a><span data-ttu-id="aeb81-106">\_Codice di notifica NEEDTEXT di TTN</span><span class="sxs-lookup"><span data-stu-id="aeb81-106">TTN\_NEEDTEXT notification code</span></span>

<span data-ttu-id="aeb81-107">Inviato da un controllo ToolTip per recuperare le informazioni necessarie per visualizzare una finestra di descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="aeb81-107">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="aeb81-108">Questo codice di notifica è identico a [TTN \_ GETDISPINFO](ttn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="aeb81-108">This notification code is identical to [TTN\_GETDISPINFO](ttn-getdispinfo.md).</span></span> <span data-ttu-id="aeb81-109">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aeb81-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="aeb81-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="aeb81-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb81-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aeb81-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb81-112">Puntatore a una struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) che identifica lo strumento che necessita di testo e riceve le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="aeb81-112">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb81-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aeb81-113">Return value</span></span>

<span data-ttu-id="aeb81-114">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="aeb81-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeb81-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="aeb81-115">Remarks</span></span>

<span data-ttu-id="aeb81-116">Compilare i membri appropriati della struttura per restituire le informazioni richieste al controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="aeb81-116">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="aeb81-117">Se il gestore di messaggi imposta il membro **uFlags** della struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) su ttf \_ di \_ SetItem, il controllo ToolTip archivia le informazioni e non le richiede di nuovo.</span><span class="sxs-lookup"><span data-stu-id="aeb81-117">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb81-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aeb81-118">Requirements</span></span>



| <span data-ttu-id="aeb81-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb81-119">Requirement</span></span> | <span data-ttu-id="aeb81-120">Valore</span><span class="sxs-lookup"><span data-stu-id="aeb81-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb81-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeb81-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb81-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aeb81-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aeb81-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeb81-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb81-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aeb81-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aeb81-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aeb81-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeb81-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeb81-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="aeb81-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="aeb81-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="aeb81-128">**TTN \_ NEEDTEXTW** (Unicode) e **TTN \_ NEEDTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="aeb81-128">**TTN\_NEEDTEXTW** (Unicode) and **TTN\_NEEDTEXTA** (ANSI)</span></span><br/>                 |



 

 





