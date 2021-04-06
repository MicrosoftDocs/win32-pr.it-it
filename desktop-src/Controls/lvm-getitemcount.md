---
title: Messaggio LVM_GETITEMCOUNT (COMmctrl. h)
description: Recupera il numero di elementi in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemCount di ListView.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- Controlli di Windows Message LVM_GETITEMCOUNT
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742991"
---
# <a name="lvm_getitemcount-message"></a><span data-ttu-id="22479-105">\_Messaggio GETITEMCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="22479-105">LVM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="22479-106">Recupera il numero di elementi in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="22479-106">Retrieves the number of items in a list-view control.</span></span> <span data-ttu-id="22479-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemCount di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="22479-107">You can send this message explicitly or by using the [**ListView\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="22479-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="22479-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22479-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22479-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="22479-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="22479-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="22479-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22479-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="22479-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="22479-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22479-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22479-113">Return value</span></span>

<span data-ttu-id="22479-114">Restituisce il numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="22479-114">Returns the number of items.</span></span>

## <a name="requirements"></a><span data-ttu-id="22479-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22479-115">Requirements</span></span>



| <span data-ttu-id="22479-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="22479-116">Requirement</span></span> | <span data-ttu-id="22479-117">Valore</span><span class="sxs-lookup"><span data-stu-id="22479-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22479-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22479-118">Minimum supported client</span></span><br/> | <span data-ttu-id="22479-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22479-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22479-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22479-120">Minimum supported server</span></span><br/> | <span data-ttu-id="22479-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22479-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22479-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22479-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="22479-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22479-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





