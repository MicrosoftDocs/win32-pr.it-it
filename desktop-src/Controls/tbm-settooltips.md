---
title: Messaggio TBM_SETTOOLTIPS (COMmctrl. h)
description: Assegna un controllo ToolTip a un controllo TrackBar.
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- Controlli di Windows Message TBM_SETTOOLTIPS
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475910"
---
# <a name="tbm_settooltips-message"></a><span data-ttu-id="8d158-104">\_Messaggio TBM SEtooltips</span><span class="sxs-lookup"><span data-stu-id="8d158-104">TBM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="8d158-105">Assegna un controllo ToolTip a un controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="8d158-105">Assigns a tooltip control to a trackbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d158-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d158-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d158-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d158-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d158-108">Handle per un controllo ToolTip esistente.</span><span class="sxs-lookup"><span data-stu-id="8d158-108">Handle to an existing tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="8d158-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d158-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8d158-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8d158-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d158-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d158-111">Return value</span></span>

<span data-ttu-id="8d158-112">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8d158-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d158-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d158-113">Remarks</span></span>

<span data-ttu-id="8d158-114">Quando viene creato un controllo TrackBar con lo stile delle [**\_ descrizioni comandi di TBS**](trackbar-control-styles.md) , viene creato un controllo ToolTip predefinito visualizzato accanto al dispositivo di scorrimento, che visualizza la posizione corrente del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="8d158-114">When a trackbar control is created with the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, it creates a default tooltip control that appears next to the slider, displaying the slider's current position.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d158-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d158-115">Requirements</span></span>



| <span data-ttu-id="8d158-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d158-116">Requirement</span></span> | <span data-ttu-id="8d158-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8d158-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d158-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d158-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8d158-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d158-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d158-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d158-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8d158-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d158-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d158-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d158-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d158-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d158-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





