---
title: Messaggio LVM_GETHOTITEM (COMmctrl. h)
description: Recupera l'indice dell'elemento attivo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetHotItem di ListView.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- Controlli di Windows Message LVM_GETHOTITEM
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c7bbfb845518eb40b55556df5294d59cff3d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120994"
---
# <a name="lvm_gethotitem-message"></a><span data-ttu-id="d7415-105">\_Messaggio GETHOTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="d7415-105">LVM\_GETHOTITEM message</span></span>

<span data-ttu-id="d7415-106">Recupera l'indice dell'elemento attivo.</span><span class="sxs-lookup"><span data-stu-id="d7415-106">Retrieves the index of the hot item.</span></span> <span data-ttu-id="d7415-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetHotItem di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) .</span><span class="sxs-lookup"><span data-stu-id="d7415-107">You can send this message explicitly or use the [**ListView\_GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7415-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7415-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7415-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7415-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d7415-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d7415-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d7415-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7415-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d7415-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d7415-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7415-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7415-113">Return value</span></span>

<span data-ttu-id="d7415-114">Restituisce l'indice dell'elemento che è attivo.</span><span class="sxs-lookup"><span data-stu-id="d7415-114">Returns the index of the item that is hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7415-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7415-115">Requirements</span></span>



| <span data-ttu-id="d7415-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7415-116">Requirement</span></span> | <span data-ttu-id="d7415-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d7415-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7415-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7415-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d7415-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7415-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7415-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7415-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d7415-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7415-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7415-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7415-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7415-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7415-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





