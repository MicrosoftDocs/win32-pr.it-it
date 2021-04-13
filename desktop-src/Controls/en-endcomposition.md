---
title: Codice di notifica EN_ENDCOMPOSITION (RichEdit. h)
description: Notifica a una finestra padre del controllo Rich Edit che l'utente ha immesso nuovi dati o ha terminato l'immissione dei dati durante l'uso di IME o del Framework dei servizi di testo.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- Controlli di Windows per il codice di notifica EN_ENDCOMPOSITION
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475389"
---
# <a name="en_endcomposition-notification-code"></a><span data-ttu-id="5a42e-104">\_Codice di notifica en ENDCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="5a42e-104">EN\_ENDCOMPOSITION notification code</span></span>

<span data-ttu-id="5a42e-105">Notifica a una finestra padre del controllo Rich Edit che l'utente ha immesso nuovi dati o ha terminato l'immissione dei dati durante l'uso di IME o del [Framework dei servizi di testo](/windows/desktop/TSF/text-services-framework).</span><span class="sxs-lookup"><span data-stu-id="5a42e-105">Notifies a rich edit control parent window that the user has entered new data or has finished entering data while using IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a><span data-ttu-id="5a42e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a42e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a42e-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a42e-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a42e-108">Struttura [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) che riceve informazioni sulla condizione di composizione finale.</span><span class="sxs-lookup"><span data-stu-id="5a42e-108">A [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) structure that receives information about the end composition condition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a42e-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a42e-109">Requirements</span></span>



| <span data-ttu-id="5a42e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a42e-110">Requirement</span></span> | <span data-ttu-id="5a42e-111">Valore</span><span class="sxs-lookup"><span data-stu-id="5a42e-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a42e-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a42e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5a42e-113">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5a42e-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5a42e-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a42e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5a42e-115">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5a42e-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a42e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a42e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a42e-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a42e-117"><dt>Richedit.h</dt></span></span> </dl> |



 

