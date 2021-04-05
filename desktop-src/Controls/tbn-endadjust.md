---
title: Codice di notifica TBN_ENDADJUST (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che l'utente ha interrotto la personalizzazione di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 9a7496ec-787d-4571-8eca-50d60383519b
keywords:
- Controlli di Windows per il codice di notifica TBN_ENDADJUST
topic_type:
- apiref
api_name:
- TBN_ENDADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec420c535a207f02d12e17901efab1c18a11bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048254"
---
# <a name="tbn_endadjust-notification-code"></a><span data-ttu-id="2ca22-105">\_Codice di notifica ENDADJUST di TBN</span><span class="sxs-lookup"><span data-stu-id="2ca22-105">TBN\_ENDADJUST notification code</span></span>

<span data-ttu-id="2ca22-106">Notifica alla finestra padre di una barra degli strumenti che l'utente ha interrotto la personalizzazione di una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="2ca22-106">Notifies a toolbar's parent window that the user has stopped customizing a toolbar.</span></span> <span data-ttu-id="2ca22-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2ca22-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2ca22-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ca22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ca22-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ca22-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ca22-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="2ca22-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ca22-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ca22-111">Return value</span></span>

<span data-ttu-id="2ca22-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2ca22-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca22-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ca22-113">Requirements</span></span>



| <span data-ttu-id="2ca22-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca22-114">Requirement</span></span> | <span data-ttu-id="2ca22-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2ca22-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca22-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ca22-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca22-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ca22-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ca22-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ca22-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca22-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ca22-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ca22-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ca22-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ca22-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca22-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





