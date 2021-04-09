---
title: Messaggio SB_SIMPLE (COMmctrl. h)
description: Specifica se una finestra di stato Visualizza testo semplice o Visualizza tutte le parti della finestra impostate da un messaggio precedente della \_ parte SB.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- Controlli di Windows Message SB_SIMPLE
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120694"
---
# <a name="sb_simple-message"></a><span data-ttu-id="e6010-104">\_Messaggio semplice SB</span><span class="sxs-lookup"><span data-stu-id="e6010-104">SB\_SIMPLE message</span></span>

<span data-ttu-id="e6010-105">Specifica se una finestra di stato Visualizza testo semplice o Visualizza tutte le parti della finestra impostate da un messaggio precedente della [**\_ parte SB**](sb-setparts.md) .</span><span class="sxs-lookup"><span data-stu-id="e6010-105">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6010-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6010-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6010-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6010-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6010-108">Flag tipo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e6010-108">Display type flag.</span></span> <span data-ttu-id="e6010-109">Se questo parametro è **true**, nella finestra viene visualizzato un testo semplice.</span><span class="sxs-lookup"><span data-stu-id="e6010-109">If this parameter is **TRUE**, the window displays simple text.</span></span> <span data-ttu-id="e6010-110">Se è **false**, vengono visualizzate più parti.</span><span class="sxs-lookup"><span data-stu-id="e6010-110">If it is **FALSE**, it displays multiple parts.</span></span>

</dd> <dt>

<span data-ttu-id="e6010-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6010-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e6010-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e6010-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6010-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6010-113">Return value</span></span>

<span data-ttu-id="e6010-114">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e6010-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6010-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6010-115">Remarks</span></span>

<span data-ttu-id="e6010-116">Se la finestra di stato viene modificata da non semplice a semplice o viceversa, la finestra viene immediatamente ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="e6010-116">If the status window is being changed from nonsimple to simple, or vice versa, the window is immediately redrawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6010-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6010-117">Requirements</span></span>



| <span data-ttu-id="e6010-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6010-118">Requirement</span></span> | <span data-ttu-id="e6010-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e6010-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6010-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6010-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e6010-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6010-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6010-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6010-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e6010-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6010-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6010-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6010-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6010-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6010-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





