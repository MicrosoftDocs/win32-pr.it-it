---
title: Codice di notifica CBEN_BEGINEDIT (COMmctrl. h)
description: Inviato quando l'utente attiva l'elenco a discesa o fa clic nella casella di modifica del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 77236471-b1c0-4679-b7b8-93e85867fe3b
keywords:
- Controlli di Windows per il codice di notifica CBEN_BEGINEDIT
topic_type:
- apiref
api_name:
- CBEN_BEGINEDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d4cc80d12b01b9374173f413f0aee3701e5040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302370"
---
# <a name="cben_beginedit-notification-code"></a><span data-ttu-id="e6a0d-105">Codice di notifica di CBEN \_ BEGINEDIT</span><span class="sxs-lookup"><span data-stu-id="e6a0d-105">CBEN\_BEGINEDIT notification code</span></span>

<span data-ttu-id="e6a0d-106">Inviato quando l'utente attiva l'elenco a discesa o fa clic nella casella di modifica del controllo.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-106">Sent when the user activates the drop-down list or clicks in the control's edit box.</span></span> <span data-ttu-id="e6a0d-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e6a0d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_BEGINEDIT

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e6a0d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6a0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a0d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6a0d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a0d-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a0d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6a0d-111">Return value</span></span>

<span data-ttu-id="e6a0d-112">L'elaborazione dell'applicazione del codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a0d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6a0d-113">Requirements</span></span>



| <span data-ttu-id="e6a0d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a0d-114">Requirement</span></span> | <span data-ttu-id="e6a0d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e6a0d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a0d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6a0d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a0d-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6a0d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6a0d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6a0d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a0d-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6a0d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6a0d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6a0d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6a0d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a0d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





