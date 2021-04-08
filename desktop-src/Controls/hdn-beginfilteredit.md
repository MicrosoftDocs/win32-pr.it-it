---
title: Codice di notifica HDN_BEGINFILTEREDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che è iniziata la modifica di un filtro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- Controlli di Windows per il codice di notifica HDN_BEGINFILTEREDIT
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0527427752b5621e626add17d61e60a675958f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965022"
---
# <a name="hdn_beginfilteredit-notification-code"></a><span data-ttu-id="37b4c-105">\_Codice di notifica BEGINFILTEREDIT di HDN</span><span class="sxs-lookup"><span data-stu-id="37b4c-105">HDN\_BEGINFILTEREDIT notification code</span></span>

<span data-ttu-id="37b4c-106">Notifica alla finestra padre di un controllo di intestazione che è iniziata la modifica di un filtro.</span><span class="sxs-lookup"><span data-stu-id="37b4c-106">Notifies a header control's parent window that a filter edit has begun.</span></span> <span data-ttu-id="37b4c-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="37b4c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="37b4c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="37b4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b4c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37b4c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37b4c-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni aggiuntive sul filtro in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="37b4c-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the filter that is being edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b4c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37b4c-111">Return value</span></span>

<span data-ttu-id="37b4c-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="37b4c-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="37b4c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37b4c-113">Requirements</span></span>



| <span data-ttu-id="37b4c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="37b4c-114">Requirement</span></span> | <span data-ttu-id="37b4c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="37b4c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37b4c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37b4c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37b4c-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37b4c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37b4c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37b4c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37b4c-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="37b4c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37b4c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37b4c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="37b4c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37b4c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





