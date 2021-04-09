---
title: Messaggio PGM_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro SetBkColor del cercapersone.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- Controlli di Windows Message PGM_SETBKCOLOR
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119586"
---
# <a name="pgm_setbkcolor-message"></a><span data-ttu-id="fe053-105">\_Messaggio SETBKCOLOR PGM</span><span class="sxs-lookup"><span data-stu-id="fe053-105">PGM\_SETBKCOLOR message</span></span>

<span data-ttu-id="fe053-106">Imposta il colore di sfondo corrente per il controllo pager.</span><span class="sxs-lookup"><span data-stu-id="fe053-106">Sets the current background color for the pager control.</span></span> <span data-ttu-id="fe053-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ SetBkColor del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="fe053-107">You can send this message explicitly or use the [**Pager\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe053-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe053-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe053-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe053-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fe053-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fe053-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fe053-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe053-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe053-112">Valore **COLORREF** che contiene il nuovo colore di sfondo del controllo pager.</span><span class="sxs-lookup"><span data-stu-id="fe053-112">**COLORREF** value that contains the new background color of the pager control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe053-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe053-113">Return value</span></span>

<span data-ttu-id="fe053-114">Restituisce un valore **COLORREF** che contiene il colore di sfondo precedente.</span><span class="sxs-lookup"><span data-stu-id="fe053-114">Returns a **COLORREF** value that contains the previous background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe053-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe053-115">Remarks</span></span>

<span data-ttu-id="fe053-116">Per impostazione predefinita, il controllo pager utilizzerà il colore della superficie del pulsante di sistema come colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="fe053-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="fe053-117">Si tratta dello stesso colore che può essere recuperato chiamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con il colore \_ BTNFACE.</span><span class="sxs-lookup"><span data-stu-id="fe053-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe053-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe053-118">Requirements</span></span>



| <span data-ttu-id="fe053-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe053-119">Requirement</span></span> | <span data-ttu-id="fe053-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fe053-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe053-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe053-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fe053-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe053-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe053-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe053-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fe053-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe053-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe053-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe053-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe053-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe053-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

