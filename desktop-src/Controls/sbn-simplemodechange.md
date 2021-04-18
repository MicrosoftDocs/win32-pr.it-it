---
title: Codice di notifica SBN_SIMPLEMODECHANGE (COMmctrl. h)
description: Inviato da un controllo barra di stato quando la modalità semplice cambia a causa di un \_ messaggio semplice SB. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- Controlli di Windows per il codice di notifica SBN_SIMPLEMODECHANGE
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302127"
---
# <a name="sbn_simplemodechange-notification-code"></a><span data-ttu-id="71b2e-105">\_Codice di notifica SIMPLEMODECHANGE di SBN</span><span class="sxs-lookup"><span data-stu-id="71b2e-105">SBN\_SIMPLEMODECHANGE notification code</span></span>

<span data-ttu-id="71b2e-106">Inviato da un controllo barra di stato quando la modalità semplice cambia a causa di un messaggio [**\_ semplice SB**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="71b2e-106">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="71b2e-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="71b2e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="71b2e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="71b2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71b2e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71b2e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71b2e-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="71b2e-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71b2e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71b2e-111">Return value</span></span>

<span data-ttu-id="71b2e-112">Il valore restituito viene ignorato dalla barra di stato.</span><span class="sxs-lookup"><span data-stu-id="71b2e-112">The return value is ignored by the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b2e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71b2e-113">Requirements</span></span>



| <span data-ttu-id="71b2e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="71b2e-114">Requirement</span></span> | <span data-ttu-id="71b2e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="71b2e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71b2e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71b2e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="71b2e-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71b2e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71b2e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71b2e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="71b2e-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71b2e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71b2e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71b2e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b2e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b2e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





