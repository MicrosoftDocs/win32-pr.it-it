---
title: Messaggio LVM_SETHOTITEM (COMmctrl. h)
description: Imposta l'elemento attivo per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHotItem di ListView.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- Controlli di Windows Message LVM_SETHOTITEM
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739943"
---
# <a name="lvm_sethotitem-message"></a><span data-ttu-id="5f0e4-105">\_Messaggio SETHOTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="5f0e4-105">LVM\_SETHOTITEM message</span></span>

<span data-ttu-id="5f0e4-106">Imposta l'elemento attivo per un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="5f0e4-106">Sets the hot item for a list-view control.</span></span> <span data-ttu-id="5f0e4-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHotItem di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) .</span><span class="sxs-lookup"><span data-stu-id="5f0e4-107">You can send this message explicitly or use the [**ListView\_SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f0e4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f0e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f0e4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f0e4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f0e4-110">Indice in base zero dell'elemento da impostare come elemento attivo.</span><span class="sxs-lookup"><span data-stu-id="5f0e4-110">Zero-based index of the item to be set as the hot item.</span></span>

</dd> <dt>

<span data-ttu-id="5f0e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f0e4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5f0e4-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5f0e4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f0e4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f0e4-113">Return value</span></span>

<span data-ttu-id="5f0e4-114">Restituisce l'indice dell'elemento precedentemente attivo.</span><span class="sxs-lookup"><span data-stu-id="5f0e4-114">Returns the index of the item that was previously hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f0e4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f0e4-115">Requirements</span></span>



| <span data-ttu-id="5f0e4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f0e4-116">Requirement</span></span> | <span data-ttu-id="5f0e4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5f0e4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0e4-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f0e4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5f0e4-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f0e4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f0e4-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f0e4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5f0e4-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5f0e4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f0e4-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f0e4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f0e4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f0e4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





