---
title: Codice di notifica TBN_DRAGOVER (COMmctrl. h)
description: Verifica se \_ deve essere inviato un messaggio TB MARKBUTTON per un pulsante trascinato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- Controlli di Windows per il codice di notifica TBN_DRAGOVER
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475904"
---
# <a name="tbn_dragover-notification-code"></a><span data-ttu-id="a6e26-105">Codice di notifica di TBN \_ DRAGOVER</span><span class="sxs-lookup"><span data-stu-id="a6e26-105">TBN\_DRAGOVER notification code</span></span>

<span data-ttu-id="a6e26-106">Verifica se deve essere inviato un messaggio [**TB \_ MARKBUTTON**](tb-markbutton.md) per un pulsante trascinato.</span><span class="sxs-lookup"><span data-stu-id="a6e26-106">Ascertains whether a [**TB\_MARKBUTTON**](tb-markbutton.md) message should be sent for a button that is being dragged over.</span></span> <span data-ttu-id="a6e26-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a6e26-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a6e26-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6e26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6e26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6e26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e26-110">Puntatore a una struttura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) che specifica l'elemento da trascinare.</span><span class="sxs-lookup"><span data-stu-id="a6e26-110">A pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that specifies which item is being dragged over.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6e26-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6e26-111">Return value</span></span>

<span data-ttu-id="a6e26-112">**False** se la barra degli strumenti deve inviare un \_ messaggio TB MARKBUTTON; in caso contrario **true**.</span><span class="sxs-lookup"><span data-stu-id="a6e26-112">**FALSE** if the toolbar should send a TB\_MARKBUTTON message; otherwise **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6e26-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6e26-113">Requirements</span></span>



| <span data-ttu-id="a6e26-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6e26-114">Requirement</span></span> | <span data-ttu-id="a6e26-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a6e26-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e26-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6e26-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a6e26-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6e26-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6e26-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6e26-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a6e26-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6e26-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6e26-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6e26-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6e26-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6e26-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





