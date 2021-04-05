---
title: Codice di notifica TBN_CUSTHELP (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che l'utente ha scelto il pulsante della guida nella finestra di dialogo Personalizza barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- Controlli di Windows per il codice di notifica TBN_CUSTHELP
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873521"
---
# <a name="tbn_custhelp-notification-code"></a><span data-ttu-id="f5342-105">\_Codice di notifica CUSTHELP di TBN</span><span class="sxs-lookup"><span data-stu-id="f5342-105">TBN\_CUSTHELP notification code</span></span>

<span data-ttu-id="f5342-106">Notifica alla finestra padre di una barra degli strumenti che l'utente ha scelto il pulsante della guida nella finestra di dialogo Personalizza barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f5342-106">Notifies a toolbar's parent window that the user has chosen the Help button in the Customize Toolbar dialog box.</span></span> <span data-ttu-id="f5342-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f5342-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_CUSTHELP 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f5342-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5342-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5342-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5342-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5342-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="f5342-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5342-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5342-111">Return value</span></span>

<span data-ttu-id="f5342-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f5342-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5342-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5342-113">Requirements</span></span>



| <span data-ttu-id="f5342-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5342-114">Requirement</span></span> | <span data-ttu-id="f5342-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f5342-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5342-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5342-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5342-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5342-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5342-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5342-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5342-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5342-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5342-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5342-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5342-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5342-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





