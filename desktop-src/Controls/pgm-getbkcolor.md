---
title: Messaggio PGM_GETBKCOLOR (COMmctrl. h)
description: Recupera il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetBkColor del cercapersone.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- Controlli di Windows Message PGM_GETBKCOLOR
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742527"
---
# <a name="pgm_getbkcolor-message"></a><span data-ttu-id="10830-105">\_Messaggio GETBKCOLOR PGM</span><span class="sxs-lookup"><span data-stu-id="10830-105">PGM\_GETBKCOLOR message</span></span>

<span data-ttu-id="10830-106">Recupera il colore di sfondo corrente per il controllo pager.</span><span class="sxs-lookup"><span data-stu-id="10830-106">Retrieves the current background color for the pager control.</span></span> <span data-ttu-id="10830-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetBkColor del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="10830-107">You can send this message explicitly or use the [**Pager\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="10830-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="10830-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10830-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10830-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="10830-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="10830-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="10830-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10830-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="10830-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="10830-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10830-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10830-113">Return value</span></span>

<span data-ttu-id="10830-114">Restituisce un valore **COLORREF** che contiene il colore di sfondo corrente.</span><span class="sxs-lookup"><span data-stu-id="10830-114">Returns a **COLORREF** value that contains the current background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="10830-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="10830-115">Remarks</span></span>

<span data-ttu-id="10830-116">Per impostazione predefinita, il controllo pager utilizzerà il colore della superficie del pulsante di sistema come colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="10830-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="10830-117">Si tratta dello stesso colore che può essere recuperato chiamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con il colore \_ BTNFACE.</span><span class="sxs-lookup"><span data-stu-id="10830-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="10830-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10830-118">Requirements</span></span>



| <span data-ttu-id="10830-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="10830-119">Requirement</span></span> | <span data-ttu-id="10830-120">Valore</span><span class="sxs-lookup"><span data-stu-id="10830-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10830-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10830-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10830-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10830-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10830-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10830-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10830-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10830-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10830-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10830-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="10830-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10830-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

