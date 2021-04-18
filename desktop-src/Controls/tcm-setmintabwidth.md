---
title: Messaggio TCM_SETMINTABWIDTH (COMmctrl. h)
description: Imposta la larghezza minima degli elementi in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl SetMinTabWidth.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- Controlli di Windows Message TCM_SETMINTABWIDTH
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300969"
---
# <a name="tcm_setmintabwidth-message"></a><span data-ttu-id="eca0f-105">\_Messaggio TCM SETMINTABWIDTH</span><span class="sxs-lookup"><span data-stu-id="eca0f-105">TCM\_SETMINTABWIDTH message</span></span>

<span data-ttu-id="eca0f-106">Imposta la larghezza minima degli elementi in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="eca0f-106">Sets the minimum width of items in a tab control.</span></span> <span data-ttu-id="eca0f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) .</span><span class="sxs-lookup"><span data-stu-id="eca0f-107">You can send this message explicitly or by using the [**TabCtrl\_SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eca0f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eca0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eca0f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eca0f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eca0f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="eca0f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eca0f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eca0f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eca0f-112">Larghezza minima da impostare per un elemento di controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="eca0f-112">Minimum width to be set for a tab control item.</span></span> <span data-ttu-id="eca0f-113">Se questo parametro è impostato su-1, il controllo utilizzerà la larghezza predefinita della scheda.</span><span class="sxs-lookup"><span data-stu-id="eca0f-113">If this parameter is set to -1, the control will use the default tab width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eca0f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eca0f-114">Return value</span></span>

<span data-ttu-id="eca0f-115">Restituisce un valore INT che rappresenta la larghezza minima della scheda precedente.</span><span class="sxs-lookup"><span data-stu-id="eca0f-115">Returns an INT value that represents the previous minimum tab width.</span></span>

## <a name="requirements"></a><span data-ttu-id="eca0f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eca0f-116">Requirements</span></span>



| <span data-ttu-id="eca0f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eca0f-117">Requirement</span></span> | <span data-ttu-id="eca0f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="eca0f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eca0f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eca0f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eca0f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eca0f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eca0f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eca0f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eca0f-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eca0f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eca0f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eca0f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eca0f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eca0f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





