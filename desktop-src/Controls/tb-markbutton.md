---
title: Messaggio TB_MARKBUTTON (COMmctrl. h)
description: Imposta lo stato di evidenziazione di un pulsante specificato in un controllo Toolbar.
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- Controlli di Windows Message TB_MARKBUTTON
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d42983f5fb0ef6e62716cefa2fa8db4fca87fa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048598"
---
# <a name="tb_markbutton-message"></a><span data-ttu-id="c7319-104">TB \_ MARKBUTTON messaggio</span><span class="sxs-lookup"><span data-stu-id="c7319-104">TB\_MARKBUTTON message</span></span>

<span data-ttu-id="c7319-105">Imposta lo stato di evidenziazione di un pulsante specificato in un controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="c7319-105">Sets the highlight state of a given button in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7319-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7319-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7319-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7319-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7319-108">Identificatore del comando per un pulsante della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="c7319-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="c7319-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7319-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7319-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un **bool** che indica il nuovo stato di evidenziazione.</span><span class="sxs-lookup"><span data-stu-id="c7319-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates the new highlight state.</span></span> <span data-ttu-id="c7319-111">Se **true**, il pulsante è evidenziato.</span><span class="sxs-lookup"><span data-stu-id="c7319-111">If **TRUE**, the button is highlighted.</span></span> <span data-ttu-id="c7319-112">Se **false**, il pulsante è impostato sullo stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="c7319-112">If **FALSE**, the button is set to its default state.</span></span>

<span data-ttu-id="c7319-113">Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c7319-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7319-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7319-114">Return value</span></span>

<span data-ttu-id="c7319-115">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c7319-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7319-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7319-116">Requirements</span></span>



| <span data-ttu-id="c7319-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7319-117">Requirement</span></span> | <span data-ttu-id="c7319-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c7319-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7319-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7319-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c7319-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7319-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7319-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7319-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c7319-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7319-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7319-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7319-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7319-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7319-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

