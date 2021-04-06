---
title: Codice di notifica LVN_ODSTATECHANGED (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando lo stato di un elemento o di un intervallo di elementi è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- Controlli di Windows per il codice di notifica LVN_ODSTATECHANGED
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86de2f5e01e15d0a97c49f451914aac5b74b27e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742551"
---
# <a name="lvn_odstatechanged-notification-code"></a><span data-ttu-id="efa7a-105">\_Codice di notifica ODSTATECHANGED di LVN</span><span class="sxs-lookup"><span data-stu-id="efa7a-105">LVN\_ODSTATECHANGED notification code</span></span>

<span data-ttu-id="efa7a-106">Inviato da un controllo di visualizzazione elenco quando lo stato di un elemento o di un intervallo di elementi è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="efa7a-106">Sent by a list-view control when the state of an item or range of items has changed.</span></span> <span data-ttu-id="efa7a-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="efa7a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="efa7a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="efa7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efa7a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efa7a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efa7a-110">Puntatore a una struttura [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) che contiene informazioni sull'elemento o gli elementi che sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="efa7a-110">Pointer to an [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) structure that contains information about the item or items that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efa7a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efa7a-111">Return value</span></span>

<span data-ttu-id="efa7a-112">L'applicazione che riceve il codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="efa7a-112">The application receiving this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="efa7a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efa7a-113">Requirements</span></span>



| <span data-ttu-id="efa7a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="efa7a-114">Requirement</span></span> | <span data-ttu-id="efa7a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="efa7a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efa7a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efa7a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="efa7a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efa7a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="efa7a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efa7a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="efa7a-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efa7a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efa7a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efa7a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="efa7a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="efa7a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





