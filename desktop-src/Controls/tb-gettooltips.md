---
title: Messaggio TB_GETTOOLTIPS (COMmctrl. h)
description: Recupera l'handle per il controllo ToolTip, se presente, associato alla barra degli strumenti.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- Controlli di Windows Message TB_GETTOOLTIPS
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048446"
---
# <a name="tb_gettooltips-message"></a><span data-ttu-id="a144a-104">\_Messaggio GETtooltips TB</span><span class="sxs-lookup"><span data-stu-id="a144a-104">TB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="a144a-105">Recupera l'handle per il controllo ToolTip, se presente, associato alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="a144a-105">Retrieves the handle to the tooltip control, if any, associated with the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a144a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a144a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a144a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a144a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a144a-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a144a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a144a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a144a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a144a-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a144a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a144a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a144a-111">Return value</span></span>

<span data-ttu-id="a144a-112">Restituisce l'handle per il controllo ToolTip oppure **null** se alla barra degli strumenti non è associata alcuna descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="a144a-112">Returns the handle to the tooltip control, or **NULL** if the toolbar has no associated tooltip.</span></span>

## <a name="requirements"></a><span data-ttu-id="a144a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a144a-113">Requirements</span></span>



| <span data-ttu-id="a144a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a144a-114">Requirement</span></span> | <span data-ttu-id="a144a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a144a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a144a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a144a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a144a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a144a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a144a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a144a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a144a-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a144a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a144a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a144a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a144a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a144a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





