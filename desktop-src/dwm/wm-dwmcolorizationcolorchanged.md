---
title: Messaggio WM_DWMCOLORIZATIONCOLORCHANGED (winuser. h)
description: Informa tutte le finestre di primo livello che il colore di colorazione è stato modificato.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- Messaggio WM_DWMCOLORIZATIONCOLORCHANGED Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119946"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a><span data-ttu-id="aaaaf-104">\_Messaggio DWMCOLORIZATIONCOLORCHANGED WM</span><span class="sxs-lookup"><span data-stu-id="aaaaf-104">WM\_DWMCOLORIZATIONCOLORCHANGED message</span></span>

<span data-ttu-id="aaaaf-105">Informa tutte le finestre di primo livello che il colore di colorazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-105">Informs all top-level windows that the colorization color has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="aaaaf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aaaaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaaaf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aaaaf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaaaf-108">Specifica il nuovo colore di colorazione.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-108">Specifies the new colorization color.</span></span> <span data-ttu-id="aaaaf-109">Il formato del colore è 0xAARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-109">The color format is 0xAARRGGBB.</span></span>

</dd> <dt>

<span data-ttu-id="aaaaf-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aaaaf-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaaaf-111">Specifica se il nuovo colore viene mescolato con l'opacità.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-111">Specifies whether the new color is blended with opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaaaf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aaaaf-112">Return value</span></span>

<span data-ttu-id="aaaaf-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaaaf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="aaaaf-114">Remarks</span></span>

<span data-ttu-id="aaaaf-115">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aaaaf-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="aaaaf-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) viene usato per determinare il valore del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) is used to determine the current color value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaaaf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aaaaf-117">Requirements</span></span>



| <span data-ttu-id="aaaaf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaaaf-118">Requirement</span></span> | <span data-ttu-id="aaaaf-119">Valore</span><span class="sxs-lookup"><span data-stu-id="aaaaf-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aaaaf-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaaaf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aaaaf-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aaaaf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aaaaf-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaaaf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aaaaf-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aaaaf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aaaaf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aaaaf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaaaf-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaaaf-125"><dt>Winuser.h</dt></span></span> </dl> |



 

