---
title: Messaggio LVM_GETINSERTMARKCOLOR (COMmctrl. h)
description: Recupera il colore del punto di inserimento.
ms.assetid: 1e98023a-9d26-4b87-bee4-bee4939ccfca
keywords:
- Controlli di Windows Message LVM_GETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18d6e9ed277f447f5097c0954819029d24b9cbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121770"
---
# <a name="lvm_getinsertmarkcolor-message"></a><span data-ttu-id="8fe75-104">\_Messaggio GETINSERTMARKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="8fe75-104">LVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="8fe75-105">Recupera il colore del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="8fe75-105">Retrieves the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fe75-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fe75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe75-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fe75-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8fe75-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8fe75-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8fe75-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fe75-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8fe75-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8fe75-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe75-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fe75-111">Return value</span></span>

<span data-ttu-id="8fe75-112">Restituisce una struttura **COLORREF** che contiene il colore del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="8fe75-112">Returns a **COLORREF** structure that contains the color of the insertion point.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fe75-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fe75-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8fe75-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="8fe75-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8fe75-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8fe75-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8fe75-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fe75-116">Requirements</span></span>



| <span data-ttu-id="8fe75-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fe75-117">Requirement</span></span> | <span data-ttu-id="8fe75-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8fe75-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe75-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fe75-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe75-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8fe75-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8fe75-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fe75-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe75-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8fe75-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8fe75-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fe75-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe75-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe75-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





