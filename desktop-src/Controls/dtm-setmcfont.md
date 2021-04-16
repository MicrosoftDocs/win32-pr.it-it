---
title: Messaggio DTM_SETMCFONT (COMmctrl. h)
description: Imposta il tipo di carattere che verrà utilizzato dal controllo Calendar Month Child del controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- Controlli di Windows Message DTM_SETMCFONT
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477932"
---
# <a name="dtm_setmcfont-message"></a><span data-ttu-id="c965d-105">\_Messaggio SETMCFONT DTM</span><span class="sxs-lookup"><span data-stu-id="c965d-105">DTM\_SETMCFONT message</span></span>

<span data-ttu-id="c965d-106">Imposta il tipo di carattere che verrà utilizzato dal controllo Calendar Month Child del controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="c965d-106">Sets the font to be used by the date and time picker (DTP) control's child month calendar control.</span></span> <span data-ttu-id="c965d-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="c965d-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c965d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c965d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c965d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c965d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c965d-110">Handle per il tipo di carattere che verrà impostato.</span><span class="sxs-lookup"><span data-stu-id="c965d-110">A handle to the font that will be set.</span></span>

</dd> <dt>

<span data-ttu-id="c965d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c965d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c965d-112">Specifica se il controllo deve essere ridisegnato immediatamente dopo l'impostazione del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="c965d-112">Specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="c965d-113">Se si imposta questo parametro su **true** , il controllo verrà ridisegnato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c965d-113">Setting this parameter to **TRUE** causes the control to redraw itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c965d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c965d-114">Return value</span></span>

<span data-ttu-id="c965d-115">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c965d-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c965d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c965d-116">Requirements</span></span>



| <span data-ttu-id="c965d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c965d-117">Requirement</span></span> | <span data-ttu-id="c965d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c965d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c965d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c965d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c965d-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c965d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c965d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c965d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c965d-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c965d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c965d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c965d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c965d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c965d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





