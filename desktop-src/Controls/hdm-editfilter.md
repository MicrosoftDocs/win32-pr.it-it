---
title: Messaggio HDM_EDITFILTER (COMmctrl. h)
description: Sposta lo stato attivo per l'input nella casella di modifica quando un pulsante di filtro dispone dello stato attivo.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- Controlli di Windows Message HDM_EDITFILTER
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742282"
---
# <a name="hdm_editfilter-message"></a><span data-ttu-id="eb852-104">\_Messaggio HDM EDITFILTER</span><span class="sxs-lookup"><span data-stu-id="eb852-104">HDM\_EDITFILTER message</span></span>

<span data-ttu-id="eb852-105">Sposta lo stato attivo per l'input nella casella di modifica quando un pulsante di filtro dispone dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="eb852-105">Moves the input focus to the edit box when a filter button has the focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb852-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb852-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb852-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb852-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb852-108">Valore che specifica la colonna da modificare.</span><span class="sxs-lookup"><span data-stu-id="eb852-108">A value specifying the column to edit.</span></span>

</dd> <dt>

<span data-ttu-id="eb852-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb852-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb852-110">Flag che specifica come gestire le modifiche apportate alla modifica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="eb852-110">A flag that specifies how to handle the user's editing changes.</span></span> <span data-ttu-id="eb852-111">Utilizzare questo flag per specificare le operazioni da eseguire se l'utente è in corso di modifica del filtro quando viene inviato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="eb852-111">Use this flag to specify what to do if the user is in the process of editing the filter when the message is sent.</span></span>



| <span data-ttu-id="eb852-112">Valore</span><span class="sxs-lookup"><span data-stu-id="eb852-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="eb852-113">Significato</span><span class="sxs-lookup"><span data-stu-id="eb852-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="eb852-114"><dt></dt>Valore <dt> **true**</dt></span><span class="sxs-lookup"><span data-stu-id="eb852-114"><dt></dt> <dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="eb852-115">Annullare le modifiche apportate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="eb852-115">Discard the changes made by the user.</span></span> <br/> |
| <dl> <span data-ttu-id="eb852-116"><dt></dt><dt> **False**</dt></span><span class="sxs-lookup"><span data-stu-id="eb852-116"><dt></dt> <dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="eb852-117">Accettare le modifiche apportate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="eb852-117">Accept the changes made by the user.</span></span> <br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb852-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb852-118">Return value</span></span>

<span data-ttu-id="eb852-119">Restituisce un Integer.</span><span class="sxs-lookup"><span data-stu-id="eb852-119">Returns an integer.</span></span> <span data-ttu-id="eb852-120">Viene eseguito il cast di **LRESULT** a un Integer che indica **true**(1) o **false**(0).</span><span class="sxs-lookup"><span data-stu-id="eb852-120">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb852-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb852-121">Requirements</span></span>



| <span data-ttu-id="eb852-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb852-122">Requirement</span></span> | <span data-ttu-id="eb852-123">Valore</span><span class="sxs-lookup"><span data-stu-id="eb852-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb852-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb852-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eb852-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb852-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb852-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb852-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eb852-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb852-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb852-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb852-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb852-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb852-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb852-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb852-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb852-131">**\_CLEARFILTER HDM**</span><span class="sxs-lookup"><span data-stu-id="eb852-131">**HDM\_CLEARFILTER**</span></span>](hdm-clearfilter.md)
</dt> </dl>

 

 





