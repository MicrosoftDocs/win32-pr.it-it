---
title: Messaggio TB_INSERTBUTTON (COMmctrl. h)
description: Inserisce un pulsante in una barra degli strumenti.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- Controlli di Windows Message TB_INSERTBUTTON
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119447"
---
# <a name="tb_insertbutton-message"></a><span data-ttu-id="4cde8-104">TB \_ INSERTBUTTON messaggio</span><span class="sxs-lookup"><span data-stu-id="4cde8-104">TB\_INSERTBUTTON message</span></span>

<span data-ttu-id="4cde8-105">Inserisce un pulsante in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="4cde8-105">Inserts a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cde8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cde8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cde8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cde8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cde8-108">Indice in base zero di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="4cde8-108">Zero-based index of a button.</span></span> <span data-ttu-id="4cde8-109">Il messaggio inserisce il pulsante nuovo a sinistra di questo pulsante.</span><span class="sxs-lookup"><span data-stu-id="4cde8-109">The message inserts the new button to the left of this button.</span></span>

</dd> <dt>

<span data-ttu-id="4cde8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cde8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cde8-111">Puntatore a una struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) contenente informazioni sul pulsante da inserire.</span><span class="sxs-lookup"><span data-stu-id="4cde8-111">Pointer to a [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure containing information about the button to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cde8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cde8-112">Return value</span></span>

<span data-ttu-id="4cde8-113">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4cde8-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cde8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cde8-114">Requirements</span></span>



| <span data-ttu-id="4cde8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cde8-115">Requirement</span></span> | <span data-ttu-id="4cde8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4cde8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cde8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cde8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4cde8-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cde8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cde8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cde8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4cde8-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4cde8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cde8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cde8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cde8-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cde8-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4cde8-123">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4cde8-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4cde8-124">**TB \_ INSERTBUTTONW** (Unicode) e **TB \_ INSERTBUTTONA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4cde8-124">**TB\_INSERTBUTTONW** (Unicode) and **TB\_INSERTBUTTONA** (ANSI)</span></span><br/>           |



 

 





