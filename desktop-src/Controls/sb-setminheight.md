---
title: Messaggio SB_SETMINHEIGHT (COMmctrl. h)
description: Imposta l'altezza minima dell'area di disegno di una finestra di stato.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- Controlli di Windows Message SB_SETMINHEIGHT
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964637"
---
# <a name="sb_setminheight-message"></a><span data-ttu-id="97239-104">\_Messaggio SETMINHEIGHT SB</span><span class="sxs-lookup"><span data-stu-id="97239-104">SB\_SETMINHEIGHT message</span></span>

<span data-ttu-id="97239-105">Imposta l'altezza minima dell'area di disegno di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="97239-105">Sets the minimum height of a status window's drawing area.</span></span>

## <a name="parameters"></a><span data-ttu-id="97239-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="97239-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97239-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97239-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97239-108">Altezza minima, in pixel, della finestra.</span><span class="sxs-lookup"><span data-stu-id="97239-108">Minimum height, in pixels, of the window.</span></span>

</dd> <dt>

<span data-ttu-id="97239-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97239-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="97239-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="97239-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97239-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97239-111">Return value</span></span>

<span data-ttu-id="97239-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="97239-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="97239-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="97239-113">Remarks</span></span>

<span data-ttu-id="97239-114">L'altezza minima è la somma di *wParam* e il doppio della larghezza, in pixel, del bordo verticale della finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="97239-114">The minimum height is the sum of *wParam* and twice the width, in pixels, of the vertical border of the status window.</span></span> <span data-ttu-id="97239-115">Per ricreare la finestra, un'applicazione deve inviare il messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) alla finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="97239-115">An application must send the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to the status window to redraw the window.</span></span> <span data-ttu-id="97239-116">I parametri *wParam* e *lParam* del messaggio **\_ dimensioni WM** devono essere impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="97239-116">The *wParam* and *lParam* parameters of the **WM\_SIZE** message should be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="97239-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97239-117">Requirements</span></span>



| <span data-ttu-id="97239-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="97239-118">Requirement</span></span> | <span data-ttu-id="97239-119">Valore</span><span class="sxs-lookup"><span data-stu-id="97239-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97239-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97239-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97239-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97239-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97239-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97239-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97239-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97239-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97239-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97239-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="97239-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97239-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

