---
title: Messaggio LVM_SETGROUPMETRICS (COMmctrl. h)
description: Imposta le informazioni sulla visualizzazione dei gruppi.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- Controlli di Windows Message LVM_SETGROUPMETRICS
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215962e6f84aac83a2151b46f489938b575303c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340352"
---
# <a name="lvm_setgroupmetrics-message"></a><span data-ttu-id="60107-104">\_Messaggio SETGROUPMETRICS LVM</span><span class="sxs-lookup"><span data-stu-id="60107-104">LVM\_SETGROUPMETRICS message</span></span>

<span data-ttu-id="60107-105">Imposta le informazioni sulla visualizzazione dei gruppi.</span><span class="sxs-lookup"><span data-stu-id="60107-105">Sets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="60107-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60107-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60107-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60107-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="60107-108">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="60107-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="60107-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60107-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="60107-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> che contiene le metriche da impostare.</span><span class="sxs-lookup"><span data-stu-id="60107-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that contains the metrics to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60107-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60107-111">Return value</span></span>

<span data-ttu-id="60107-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="60107-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="60107-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="60107-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="60107-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="60107-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="60107-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="60107-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60107-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60107-116">Requirements</span></span>



| <span data-ttu-id="60107-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="60107-117">Requirement</span></span> | <span data-ttu-id="60107-118">Valore</span><span class="sxs-lookup"><span data-stu-id="60107-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60107-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60107-119">Minimum supported client</span></span><br/> | <span data-ttu-id="60107-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60107-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60107-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60107-121">Minimum supported server</span></span><br/> | <span data-ttu-id="60107-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60107-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60107-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60107-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="60107-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60107-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





