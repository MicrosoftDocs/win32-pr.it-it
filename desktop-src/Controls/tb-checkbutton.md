---
title: Messaggio TB_CHECKBUTTON (COMmctrl. h)
description: Controlla o deseleziona un pulsante specificato in una barra degli strumenti.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- Controlli di Windows Message TB_CHECKBUTTON
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7734b37da44db38d9ca09b34ad9e666cc90eb5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048770"
---
# <a name="tb_checkbutton-message"></a><span data-ttu-id="20607-104">TB \_ CHECKBUTTON messaggio</span><span class="sxs-lookup"><span data-stu-id="20607-104">TB\_CHECKBUTTON message</span></span>

<span data-ttu-id="20607-105">Controlla o deseleziona un pulsante specificato in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="20607-105">Checks or unchecks a given button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="20607-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20607-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20607-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20607-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20607-108">Identificatore di comando del pulsante da verificare.</span><span class="sxs-lookup"><span data-stu-id="20607-108">Command identifier of the button to check.</span></span>

</dd> <dt>

<span data-ttu-id="20607-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20607-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20607-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **bool** che indica se selezionare o deselezionare il pulsante specificato.</span><span class="sxs-lookup"><span data-stu-id="20607-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to check or uncheck the specified button.</span></span> <span data-ttu-id="20607-111">Se **true**, viene aggiunto il controllo.</span><span class="sxs-lookup"><span data-stu-id="20607-111">If **TRUE**, the check is added.</span></span> <span data-ttu-id="20607-112">Se **false**, il controllo viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="20607-112">If **FALSE**, the check is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20607-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20607-113">Return value</span></span>

<span data-ttu-id="20607-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="20607-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="20607-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="20607-115">Remarks</span></span>

<span data-ttu-id="20607-116">Quando si seleziona un pulsante, questo viene visualizzato nello stato premuto.</span><span class="sxs-lookup"><span data-stu-id="20607-116">When a button is checked, it is displayed in the pressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="20607-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20607-117">Requirements</span></span>



| <span data-ttu-id="20607-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="20607-118">Requirement</span></span> | <span data-ttu-id="20607-119">Valore</span><span class="sxs-lookup"><span data-stu-id="20607-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20607-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20607-120">Minimum supported client</span></span><br/> | <span data-ttu-id="20607-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20607-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20607-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20607-122">Minimum supported server</span></span><br/> | <span data-ttu-id="20607-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="20607-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20607-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20607-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="20607-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="20607-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

