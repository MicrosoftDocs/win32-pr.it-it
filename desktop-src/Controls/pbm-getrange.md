---
title: Messaggio PBM_GETRANGE (COMmctrl. h)
description: Recupera le informazioni sui limiti massimo e minimo correnti di un determinato controllo indicatore di stato.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- Controlli di Windows Message PBM_GETRANGE
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964566"
---
# <a name="pbm_getrange-message"></a><span data-ttu-id="6b1ea-104">Messaggio della gestione della serie di Criteri PBM \_</span><span class="sxs-lookup"><span data-stu-id="6b1ea-104">PBM\_GETRANGE message</span></span>

<span data-ttu-id="6b1ea-105">Recupera le informazioni sui limiti massimo e minimo correnti di un determinato controllo indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="6b1ea-105">Retrieves information about the current high and low limits of a given progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b1ea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b1ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b1ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b1ea-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b1ea-108">Valore del flag che specifica il valore del limite da utilizzare come valore restituito del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6b1ea-108">Flag value specifying which limit value is to be used as the message's return value.</span></span> <span data-ttu-id="6b1ea-109">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b1ea-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="6b1ea-110">Valore</span><span class="sxs-lookup"><span data-stu-id="6b1ea-110">Value</span></span>                                                                                                                                    | <span data-ttu-id="6b1ea-111">Significato</span><span class="sxs-lookup"><span data-stu-id="6b1ea-111">Meaning</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="6b1ea-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6b1ea-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="6b1ea-113">Restituisce il limite minimo.</span><span class="sxs-lookup"><span data-stu-id="6b1ea-113">Return the low limit.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="6b1ea-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6b1ea-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="6b1ea-115">Restituisce il limite massimo.</span><span class="sxs-lookup"><span data-stu-id="6b1ea-115">Return the high limit.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b1ea-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b1ea-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b1ea-117">Puntatore a una struttura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) che deve essere riempita con i limiti massimo e minimo del controllo indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="6b1ea-117">Pointer to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with the high and low limits of the progress bar control.</span></span> <span data-ttu-id="6b1ea-118">Se questo parametro è impostato su **null**, il controllo restituirà solo il limite specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="6b1ea-118">If this parameter is set to **NULL**, the control will return only the limit specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b1ea-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b1ea-119">Return value</span></span>

<span data-ttu-id="6b1ea-120">Restituisce un valore INT che rappresenta il valore limite specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="6b1ea-120">Returns an INT that represents the limit value specified by *wParam*.</span></span> <span data-ttu-id="6b1ea-121">Se *lParam* non è **null**, *lParam* deve puntare a una struttura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) che deve essere riempita con entrambi i valori limite.</span><span class="sxs-lookup"><span data-stu-id="6b1ea-121">If *lParam* is not **NULL**, *lParam* must point to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with both limit values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b1ea-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b1ea-122">Requirements</span></span>



| <span data-ttu-id="6b1ea-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b1ea-123">Requirement</span></span> | <span data-ttu-id="6b1ea-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6b1ea-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1ea-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b1ea-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6b1ea-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b1ea-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b1ea-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b1ea-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6b1ea-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b1ea-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b1ea-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b1ea-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b1ea-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b1ea-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





