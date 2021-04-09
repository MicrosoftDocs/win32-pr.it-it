---
title: Messaggio CCM_GETUNICODEFORMAT (COMmctrl. h)
description: Ottiene il flag del formato carattere Unicode per il controllo.
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- Controlli di Windows Message CCM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d49ccc57faa05e86d12df130b12ce3d542bf6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120327"
---
# <a name="ccm_getunicodeformat-message"></a><span data-ttu-id="84a5f-104">\_Messaggio GETUNICODEFORMAT CCM</span><span class="sxs-lookup"><span data-stu-id="84a5f-104">CCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="84a5f-105">Ottiene il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="84a5f-105">Gets the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="84a5f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="84a5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84a5f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84a5f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="84a5f-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="84a5f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="84a5f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84a5f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="84a5f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="84a5f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84a5f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84a5f-111">Return value</span></span>

<span data-ttu-id="84a5f-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="84a5f-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="84a5f-113">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="84a5f-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="84a5f-114">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="84a5f-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="84a5f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84a5f-115">Requirements</span></span>



| <span data-ttu-id="84a5f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="84a5f-116">Requirement</span></span> | <span data-ttu-id="84a5f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="84a5f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84a5f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a5f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="84a5f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84a5f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84a5f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a5f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="84a5f-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84a5f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84a5f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84a5f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="84a5f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84a5f-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a5f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84a5f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a5f-125">**\_SETUNICODEFORMAT CCM**</span><span class="sxs-lookup"><span data-stu-id="84a5f-125">**CCM\_SETUNICODEFORMAT**</span></span>](ccm-setunicodeformat.md)
</dt> </dl>

 

 





