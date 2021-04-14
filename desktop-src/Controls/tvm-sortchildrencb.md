---
title: Messaggio TVM_SORTCHILDRENCB (COMmctrl. h)
description: Ordina gli elementi della visualizzazione albero utilizzando una funzione di callback definita dall'applicazione che confronta gli elementi. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortChildrenCB di TreeView.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- Controlli di Windows Message TVM_SORTCHILDRENCB
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478946"
---
# <a name="tvm_sortchildrencb-message"></a><span data-ttu-id="93c29-105">\_Messaggio SORTCHILDRENCB TVM</span><span class="sxs-lookup"><span data-stu-id="93c29-105">TVM\_SORTCHILDRENCB message</span></span>

<span data-ttu-id="93c29-106">Ordina gli elementi della visualizzazione albero utilizzando una funzione di callback definita dall'applicazione che confronta gli elementi.</span><span class="sxs-lookup"><span data-stu-id="93c29-106">Sorts tree-view items using an application-defined callback function that compares the items.</span></span> <span data-ttu-id="93c29-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortChildrenCB di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) .</span><span class="sxs-lookup"><span data-stu-id="93c29-107">You can send this message explicitly or by using the [**TreeView\_SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="93c29-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="93c29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c29-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93c29-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93c29-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="93c29-110">Reserved.</span></span> <span data-ttu-id="93c29-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="93c29-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="93c29-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93c29-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93c29-113">Puntatore a una struttura [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) .</span><span class="sxs-lookup"><span data-stu-id="93c29-113">Pointer to a [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) structure.</span></span> <span data-ttu-id="93c29-114">Il membro **lpfnCompare** è l'indirizzo della funzione di callback definita dall'applicazione, che viene chiamata durante l'operazione di ordinamento ogni volta che è necessario confrontare l'ordine relativo di due elementi dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="93c29-114">The **lpfnCompare** member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared.</span></span> <span data-ttu-id="93c29-115">Per ulteriori informazioni sulla funzione di callback, vedere la descrizione di **TVSORTCB**.</span><span class="sxs-lookup"><span data-stu-id="93c29-115">For more information about the callback function, see the description of **TVSORTCB**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c29-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93c29-116">Return value</span></span>

<span data-ttu-id="93c29-117">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="93c29-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c29-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93c29-118">Requirements</span></span>



| <span data-ttu-id="93c29-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c29-119">Requirement</span></span> | <span data-ttu-id="93c29-120">Valore</span><span class="sxs-lookup"><span data-stu-id="93c29-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93c29-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c29-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93c29-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93c29-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93c29-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c29-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93c29-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93c29-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93c29-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93c29-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="93c29-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="93c29-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





