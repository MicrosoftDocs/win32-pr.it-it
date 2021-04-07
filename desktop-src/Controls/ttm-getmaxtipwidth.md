---
title: Messaggio TTM_GETMAXTIPWIDTH (COMmctrl. h)
description: Recupera la larghezza massima per una finestra della descrizione comando.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- Controlli di Windows Message TTM_GETMAXTIPWIDTH
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964239"
---
# <a name="ttm_getmaxtipwidth-message"></a><span data-ttu-id="bbd19-104">\_Messaggio TTM GETMAXTIPWIDTH</span><span class="sxs-lookup"><span data-stu-id="bbd19-104">TTM\_GETMAXTIPWIDTH message</span></span>

<span data-ttu-id="bbd19-105">Recupera la larghezza massima per una finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="bbd19-105">Retrieves the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbd19-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbd19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbd19-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbd19-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bbd19-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bbd19-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bbd19-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbd19-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bbd19-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bbd19-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbd19-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbd19-111">Return value</span></span>

<span data-ttu-id="bbd19-112">Restituisce un valore **int** che rappresenta la larghezza massima della descrizione comando, in pixel.</span><span class="sxs-lookup"><span data-stu-id="bbd19-112">Returns an **INT** value that represents the maximum tooltip width, in pixels.</span></span> <span data-ttu-id="bbd19-113">Se la larghezza massima non è stata impostata in precedenza, il messaggio restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="bbd19-113">If no maximum width was set previously, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd19-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbd19-114">Remarks</span></span>

<span data-ttu-id="bbd19-115">Il valore di larghezza massima della descrizione comando non indica la larghezza effettiva della finestra descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="bbd19-115">The maximum tooltip width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="bbd19-116">Se invece una stringa della descrizione comando supera la larghezza massima, il controllo suddivide il testo in più righe, usando spazi per determinare le interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="bbd19-116">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="bbd19-117">Se il testo non può essere segmentato in più righe, verrà visualizzato su una sola riga.</span><span class="sxs-lookup"><span data-stu-id="bbd19-117">If the text cannot be segmented into multiple lines, it will be displayed on a single line.</span></span> <span data-ttu-id="bbd19-118">La lunghezza di questa riga può superare la larghezza massima della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="bbd19-118">The length of this line may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd19-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbd19-119">Requirements</span></span>



| <span data-ttu-id="bbd19-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbd19-120">Requirement</span></span> | <span data-ttu-id="bbd19-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bbd19-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd19-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbd19-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd19-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bbd19-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbd19-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbd19-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd19-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bbd19-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbd19-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbd19-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbd19-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbd19-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd19-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbd19-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd19-129">**\_SETMAXTIPWIDTH TTM**</span><span class="sxs-lookup"><span data-stu-id="bbd19-129">**TTM\_SETMAXTIPWIDTH**</span></span>](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





