---
title: Messaggio LM_SETITEM (COMmctrl. h)
description: Imposta gli Stati e gli attributi di un elemento.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- Controlli di Windows Message LM_SETITEM
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119022"
---
# <a name="lm_setitem-message"></a><span data-ttu-id="5d8ac-104">\_Messaggio elemento</span><span class="sxs-lookup"><span data-stu-id="5d8ac-104">LM\_SETITEM message</span></span>

<span data-ttu-id="5d8ac-105">Imposta gli Stati e gli attributi di un elemento.</span><span class="sxs-lookup"><span data-stu-id="5d8ac-105">Sets the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d8ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d8ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d8ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d8ac-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5d8ac-108">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5d8ac-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="5d8ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d8ac-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5d8ac-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litey</a> che contiene i nuovi Stati e attributi desiderati per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="5d8ac-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure containing the new states and attributes desired for the link.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d8ac-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d8ac-111">Return value</span></span>

<span data-ttu-id="5d8ac-112">Restituisce **true** se il messaggio riesce a impostare i valori e gli attributi specificati.</span><span class="sxs-lookup"><span data-stu-id="5d8ac-112">Returns **TRUE** if the message succeeds in setting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d8ac-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d8ac-113">Remarks</span></span>

<span data-ttu-id="5d8ac-114">Con il messaggio [**LM \_ GetItem**](lm-getitem.md) , è possibile accedere ai collegamenti solo tramite l'indice numerico restituito nel membro **iLink** di [**liteo**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="5d8ac-114">With the [**LM\_GETITEM**](lm-getitem.md) message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="5d8ac-115">L'accesso al collegamento tramite il nome ID restituito in **szId** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5d8ac-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="5d8ac-116">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comctl32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="5d8ac-116">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="5d8ac-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5d8ac-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d8ac-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d8ac-118">Requirements</span></span>



| <span data-ttu-id="5d8ac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d8ac-119">Requirement</span></span> | <span data-ttu-id="5d8ac-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5d8ac-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d8ac-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d8ac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d8ac-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d8ac-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d8ac-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d8ac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d8ac-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d8ac-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d8ac-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d8ac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d8ac-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d8ac-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





