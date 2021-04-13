---
title: Messaggio TDM_SET_PROGRESS_BAR_STATE (COMmctrl. h)
description: Imposta lo stato dell'indicatore di stato in una finestra di dialogo attività.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- Controlli di Windows Message TDM_SET_PROGRESS_BAR_STATE
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2021
ms.locfileid: "104352036"
---
# <a name="tdm_set_progress_bar_state-message"></a><span data-ttu-id="84df3-104">\_Messaggio di \_ stato della barra di \_ \_ stato set TDM</span><span class="sxs-lookup"><span data-stu-id="84df3-104">TDM\_SET\_PROGRESS\_BAR\_STATE message</span></span>

<span data-ttu-id="84df3-105">Imposta lo stato dell'indicatore di stato in una finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="84df3-105">Sets the state of the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="84df3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="84df3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84df3-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84df3-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84df3-108">Valore **int** che specifica lo stato dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="84df3-108">An **int** that specifies the state of the progress bar.</span></span> <span data-ttu-id="84df3-109">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="84df3-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="84df3-110">Valore</span><span class="sxs-lookup"><span data-stu-id="84df3-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="84df3-111">Significato</span><span class="sxs-lookup"><span data-stu-id="84df3-111">Meaning</span></span>                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="84df3-112"><dt>**PBST \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="84df3-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="84df3-113">Imposta lo stato normale per l'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="84df3-113">Sets the progress bar to the normal state.</span></span><br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="84df3-114"><dt>**PBST \_ sospeso**</dt></span><span class="sxs-lookup"><span data-stu-id="84df3-114"><dt>**PBST\_PAUSED**</dt></span></span> </dl>    | <span data-ttu-id="84df3-115">Imposta l'indicatore di stato sullo stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="84df3-115">Sets the progress bar to the paused state.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="84df3-116"><dt>**\_errore PBST**</dt></span><span class="sxs-lookup"><span data-stu-id="84df3-116"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="84df3-117">Impostare l'indicatore di stato sullo stato di errore.</span><span class="sxs-lookup"><span data-stu-id="84df3-117">Set the progress bar to the error state.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="84df3-118">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84df3-118">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84df3-119">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="84df3-119">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84df3-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84df3-120">Return value</span></span>

<span data-ttu-id="84df3-121">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="84df3-121">If the function succeeds, the return value is non zero.</span></span>

<span data-ttu-id="84df3-122">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="84df3-122">If the function fails, the return value is zero.</span></span> <span data-ttu-id="84df3-123">Per ottenere informazioni estese sull'errore, chiamare GetLastError.</span><span class="sxs-lookup"><span data-stu-id="84df3-123">To get extended error information call GetLastError.</span></span>

## <a name="requirements"></a><span data-ttu-id="84df3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84df3-124">Requirements</span></span>



| <span data-ttu-id="84df3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="84df3-125">Requirement</span></span> | <span data-ttu-id="84df3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="84df3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84df3-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84df3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="84df3-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84df3-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84df3-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84df3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="84df3-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84df3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84df3-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84df3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="84df3-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84df3-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





