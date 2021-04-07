---
title: Codice di notifica HDN_ITEMKEYDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che è stato premuto un tasto con un elemento selezionato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- Controlli di Windows per il codice di notifica HDN_ITEMKEYDOWN
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048749"
---
# <a name="hdn_itemkeydown-notification-code"></a><span data-ttu-id="10897-105">\_Codice di notifica ITEMKEYDOWN di HDN</span><span class="sxs-lookup"><span data-stu-id="10897-105">HDN\_ITEMKEYDOWN notification code</span></span>

<span data-ttu-id="10897-106">Notifica alla finestra padre di un controllo di intestazione che è stato premuto un tasto con un elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="10897-106">Notifies a header control's parent window that a key has been pressed with an item selected.</span></span> <span data-ttu-id="10897-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="10897-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="10897-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="10897-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10897-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10897-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10897-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni aggiuntive sulla chiave da premere.</span><span class="sxs-lookup"><span data-stu-id="10897-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10897-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10897-111">Return value</span></span>

<span data-ttu-id="10897-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="10897-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="10897-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10897-113">Requirements</span></span>



| <span data-ttu-id="10897-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="10897-114">Requirement</span></span> | <span data-ttu-id="10897-115">Valore</span><span class="sxs-lookup"><span data-stu-id="10897-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10897-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10897-116">Minimum supported client</span></span><br/> | <span data-ttu-id="10897-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10897-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10897-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10897-118">Minimum supported server</span></span><br/> | <span data-ttu-id="10897-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10897-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10897-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10897-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="10897-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10897-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





