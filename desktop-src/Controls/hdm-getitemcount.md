---
title: Messaggio HDM_GETITEMCOUNT (COMmctrl. h)
description: Ottiene un conteggio degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetItemCount dell'intestazione.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- Controlli di Windows Message HDM_GETITEMCOUNT
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120307"
---
# <a name="hdm_getitemcount-message"></a><span data-ttu-id="78af5-105">\_Messaggio HDM GETITEMCOUNT</span><span class="sxs-lookup"><span data-stu-id="78af5-105">HDM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="78af5-106">Ottiene un conteggio degli elementi in un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="78af5-106">Gets a count of the items in a header control.</span></span> <span data-ttu-id="78af5-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetItemCount dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="78af5-107">You can send this message explicitly or use the [**Header\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="78af5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="78af5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78af5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78af5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="78af5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="78af5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="78af5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78af5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="78af5-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="78af5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78af5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78af5-113">Return value</span></span>

<span data-ttu-id="78af5-114">Restituisce il numero di elementi in caso di esito positivo, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="78af5-114">Returns the number of items if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="78af5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78af5-115">Requirements</span></span>



| <span data-ttu-id="78af5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="78af5-116">Requirement</span></span> | <span data-ttu-id="78af5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="78af5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78af5-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78af5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78af5-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78af5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78af5-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78af5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78af5-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78af5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78af5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78af5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78af5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="78af5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





