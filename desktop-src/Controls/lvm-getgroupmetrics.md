---
title: Messaggio LVM_GETGROUPMETRICS (COMmctrl. h)
description: Ottiene informazioni sulla visualizzazione dei gruppi.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- Controlli di Windows Message LVM_GETGROUPMETRICS
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5af8ec50fe74ab90a0f3e44a69e2cbc7dda583e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964746"
---
# <a name="lvm_getgroupmetrics-message"></a><span data-ttu-id="e8ff2-104">\_Messaggio GETGROUPMETRICS LVM</span><span class="sxs-lookup"><span data-stu-id="e8ff2-104">LVM\_GETGROUPMETRICS message</span></span>

<span data-ttu-id="e8ff2-105">Ottiene informazioni sulla visualizzazione dei gruppi.</span><span class="sxs-lookup"><span data-stu-id="e8ff2-105">Gets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8ff2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8ff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8ff2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8ff2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8ff2-108">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e8ff2-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="e8ff2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8ff2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e8ff2-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> che riceve la metrica recuperata.</span><span class="sxs-lookup"><span data-stu-id="e8ff2-110">A pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that receives the retrieved metrics.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8ff2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8ff2-111">Return value</span></span>

<span data-ttu-id="e8ff2-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e8ff2-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8ff2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8ff2-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8ff2-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="e8ff2-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e8ff2-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e8ff2-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8ff2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8ff2-116">Requirements</span></span>



| <span data-ttu-id="e8ff2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8ff2-117">Requirement</span></span> | <span data-ttu-id="e8ff2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e8ff2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ff2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8ff2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ff2-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8ff2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8ff2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8ff2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ff2-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8ff2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8ff2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8ff2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8ff2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8ff2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





