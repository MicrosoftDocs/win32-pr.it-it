---
title: Messaggio LVM_GETCALLBACKMASK (COMmctrl. h)
description: Ottiene la maschera di callback per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetCallbackMask di ListView.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- Controlli di Windows Message LVM_GETCALLBACKMASK
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475178"
---
# <a name="lvm_getcallbackmask-message"></a><span data-ttu-id="7be89-105">\_Messaggio GETCALLBACKMASK LVM</span><span class="sxs-lookup"><span data-stu-id="7be89-105">LVM\_GETCALLBACKMASK message</span></span>

<span data-ttu-id="7be89-106">Ottiene la maschera di callback per un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="7be89-106">Gets the callback mask for a list-view control.</span></span> <span data-ttu-id="7be89-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetCallbackMask di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="7be89-107">You can send this message explicitly or by using the [**ListView\_GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7be89-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7be89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be89-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7be89-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7be89-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7be89-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7be89-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7be89-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7be89-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7be89-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be89-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7be89-113">Return value</span></span>

<span data-ttu-id="7be89-114">Restituisce la maschera di callback.</span><span class="sxs-lookup"><span data-stu-id="7be89-114">Returns the callback mask.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be89-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7be89-115">Requirements</span></span>



| <span data-ttu-id="7be89-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be89-116">Requirement</span></span> | <span data-ttu-id="7be89-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7be89-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7be89-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7be89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7be89-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7be89-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7be89-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7be89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7be89-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7be89-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7be89-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7be89-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be89-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7be89-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





