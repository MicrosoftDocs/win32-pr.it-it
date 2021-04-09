---
title: Messaggio PGM_SETPOS (COMmctrl. h)
description: Imposta la posizione di scorrimento corrente per il controllo cercapersone. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro SetPos del cercapersone.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- Controlli di Windows Message PGM_SETPOS
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741223"
---
# <a name="pgm_setpos-message"></a><span data-ttu-id="cb84a-105">\_Messaggio SETPOS PGM</span><span class="sxs-lookup"><span data-stu-id="cb84a-105">PGM\_SETPOS message</span></span>

<span data-ttu-id="cb84a-106">Imposta la posizione di scorrimento corrente per il controllo cercapersone.</span><span class="sxs-lookup"><span data-stu-id="cb84a-106">Sets the current scroll position for the pager control.</span></span> <span data-ttu-id="cb84a-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ SetPos del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) .</span><span class="sxs-lookup"><span data-stu-id="cb84a-107">You can send this message explicitly or use the [**Pager\_SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb84a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb84a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb84a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb84a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cb84a-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cb84a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cb84a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb84a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb84a-112">Valore di tipo **int** che contiene la nuova posizione di scorrimento, in pixel.</span><span class="sxs-lookup"><span data-stu-id="cb84a-112">Value of type **int** that contains the new scroll position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb84a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb84a-113">Return value</span></span>

<span data-ttu-id="cb84a-114">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cb84a-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb84a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb84a-115">Requirements</span></span>



| <span data-ttu-id="cb84a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb84a-116">Requirement</span></span> | <span data-ttu-id="cb84a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cb84a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb84a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb84a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb84a-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb84a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb84a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb84a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb84a-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb84a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb84a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb84a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb84a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb84a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





