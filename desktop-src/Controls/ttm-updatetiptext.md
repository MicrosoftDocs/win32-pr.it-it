---
title: Messaggio TTM_UPDATETIPTEXT (COMmctrl. h)
description: Imposta il testo della descrizione comando per uno strumento.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- Controlli di Windows Message TTM_UPDATETIPTEXT
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120274"
---
# <a name="ttm_updatetiptext-message"></a><span data-ttu-id="c0ede-104">\_Messaggio TTM UPDATETIPTEXT</span><span class="sxs-lookup"><span data-stu-id="c0ede-104">TTM\_UPDATETIPTEXT message</span></span>

<span data-ttu-id="c0ede-105">Imposta il testo della descrizione comando per uno strumento.</span><span class="sxs-lookup"><span data-stu-id="c0ede-105">Sets the tooltip text for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0ede-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0ede-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0ede-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0ede-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c0ede-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c0ede-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c0ede-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0ede-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0ede-110">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="c0ede-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="c0ede-111">I membri **hInst** e **lpszText** devono specificare l'handle dell'istanza e l'indirizzo del testo.</span><span class="sxs-lookup"><span data-stu-id="c0ede-111">The **hinst** and **lpszText** members must specify the instance handle and the address of the text.</span></span> <span data-ttu-id="c0ede-112">I membri **HWND** e **UID** identificano lo strumento da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c0ede-112">The **hwnd** and **uId** members identify the tool to update.</span></span> <span data-ttu-id="c0ede-113">Prima di inviare questo messaggio, è necessario compilare il membro **cbSize** della struttura.</span><span class="sxs-lookup"><span data-stu-id="c0ede-113">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0ede-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0ede-114">Return value</span></span>

<span data-ttu-id="c0ede-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c0ede-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ede-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0ede-116">Requirements</span></span>



| <span data-ttu-id="c0ede-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0ede-117">Requirement</span></span> | <span data-ttu-id="c0ede-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c0ede-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ede-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0ede-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ede-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0ede-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0ede-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0ede-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ede-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0ede-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0ede-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0ede-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0ede-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0ede-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c0ede-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c0ede-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c0ede-126">**TTM \_ UPDATETIPTEXTW** (Unicode) e **TTM \_ UPDATETIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c0ede-126">**TTM\_UPDATETIPTEXTW** (Unicode) and **TTM\_UPDATETIPTEXTA** (ANSI)</span></span><br/>       |



 

 





