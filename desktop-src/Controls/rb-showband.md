---
title: Messaggio RB_SHOWBAND (COMmctrl. h)
description: Mostra o nasconde una determinata banda in un controllo Rebar.
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- Controlli di Windows Message RB_SHOWBAND
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27c9cedeb42e7eeed9432af9c2a040ac4991810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121483"
---
# <a name="rb_showband-message"></a><span data-ttu-id="7d11b-104">\_Messaggio SHOWBAND RB</span><span class="sxs-lookup"><span data-stu-id="7d11b-104">RB\_SHOWBAND message</span></span>

<span data-ttu-id="7d11b-105">Mostra o nasconde una determinata banda in un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="7d11b-105">Shows or hides a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d11b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d11b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d11b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d11b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d11b-108">Indice in base zero di una banda nel controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="7d11b-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="7d11b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d11b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d11b-110">Valore **bool** che indica se la banda deve essere mostrata o nascosta.</span><span class="sxs-lookup"><span data-stu-id="7d11b-110">**BOOL** value that indicates if the band should be shown or hidden.</span></span> <span data-ttu-id="7d11b-111">Se questo valore è diverso da zero, verrà visualizzata la banda.</span><span class="sxs-lookup"><span data-stu-id="7d11b-111">If this value is nonzero, the band will be shown.</span></span> <span data-ttu-id="7d11b-112">In caso contrario, la banda sarà nascosta.</span><span class="sxs-lookup"><span data-stu-id="7d11b-112">Otherwise, the band will be hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d11b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d11b-113">Return value</span></span>

<span data-ttu-id="7d11b-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7d11b-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d11b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d11b-115">Requirements</span></span>



| <span data-ttu-id="7d11b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d11b-116">Requirement</span></span> | <span data-ttu-id="7d11b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7d11b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d11b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d11b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7d11b-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d11b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d11b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d11b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7d11b-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d11b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d11b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d11b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d11b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d11b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





