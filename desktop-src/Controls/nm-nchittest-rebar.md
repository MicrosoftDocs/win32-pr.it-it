---
title: NM_NCHITTEST codice di notifica (rebar) (Commctrl.h)
description: 'NM_NCHITTEST di notifica (rebar): inviato da un controllo rebar quando il controllo riceve un messaggio WM \_ NCHITTEST. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.'
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST codice di notifica (rebar) Controlli Windows
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7935f1b3e990db55518c9d22537e8fb6db97962
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112329"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="98cf3-105">Codice di notifica NM \_ NCHITTEST (rebar)</span><span class="sxs-lookup"><span data-stu-id="98cf3-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="98cf3-106">Inviato da un controllo rebar quando il controllo riceve un [**messaggio \_ WM NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest)</span><span class="sxs-lookup"><span data-stu-id="98cf3-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="98cf3-107">Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="98cf3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="98cf3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="98cf3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98cf3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98cf3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98cf3-110">Puntatore a [**una struttura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="98cf3-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="98cf3-111">Il **membro dwItemSpec contiene** l'indice della banda su cui si è verificato il messaggio di hit test e il membro **pt** contiene le coordinate del mouse del messaggio di hit test.</span><span class="sxs-lookup"><span data-stu-id="98cf3-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98cf3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98cf3-112">Return value</span></span>

<span data-ttu-id="98cf3-113">Restituire zero per consentire all'oggetto rebar di eseguire l'elaborazione predefinita del messaggio di hit test o restituire uno dei valori HT documentati in \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) per eseguire l'override dell'elaborazione dell'hit test predefinita.</span><span class="sxs-lookup"><span data-stu-id="98cf3-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="98cf3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98cf3-114">Requirements</span></span>



| <span data-ttu-id="98cf3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="98cf3-115">Requirement</span></span> | <span data-ttu-id="98cf3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="98cf3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98cf3-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98cf3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="98cf3-118">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="98cf3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98cf3-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98cf3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="98cf3-120">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="98cf3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98cf3-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98cf3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="98cf3-122"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="98cf3-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

