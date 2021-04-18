---
title: Codice di notifica NM_CHAR (COMmctrl. h)
description: Il \_ codice di notifica del valore Nm viene inviato da un controllo quando viene elaborato un tasto carattere. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- Controlli di Windows per il codice di notifica NM_CHAR
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302793"
---
# <a name="nm_char-notification-code"></a><span data-ttu-id="0356d-105">Codice di notifica di NM \_ Char</span><span class="sxs-lookup"><span data-stu-id="0356d-105">NM\_CHAR notification code</span></span>

<span data-ttu-id="0356d-106">Il \_ codice di notifica del valore Nm viene inviato da un controllo quando viene elaborato un tasto carattere.</span><span class="sxs-lookup"><span data-stu-id="0356d-106">The NM\_CHAR notification code is sent by a control when a character key is processed.</span></span> <span data-ttu-id="0356d-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0356d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0356d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0356d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0356d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0356d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0356d-110">Puntatore a una struttura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) contenente informazioni aggiuntive sul carattere che ha causato il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="0356d-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0356d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0356d-111">Return value</span></span>

<span data-ttu-id="0356d-112">Il valore restituito viene ignorato dalla maggior parte dei controlli.</span><span class="sxs-lookup"><span data-stu-id="0356d-112">The return value is ignored by most controls.</span></span> <span data-ttu-id="0356d-113">Per ulteriori informazioni, vedere la documentazione per i singoli controlli.</span><span class="sxs-lookup"><span data-stu-id="0356d-113">For more information, see the documentation for the individual controls.</span></span>

## <a name="requirements"></a><span data-ttu-id="0356d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0356d-114">Requirements</span></span>



| <span data-ttu-id="0356d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0356d-115">Requirement</span></span> | <span data-ttu-id="0356d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0356d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0356d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0356d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0356d-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0356d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0356d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0356d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0356d-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0356d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0356d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0356d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0356d-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0356d-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0356d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0356d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0356d-124">NM \_ char (barra degli strumenti)</span><span class="sxs-lookup"><span data-stu-id="0356d-124">NM\_CHAR (toolbar)</span></span>](nm-char-toolbar.md)
</dt> </dl>

 

 





