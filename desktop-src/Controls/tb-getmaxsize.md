---
title: Messaggio TB_GETMAXSIZE (COMmctrl. h)
description: Recupera la dimensione totale di tutti i pulsanti e i separatori visibili nella barra degli strumenti.
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- Controlli di Windows Message TB_GETMAXSIZE
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4829e65d90c04181369dd73b9c54634f1077144
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302126"
---
# <a name="tb_getmaxsize-message"></a><span data-ttu-id="ef84a-104">TB \_ GETMAXSIZE messaggio</span><span class="sxs-lookup"><span data-stu-id="ef84a-104">TB\_GETMAXSIZE message</span></span>

<span data-ttu-id="ef84a-105">Recupera la dimensione totale di tutti i pulsanti e i separatori visibili nella barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="ef84a-105">Retrieves the total size of all of the visible buttons and separators in the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef84a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef84a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef84a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef84a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ef84a-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ef84a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ef84a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef84a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef84a-110">Puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) che riceve le dimensioni degli elementi.</span><span class="sxs-lookup"><span data-stu-id="ef84a-110">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the size of the items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef84a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef84a-111">Return value</span></span>

<span data-ttu-id="ef84a-112">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ef84a-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef84a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef84a-113">Requirements</span></span>



| <span data-ttu-id="ef84a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef84a-114">Requirement</span></span> | <span data-ttu-id="ef84a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ef84a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef84a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef84a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef84a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef84a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef84a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef84a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef84a-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef84a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef84a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef84a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef84a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef84a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

