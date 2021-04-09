---
title: Messaggio MCM_GETMAXSELCOUNT (COMmctrl. h)
description: Recupera l'intervallo massimo di date che può essere selezionato in un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMaxSelCount.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- Controlli di Windows Message MCM_GETMAXSELCOUNT
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048518"
---
# <a name="mcm_getmaxselcount-message"></a><span data-ttu-id="97eff-105">\_Messaggio GETMAXSELCOUNT MCM</span><span class="sxs-lookup"><span data-stu-id="97eff-105">MCM\_GETMAXSELCOUNT message</span></span>

<span data-ttu-id="97eff-106">Recupera l'intervallo massimo di date che può essere selezionato in un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="97eff-106">Retrieves the maximum date range that can be selected in a month calendar control.</span></span> <span data-ttu-id="97eff-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="97eff-107">You can send this message explicitly or by using the [**MonthCal\_GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="97eff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="97eff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97eff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97eff-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="97eff-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="97eff-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="97eff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97eff-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="97eff-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="97eff-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97eff-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97eff-113">Return value</span></span>

<span data-ttu-id="97eff-114">Restituisce un valore INT che rappresenta il numero totale di giorni che è possibile selezionare per il controllo.</span><span class="sxs-lookup"><span data-stu-id="97eff-114">Returns an INT value that represents the total number of days that can be selected for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="97eff-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="97eff-115">Remarks</span></span>

<span data-ttu-id="97eff-116">È possibile modificare l'intervallo massimo di date selezionabile usando il messaggio [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="97eff-116">You can change the maximum date range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="97eff-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97eff-117">Requirements</span></span>



| <span data-ttu-id="97eff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="97eff-118">Requirement</span></span> | <span data-ttu-id="97eff-119">Valore</span><span class="sxs-lookup"><span data-stu-id="97eff-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97eff-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97eff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97eff-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97eff-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97eff-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97eff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97eff-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97eff-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97eff-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97eff-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="97eff-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97eff-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





