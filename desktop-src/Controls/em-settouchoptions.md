---
title: Messaggio di EM_SETTOUCHOPTIONS (RichEdit. h)
description: Imposta le opzioni di tocco associate a un controllo Rich Edit.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- Controlli di Windows Message EM_SETTOUCHOPTIONS
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477308"
---
# <a name="em_settouchoptions-message"></a><span data-ttu-id="2584e-104">\_Messaggio SETTOUCHOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="2584e-104">EM\_SETTOUCHOPTIONS message</span></span>

<span data-ttu-id="2584e-105">Imposta le opzioni di tocco associate a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2584e-105">Sets the touch options associated with a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2584e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2584e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2584e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2584e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2584e-108">Opzione di tocco da impostare.</span><span class="sxs-lookup"><span data-stu-id="2584e-108">The touch option to set.</span></span> <span data-ttu-id="2584e-109">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2584e-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2584e-110">Valore</span><span class="sxs-lookup"><span data-stu-id="2584e-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="2584e-111">Significato</span><span class="sxs-lookup"><span data-stu-id="2584e-111">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="2584e-112"><dt>**\_SHOWHANDLES RTO**</dt></span><span class="sxs-lookup"><span data-stu-id="2584e-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="2584e-113">Mostrare o nascondere i punti di manipolazione del tocco, a seconda del valore di *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2584e-113">Show or hide the touch gripper handles, depending on the value of *lParam*.</span></span><br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="2584e-114"><dt>**\_DISABLEHANDLES RTO**</dt></span><span class="sxs-lookup"><span data-stu-id="2584e-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="2584e-115">Consente di abilitare o disabilitare gli handle del grip touch, a seconda del valore di *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2584e-115">Enable or disable the touch gripper handles, depending on the value of *lParam*.</span></span> <span data-ttu-id="2584e-116">Quando gli handle sono disabilitati, vengono nascosti se sono visibili e rimangono nascosti fino a quando un messaggio **\_ SETTOUCHOPTIONS em** non cambia il proprio stato.</span><span class="sxs-lookup"><span data-stu-id="2584e-116">When handles are disabled, they are hidden if they are visible and remain hidden until an **EM\_SETTOUCHOPTIONS** message changes their status.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="2584e-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2584e-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2584e-118">Impostare su **true** per visualizzare/abilitare gli handle di selezione tocco oppure su **false** per nascondere o disabilitare gli handle di selezione tocco.</span><span class="sxs-lookup"><span data-stu-id="2584e-118">Set to **TRUE** to show/enable the touch selection handles, or **FALSE** to hide/disable the touch selection handles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2584e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2584e-119">Return value</span></span>

<span data-ttu-id="2584e-120">Questo messaggio restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="2584e-120">This message returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2584e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2584e-121">Requirements</span></span>



| <span data-ttu-id="2584e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2584e-122">Requirement</span></span> | <span data-ttu-id="2584e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2584e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2584e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2584e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2584e-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2584e-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2584e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2584e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2584e-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2584e-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2584e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2584e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2584e-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2584e-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2584e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2584e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2584e-131">**\_GETTOUCHOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="2584e-131">**EM\_GETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





