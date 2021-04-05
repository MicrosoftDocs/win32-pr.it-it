---
title: Messaggio TB_INDETERMINATE (COMmctrl. h)
description: Imposta o cancella lo stato indeterminato del pulsante specificato in una barra degli strumenti.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- Controlli di Windows Message TB_INDETERMINATE
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048189"
---
# <a name="tb_indeterminate-message"></a><span data-ttu-id="1d58d-104">TB \_ messaggio INdeterminato</span><span class="sxs-lookup"><span data-stu-id="1d58d-104">TB\_INDETERMINATE message</span></span>

<span data-ttu-id="1d58d-105">Imposta o cancella lo stato indeterminato del pulsante specificato in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="1d58d-105">Sets or clears the indeterminate state of the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d58d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d58d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d58d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d58d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d58d-108">Identificatore di comando del pulsante di cui è necessario impostare o deselezionare lo stato indeterminato.</span><span class="sxs-lookup"><span data-stu-id="1d58d-108">Command identifier of the button whose indeterminate state is to be set or cleared.</span></span>

</dd> <dt>

<span data-ttu-id="1d58d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d58d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d58d-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un **bool** che indica se impostare o deselezionare lo stato indeterminato.</span><span class="sxs-lookup"><span data-stu-id="1d58d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to set or clear the indeterminate state.</span></span> <span data-ttu-id="1d58d-111">Se **true**, viene impostato lo stato indeterminato.</span><span class="sxs-lookup"><span data-stu-id="1d58d-111">If **TRUE**, the indeterminate state is set.</span></span> <span data-ttu-id="1d58d-112">Se **false**, lo stato è deselezionato.</span><span class="sxs-lookup"><span data-stu-id="1d58d-112">If **FALSE**, the state is cleared.</span></span>

<span data-ttu-id="1d58d-113">Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1d58d-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d58d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d58d-114">Return value</span></span>

<span data-ttu-id="1d58d-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1d58d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d58d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d58d-116">Requirements</span></span>



| <span data-ttu-id="1d58d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d58d-117">Requirement</span></span> | <span data-ttu-id="1d58d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1d58d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d58d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d58d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1d58d-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d58d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d58d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d58d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1d58d-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d58d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d58d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d58d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d58d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d58d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

