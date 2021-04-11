---
title: Messaggio LM_GETITEM (COMmctrl. h)
description: Recupera gli Stati e gli attributi di un elemento.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- Controlli di Windows Message LM_GETITEM
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119026"
---
# <a name="lm_getitem-message"></a><span data-ttu-id="df79f-104">\_Messaggio GETitem di LM</span><span class="sxs-lookup"><span data-stu-id="df79f-104">LM\_GETITEM message</span></span>

<span data-ttu-id="df79f-105">Recupera gli Stati e gli attributi di un elemento.</span><span class="sxs-lookup"><span data-stu-id="df79f-105">Retrieves the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="df79f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df79f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df79f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df79f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="df79f-108">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="df79f-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="df79f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df79f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="df79f-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litey</a> da riempire con le informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="df79f-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure to be filled with information about the item.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df79f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df79f-111">Return value</span></span>

<span data-ttu-id="df79f-112">Restituisce **true** se il messaggio riesce a ottenere i valori e gli attributi specificati.</span><span class="sxs-lookup"><span data-stu-id="df79f-112">Returns **TRUE** if the message succeeds in getting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="df79f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="df79f-113">Remarks</span></span>

<span data-ttu-id="df79f-114">Con il messaggio **LM \_ GetItem** , è possibile accedere ai collegamenti solo tramite l'indice numerico restituito nel membro **iLink** di [**liteo**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="df79f-114">With the **LM\_GETITEM** message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="df79f-115">L'accesso al collegamento tramite il nome ID restituito in **szId** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df79f-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="df79f-116">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="df79f-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="df79f-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="df79f-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df79f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df79f-118">Requirements</span></span>



| <span data-ttu-id="df79f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="df79f-119">Requirement</span></span> | <span data-ttu-id="df79f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="df79f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df79f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df79f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="df79f-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df79f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df79f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df79f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="df79f-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df79f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df79f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df79f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="df79f-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df79f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





