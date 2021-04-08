---
title: Messaggio LVM_SETITEMINDEXSTATE (COMmctrl. h)
description: Imposta lo stato di un elemento della visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro SetItemIndexState di ListView.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- Controlli di Windows Message LVM_SETITEMINDEXSTATE
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048123"
---
# <a name="lvm_setitemindexstate-message"></a><span data-ttu-id="fc3c2-105">\_Messaggio SETITEMINDEXSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="fc3c2-105">LVM\_SETITEMINDEXSTATE message</span></span>

<span data-ttu-id="fc3c2-106">Imposta lo stato di un elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="fc3c2-106">Sets the state of a list-view item.</span></span> <span data-ttu-id="fc3c2-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ SetItemIndexState di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) .</span><span class="sxs-lookup"><span data-stu-id="fc3c2-107">Send this message explicitly or by using the [**ListView\_SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc3c2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc3c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc3c2-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc3c2-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc3c2-110">Puntatore a una struttura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="fc3c2-110">A pointer to an [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the item.</span></span> <span data-ttu-id="fc3c2-111">Il processo chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei membri.</span><span class="sxs-lookup"><span data-stu-id="fc3c2-111">The calling process is responsible for allocating this structure and setting the members.</span></span>

</dd> <dt>

<span data-ttu-id="fc3c2-112">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc3c2-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc3c2-113">Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="fc3c2-113">A pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="fc3c2-114">Il processo chiamante è responsabile dell'allocazione della memoria per la struttura.</span><span class="sxs-lookup"><span data-stu-id="fc3c2-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="fc3c2-115">Impostare il membro **stato** su uno o più (come combinazione bit per bit) dei flag [degli Stati degli elementi della visualizzazione elenco](list-view-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="fc3c2-115">Set the **state** member to one or more (as a bitwise combination) of the [List-View Item States](list-view-item-states.md) flags.</span></span> <span data-ttu-id="fc3c2-116">Impostare il membro **stateMask** della struttura per indicare i bit validi del membro di **stato** .</span><span class="sxs-lookup"><span data-stu-id="fc3c2-116">Set the **stateMask** member of the structure to indicate the valid bits of the **state** member.</span></span> <span data-ttu-id="fc3c2-117">Per ulteriori informazioni, vedere il membro **stateMask** della struttura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="fc3c2-117">For more information, see the **stateMask** member of the **LVITEM** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc3c2-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc3c2-118">Return value</span></span>

<span data-ttu-id="fc3c2-119">Restituisce uno dei valori seguenti di tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fc3c2-119">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="fc3c2-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fc3c2-120">Return code</span></span>                                                                                  | <span data-ttu-id="fc3c2-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc3c2-121">Description</span></span>                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc3c2-122"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="fc3c2-122"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="fc3c2-123">Non è stato possibile impostare lo stato.</span><span class="sxs-lookup"><span data-stu-id="fc3c2-123">The state could not be set.</span></span><br/>                            |
| <dl> <span data-ttu-id="fc3c2-124"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="fc3c2-124"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="fc3c2-125">Il controllo elenco-visualizzazione non è pronto per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fc3c2-125">The list-view control was not ready for the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fc3c2-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fc3c2-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fc3c2-127">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fc3c2-127">The operation was successful.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="fc3c2-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc3c2-128">Requirements</span></span>



| <span data-ttu-id="fc3c2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc3c2-129">Requirement</span></span> | <span data-ttu-id="fc3c2-130">Valore</span><span class="sxs-lookup"><span data-stu-id="fc3c2-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3c2-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc3c2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fc3c2-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc3c2-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc3c2-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc3c2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fc3c2-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc3c2-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc3c2-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc3c2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc3c2-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc3c2-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





