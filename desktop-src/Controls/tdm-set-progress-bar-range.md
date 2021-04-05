---
title: Messaggio TDM_SET_PROGRESS_BAR_RANGE (COMmctrl. h)
description: Imposta i valori minimo e massimo per l'indicatore di stato in una finestra di dialogo attività.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- Controlli di Windows Message TDM_SET_PROGRESS_BAR_RANGE
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874593"
---
# <a name="tdm_set_progress_bar_range-message"></a><span data-ttu-id="b9c7e-104">Messaggio di intervallo indicatore di \_ stato set TDM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b9c7e-104">TDM\_SET\_PROGRESS\_BAR\_RANGE message</span></span>

<span data-ttu-id="b9c7e-105">Imposta i valori minimo e massimo per l'indicatore di stato in una finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="b9c7e-105">Sets the minimum and maximum values for the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9c7e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9c7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9c7e-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9c7e-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9c7e-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b9c7e-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b9c7e-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9c7e-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9c7e-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il valore minimo.</span><span class="sxs-lookup"><span data-stu-id="b9c7e-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum value.</span></span> <span data-ttu-id="b9c7e-111">Per impostazione predefinita, il valore minimo è zero.</span><span class="sxs-lookup"><span data-stu-id="b9c7e-111">By default, the minimum value is zero.</span></span> <span data-ttu-id="b9c7e-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="b9c7e-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum value.</span></span> <span data-ttu-id="b9c7e-113">Per impostazione predefinita, il valore massimo è 100.</span><span class="sxs-lookup"><span data-stu-id="b9c7e-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9c7e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9c7e-114">Return value</span></span>

<span data-ttu-id="b9c7e-115">Restituisce i valori minimo e massimo precedenti, se ha esito positivo, oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b9c7e-115">Returns the previous minimum and maximum values, if successful, or zero otherwise.</span></span> <span data-ttu-id="b9c7e-116">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene il valore minimo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="b9c7e-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9c7e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9c7e-117">Requirements</span></span>



| <span data-ttu-id="b9c7e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9c7e-118">Requirement</span></span> | <span data-ttu-id="b9c7e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b9c7e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c7e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9c7e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c7e-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9c7e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b9c7e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9c7e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c7e-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9c7e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b9c7e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9c7e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9c7e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9c7e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

