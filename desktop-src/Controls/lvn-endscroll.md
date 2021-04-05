---
title: Messaggio LVN_ENDSCROLL (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco la fine di un'operazione di scorrimento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- Controlli di Windows Message LVN_ENDSCROLL
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874706"
---
# <a name="lvn_endscroll-message"></a><span data-ttu-id="70846-105">\_Messaggio LVN ENDSCROLL</span><span class="sxs-lookup"><span data-stu-id="70846-105">LVN\_ENDSCROLL message</span></span>

<span data-ttu-id="70846-106">Notifica alla finestra padre di un controllo di visualizzazione elenco la fine di un'operazione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="70846-106">Notifies a list-view control's parent window when a scrolling operation ends.</span></span> <span data-ttu-id="70846-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="70846-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="70846-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="70846-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70846-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70846-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70846-110">Puntatore a una struttura [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) che contiene la posizione orizzontale o verticale del punto in cui termina l'operazione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="70846-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation ends.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70846-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70846-111">Return value</span></span>

<span data-ttu-id="70846-112">Valore restituito non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="70846-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="70846-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="70846-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70846-114">Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="70846-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="70846-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="70846-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70846-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70846-116">Requirements</span></span>



| <span data-ttu-id="70846-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="70846-117">Requirement</span></span> | <span data-ttu-id="70846-118">Valore</span><span class="sxs-lookup"><span data-stu-id="70846-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70846-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70846-119">Minimum supported client</span></span><br/> | <span data-ttu-id="70846-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70846-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70846-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70846-121">Minimum supported server</span></span><br/> | <span data-ttu-id="70846-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70846-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70846-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70846-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="70846-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="70846-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





