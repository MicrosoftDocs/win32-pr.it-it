---
title: Messaggio TTM_DELTOOL (COMmctrl. h)
description: Rimuove uno strumento da un controllo ToolTip.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- Controlli di Windows Message TTM_DELTOOL
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301657"
---
# <a name="ttm_deltool-message"></a><span data-ttu-id="56679-104">\_Messaggio TTM DELTOOL</span><span class="sxs-lookup"><span data-stu-id="56679-104">TTM\_DELTOOL message</span></span>

<span data-ttu-id="56679-105">Rimuove uno strumento da un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="56679-105">Removes a tool from a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="56679-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="56679-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56679-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56679-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="56679-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="56679-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="56679-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56679-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56679-110">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="56679-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="56679-111">I membri **HWND** e **UID** identificano lo strumento da rimuovere e il membro **cbSize** deve specificare le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="56679-111">The **hwnd** and **uId** members identify the tool to remove, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="56679-112">Tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="56679-112">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56679-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56679-113">Return value</span></span>

<span data-ttu-id="56679-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="56679-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="56679-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56679-115">Requirements</span></span>



| <span data-ttu-id="56679-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="56679-116">Requirement</span></span> | <span data-ttu-id="56679-117">Valore</span><span class="sxs-lookup"><span data-stu-id="56679-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56679-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56679-118">Minimum supported client</span></span><br/> | <span data-ttu-id="56679-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56679-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56679-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56679-120">Minimum supported server</span></span><br/> | <span data-ttu-id="56679-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56679-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56679-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56679-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="56679-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56679-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="56679-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="56679-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="56679-125">**TTM \_ DELTOOLW** (Unicode) e **TTM \_ DELTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="56679-125">**TTM\_DELTOOLW** (Unicode) and **TTM\_DELTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="56679-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56679-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="56679-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="56679-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="56679-128">**\_ADDTOOL TTM**</span><span class="sxs-lookup"><span data-stu-id="56679-128">**TTM\_ADDTOOL**</span></span>](ttm-addtool.md)
</dt> <dt>

<span data-ttu-id="56679-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="56679-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="56679-130">Informazioni sui controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="56679-130">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





