---
title: Codice di notifica EN_STARTCOMPOSITION (RichEdit. h)
description: Notifica a una finestra padre del controllo Rich Edit che l'utente ha iniziato a digitare con IME o il Framework dei servizi di testo.
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- Controlli di Windows per il codice di notifica EN_STARTCOMPOSITION
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a103431427a9325a6b74c27927fb56e65f6fe771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121022"
---
# <a name="en_startcomposition-notification-code"></a><span data-ttu-id="04996-104">\_Codice di notifica en STARTCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="04996-104">EN\_STARTCOMPOSITION notification code</span></span>

<span data-ttu-id="04996-105">Notifica a una finestra padre del controllo Rich Edit che l'utente ha iniziato a digitare con IME o il [Framework dei servizi di testo](/windows/desktop/TSF/text-services-framework).</span><span class="sxs-lookup"><span data-stu-id="04996-105">Notifies a rich edit control parent window that the user started typing with IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="04996-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04996-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04996-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04996-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04996-108">Struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="04996-108">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04996-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04996-109">Requirements</span></span>



| <span data-ttu-id="04996-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="04996-110">Requirement</span></span> | <span data-ttu-id="04996-111">Valore</span><span class="sxs-lookup"><span data-stu-id="04996-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04996-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04996-112">Minimum supported client</span></span><br/> | <span data-ttu-id="04996-113">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="04996-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="04996-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04996-114">Minimum supported server</span></span><br/> | <span data-ttu-id="04996-115">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="04996-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04996-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04996-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="04996-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="04996-117"><dt>Richedit.h</dt></span></span> </dl> |



 

