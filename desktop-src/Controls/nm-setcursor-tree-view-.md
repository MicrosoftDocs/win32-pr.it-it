---
title: Codice di notifica di NM_SETCURSOR (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo sta impostando il cursore in risposta a un \_ messaggio del cursore WM. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- NM_SETCURSOR (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40b733e32c72abc9620e0fd18a6ef554aee9214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964642"
---
# <a name="nm_setcursor-tree-view-notification-code"></a><span data-ttu-id="99480-105">\_Codice di notifica del cursore Nm (visualizzazione albero)</span><span class="sxs-lookup"><span data-stu-id="99480-105">NM\_SETCURSOR (tree view) notification code</span></span>

<span data-ttu-id="99480-106">Notifica alla finestra padre di un controllo di visualizzazione albero che il controllo sta impostando il cursore in risposta a un messaggio del [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="99480-106">Notifies a tree-view control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="99480-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="99480-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="99480-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="99480-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99480-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99480-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99480-110">Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="99480-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99480-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99480-111">Return value</span></span>

<span data-ttu-id="99480-112">Restituisce zero per consentire al controllo di impostare il cursore o un valore diverso da zero per impedire al controllo di impostare il cursore.</span><span class="sxs-lookup"><span data-stu-id="99480-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="99480-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99480-113">Requirements</span></span>



| <span data-ttu-id="99480-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="99480-114">Requirement</span></span> | <span data-ttu-id="99480-115">Valore</span><span class="sxs-lookup"><span data-stu-id="99480-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99480-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99480-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99480-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99480-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99480-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99480-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99480-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99480-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99480-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99480-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99480-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="99480-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

