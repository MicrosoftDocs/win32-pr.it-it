---
title: Messaggio PGM_SETCHILD (COMmctrl. h)
description: Imposta la finestra contenuta per il controllo pager.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- Controlli di Windows Message PGM_SETCHILD
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119582"
---
# <a name="pgm_setchild-message"></a><span data-ttu-id="595ad-104">\_Messaggio del messaggio PGM</span><span class="sxs-lookup"><span data-stu-id="595ad-104">PGM\_SETCHILD message</span></span>

<span data-ttu-id="595ad-105">Imposta la finestra contenuta per il controllo pager.</span><span class="sxs-lookup"><span data-stu-id="595ad-105">Sets the contained window for the pager control.</span></span> <span data-ttu-id="595ad-106">Questo messaggio non modificherà l'elemento padre della finestra contenuta; assegna un handle di finestra al controllo pager per lo scorrimento.</span><span class="sxs-lookup"><span data-stu-id="595ad-106">This message will not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling.</span></span> <span data-ttu-id="595ad-107">Nella maggior parte dei casi, la finestra contenuta sarà una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="595ad-107">In most cases, the contained window will be a child window.</span></span> <span data-ttu-id="595ad-108">In tal caso, la finestra contenuta deve essere un elemento figlio del controllo pager.</span><span class="sxs-lookup"><span data-stu-id="595ad-108">If this is the case, the contained window should be a child of the pager control.</span></span> <span data-ttu-id="595ad-109">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**pager \_ figlio**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) .</span><span class="sxs-lookup"><span data-stu-id="595ad-109">You can send this message explicitly or use the [**Pager\_SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="595ad-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="595ad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="595ad-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="595ad-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="595ad-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="595ad-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="595ad-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="595ad-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="595ad-114">Handle per la finestra da contenere.</span><span class="sxs-lookup"><span data-stu-id="595ad-114">Handle to the window to be contained.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="595ad-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="595ad-115">Return value</span></span>

<span data-ttu-id="595ad-116">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="595ad-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="595ad-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="595ad-117">Requirements</span></span>



| <span data-ttu-id="595ad-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="595ad-118">Requirement</span></span> | <span data-ttu-id="595ad-119">Valore</span><span class="sxs-lookup"><span data-stu-id="595ad-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="595ad-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="595ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="595ad-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="595ad-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="595ad-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="595ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="595ad-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="595ad-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="595ad-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="595ad-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="595ad-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="595ad-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





