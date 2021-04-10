---
title: Messaggio RB_GETBANDMARGINS (COMmctrl. h)
description: Recupera i margini di una banda.
ms.assetid: 262f4180-53f9-428f-9360-75b762470270
keywords:
- Controlli di Windows Message RB_GETBANDMARGINS
topic_type:
- apiref
api_name:
- RB_GETBANDMARGINS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ab77c057073d9816d1310b1e8cb39fd374956b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964551"
---
# <a name="rb_getbandmargins-message"></a><span data-ttu-id="1499a-104">\_Messaggio GETBANDMARGINS RB</span><span class="sxs-lookup"><span data-stu-id="1499a-104">RB\_GETBANDMARGINS message</span></span>

<span data-ttu-id="1499a-105">Recupera i margini di una banda.</span><span class="sxs-lookup"><span data-stu-id="1499a-105">Retrieves the margins of a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="1499a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1499a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1499a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1499a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1499a-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1499a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1499a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1499a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1499a-110">Puntatore a una struttura dei [**margini**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) che riceve i margini recuperati.</span><span class="sxs-lookup"><span data-stu-id="1499a-110">Pointer to a [**MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) structure that receives the retrieved margins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1499a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1499a-111">Return value</span></span>

<span data-ttu-id="1499a-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1499a-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="1499a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1499a-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1499a-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="1499a-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1499a-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1499a-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1499a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1499a-116">Requirements</span></span>



| <span data-ttu-id="1499a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1499a-117">Requirement</span></span> | <span data-ttu-id="1499a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1499a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1499a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1499a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1499a-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1499a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1499a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1499a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1499a-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1499a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1499a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1499a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1499a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1499a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





