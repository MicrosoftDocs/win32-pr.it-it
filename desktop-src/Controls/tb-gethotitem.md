---
title: Messaggio TB_GETHOTITEM (COMmctrl. h)
description: Recupera l'indice dell'elemento attivo in una barra degli strumenti.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- Controlli di Windows Message TB_GETHOTITEM
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476301"
---
# <a name="tb_gethotitem-message"></a><span data-ttu-id="b40f5-104">TB \_ GETHOTITEM messaggio</span><span class="sxs-lookup"><span data-stu-id="b40f5-104">TB\_GETHOTITEM message</span></span>

<span data-ttu-id="b40f5-105">Recupera l'indice dell'elemento attivo in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="b40f5-105">Retrieves the index of the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b40f5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b40f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b40f5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b40f5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b40f5-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b40f5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b40f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b40f5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b40f5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b40f5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b40f5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b40f5-111">Return value</span></span>

<span data-ttu-id="b40f5-112">Restituisce l'indice dell'elemento attivo oppure-1 se non è impostato alcun elemento attivo.</span><span class="sxs-lookup"><span data-stu-id="b40f5-112">Returns the index of the hot item, or -1 if no hot item is set.</span></span> <span data-ttu-id="b40f5-113">I controlli della barra degli strumenti che non hanno lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) non hanno elementi sensibili.</span><span class="sxs-lookup"><span data-stu-id="b40f5-113">Toolbar controls that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style do not have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="b40f5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b40f5-114">Requirements</span></span>



| <span data-ttu-id="b40f5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b40f5-115">Requirement</span></span> | <span data-ttu-id="b40f5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b40f5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b40f5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b40f5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b40f5-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b40f5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b40f5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b40f5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b40f5-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b40f5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b40f5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b40f5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b40f5-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b40f5-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





