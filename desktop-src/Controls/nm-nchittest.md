---
title: Codice di notifica NM_NCHITTEST (COMmctrl. h)
description: Inviato da un controllo Rebar quando il controllo riceve un \_ messaggio WM NCHITTEST. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- Controlli di Windows per il codice di notifica NM_NCHITTEST
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
ms.openlocfilehash: f8af39fd792ecb9aeb463957f49f5722737e6ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301704"
---
# <a name="nm_nchittest-notification-code"></a><span data-ttu-id="a45ea-105">\_Codice di notifica NCHITTEST Nm</span><span class="sxs-lookup"><span data-stu-id="a45ea-105">NM\_NCHITTEST notification code</span></span>

<span data-ttu-id="a45ea-106">Inviato da un controllo Rebar quando il controllo riceve un messaggio [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) .</span><span class="sxs-lookup"><span data-stu-id="a45ea-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="a45ea-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a45ea-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a45ea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a45ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a45ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a45ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a45ea-110">Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="a45ea-110">A pointer to a [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="a45ea-111">Il membro *PT* contiene le coordinate del mouse del messaggio di hit test.</span><span class="sxs-lookup"><span data-stu-id="a45ea-111">The *pt* member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a45ea-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a45ea-112">Return value</span></span>

<span data-ttu-id="a45ea-113">Se non diversamente specificato, restituire zero per consentire al controllo di eseguire l'elaborazione predefinita del messaggio di hit test oppure restituire uno dei valori HT \* documentati in [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) per eseguire l'override dell'elaborazione dell'hit test predefinito.</span><span class="sxs-lookup"><span data-stu-id="a45ea-113">Unless otherwise specified, return zero to allow the control to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="a45ea-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a45ea-114">Requirements</span></span>



| <span data-ttu-id="a45ea-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a45ea-115">Requirement</span></span> | <span data-ttu-id="a45ea-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a45ea-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a45ea-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a45ea-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a45ea-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a45ea-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a45ea-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a45ea-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a45ea-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a45ea-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a45ea-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a45ea-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a45ea-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a45ea-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

