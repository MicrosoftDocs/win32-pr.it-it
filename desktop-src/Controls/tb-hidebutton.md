---
title: Messaggio TB_HIDEBUTTON (COMmctrl. h)
description: Nasconde o Mostra il pulsante specificato in una barra degli strumenti.
ms.assetid: 57941a40-279a-426e-baf9-115429c62839
keywords:
- Controlli di Windows Message TB_HIDEBUTTON
topic_type:
- apiref
api_name:
- TB_HIDEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198a48ae65f13be699b76a20c9f423cdb0da197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964040"
---
# <a name="tb_hidebutton-message"></a><span data-ttu-id="11062-104">TB \_ HIDEBUTTON messaggio</span><span class="sxs-lookup"><span data-stu-id="11062-104">TB\_HIDEBUTTON message</span></span>

<span data-ttu-id="11062-105">Nasconde o Mostra il pulsante specificato in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="11062-105">Hides or shows the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="11062-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="11062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11062-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11062-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11062-108">Identificatore di comando del pulsante da nascondere o mostrare.</span><span class="sxs-lookup"><span data-stu-id="11062-108">Command identifier of the button to hide or show.</span></span>

</dd> <dt>

<span data-ttu-id="11062-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11062-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11062-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **bool** che indica se nascondere o visualizzare il pulsante specificato.</span><span class="sxs-lookup"><span data-stu-id="11062-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to hide or show the specified button.</span></span> <span data-ttu-id="11062-111">Se **true**, il pulsante è nascosto.</span><span class="sxs-lookup"><span data-stu-id="11062-111">If **TRUE**, the button is hidden.</span></span> <span data-ttu-id="11062-112">Se **false**, viene visualizzato il pulsante.</span><span class="sxs-lookup"><span data-stu-id="11062-112">If **FALSE**, the button is shown.</span></span>

<span data-ttu-id="11062-113">Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="11062-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11062-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11062-114">Return value</span></span>

<span data-ttu-id="11062-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="11062-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="11062-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11062-116">Requirements</span></span>



| <span data-ttu-id="11062-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="11062-117">Requirement</span></span> | <span data-ttu-id="11062-118">Valore</span><span class="sxs-lookup"><span data-stu-id="11062-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11062-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11062-119">Minimum supported client</span></span><br/> | <span data-ttu-id="11062-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11062-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11062-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11062-121">Minimum supported server</span></span><br/> | <span data-ttu-id="11062-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="11062-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11062-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11062-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="11062-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="11062-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

