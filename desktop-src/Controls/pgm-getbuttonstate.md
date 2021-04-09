---
title: Messaggio PGM_GETBUTTONSTATE (COMmctrl. h)
description: Recupera lo stato del pulsante specificato in un controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetButtonState del cercapersone.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- Controlli di Windows Message PGM_GETBUTTONSTATE
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964559"
---
# <a name="pgm_getbuttonstate-message"></a><span data-ttu-id="ea8f1-105">\_Messaggio GETBUTTONSTATE PGM</span><span class="sxs-lookup"><span data-stu-id="ea8f1-105">PGM\_GETBUTTONSTATE message</span></span>

<span data-ttu-id="ea8f1-106">Recupera lo stato del pulsante specificato in un controllo pager.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-106">Retrieves the state of the specified button in a pager control.</span></span> <span data-ttu-id="ea8f1-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetButtonState del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) .</span><span class="sxs-lookup"><span data-stu-id="ea8f1-107">You can send this message explicitly or use the [**Pager\_GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea8f1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea8f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea8f1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ea8f1-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ea8f1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea8f1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea8f1-112">Indica il pulsante per il quale recuperare lo stato.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-112">Indicates which button to retrieve the state for.</span></span> <span data-ttu-id="ea8f1-113">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea8f1-113">This can be one of the following values:</span></span>



| <span data-ttu-id="ea8f1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ea8f1-114">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="ea8f1-115">Significato</span><span class="sxs-lookup"><span data-stu-id="ea8f1-115">Meaning</span></span>                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <span data-ttu-id="ea8f1-116"><dt>**\_TOPORLEFT PGB**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-116"><dt>**PGB\_TOPORLEFT**</dt></span></span> </dl>             | <span data-ttu-id="ea8f1-117">Indica il pulsante in alto in un controllo pager [**PGS \_ Vert**](pager-control-styles.md) o il pulsante sinistro in un controllo pager [**\_ orizzontalmente**](pager-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ea8f1-117">Indicates the top button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the left button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <span data-ttu-id="ea8f1-118"><dt>**\_BOTTOMORRIGHT PGB**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-118"><dt>**PGB\_BOTTOMORRIGHT**</dt></span></span> </dl> | <span data-ttu-id="ea8f1-119">Indica il pulsante in basso in un controllo pager [**PGS \_ Vert**](pager-control-styles.md) o il pulsante destro in un controllo pager [**\_ orizzontalmente**](pager-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ea8f1-119">Indicates the bottom button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the right button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8f1-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea8f1-120">Return value</span></span>

<span data-ttu-id="ea8f1-121">Restituisce lo stato del pulsante specificato in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-121">Returns the state of the button specified in *lParam*.</span></span> <span data-ttu-id="ea8f1-122">Si tratta di uno o più dei valori seguenti (se viene restituito più di un valore, questi verranno combinati usando un operatore OR bit per bit):</span><span class="sxs-lookup"><span data-stu-id="ea8f1-122">This will be one or more of the following values (if more then one value is returned they will be combined using a bitwise OR):</span></span>



| <span data-ttu-id="ea8f1-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ea8f1-123">Return code</span></span>                                                                                   | <span data-ttu-id="ea8f1-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea8f1-124">Description</span></span>                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="ea8f1-125"><dt>**PGF \_ invisibile**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-125"><dt>**PGF\_INVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="ea8f1-126">Il pulsante non è visibile.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-126">The button is not visible.</span></span> <br/>      |
| <dl> <span data-ttu-id="ea8f1-127"><dt>**PGF \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-127"><dt>**PGF\_NORMAL**</dt></span></span> </dl>    | <span data-ttu-id="ea8f1-128">Il pulsante è nello stato normale.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-128">The button is in normal state.</span></span> <br/>  |
| <dl> <span data-ttu-id="ea8f1-129"><dt>**PGF \_ grigio**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-129"><dt>**PGF\_GRAYED**</dt></span></span> </dl>    | <span data-ttu-id="ea8f1-130">Il pulsante è in stato grigio.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-130">The button is in grayed state.</span></span> <br/>  |
| <dl> <span data-ttu-id="ea8f1-131"><dt>**PGF \_ premuto**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-131"><dt>**PGF\_DEPRESSED**</dt></span></span> </dl> | <span data-ttu-id="ea8f1-132">Il pulsante è nello stato premuto.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-132">The button is in pressed state.</span></span> <br/> |
| <dl> <span data-ttu-id="ea8f1-133"><dt>**PGF \_ Hot**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-133"><dt>**PGF\_HOT**</dt></span></span> </dl>       | <span data-ttu-id="ea8f1-134">Il pulsante è nello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-134">The button is in hot state.</span></span> <br/>     |



 

## <a name="requirements"></a><span data-ttu-id="ea8f1-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea8f1-135">Requirements</span></span>



| <span data-ttu-id="ea8f1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea8f1-136">Requirement</span></span> | <span data-ttu-id="ea8f1-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ea8f1-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8f1-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea8f1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8f1-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea8f1-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea8f1-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea8f1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8f1-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea8f1-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea8f1-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea8f1-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea8f1-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-143"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





