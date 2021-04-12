---
title: Messaggio TTM_SETMAXTIPWIDTH (COMmctrl. h)
description: Imposta la larghezza massima per una finestra della descrizione comando.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- Controlli di Windows Message TTM_SETMAXTIPWIDTH
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225209"
---
# <a name="ttm_setmaxtipwidth-message"></a><span data-ttu-id="f7d71-104">\_Messaggio TTM SETMAXTIPWIDTH</span><span class="sxs-lookup"><span data-stu-id="f7d71-104">TTM\_SETMAXTIPWIDTH message</span></span>

<span data-ttu-id="f7d71-105">Imposta la larghezza massima per una finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="f7d71-105">Sets the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7d71-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7d71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d71-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7d71-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f7d71-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f7d71-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f7d71-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7d71-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d71-110">Lunghezza massima della finestra ToolTip oppure-1 per consentire qualsiasi larghezza.</span><span class="sxs-lookup"><span data-stu-id="f7d71-110">Maximum tooltip window width, or -1 to allow any width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d71-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7d71-111">Return value</span></span>

<span data-ttu-id="f7d71-112">Restituisce la larghezza massima precedente della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="f7d71-112">Returns the previous maximum tooltip width.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d71-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7d71-113">Remarks</span></span>

<span data-ttu-id="f7d71-114">Il valore di larghezza massima non indica la larghezza effettiva della finestra descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="f7d71-114">The maximum width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="f7d71-115">Se invece una stringa della descrizione comando supera la larghezza massima, il controllo suddivide il testo in più righe, usando spazi per determinare le interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="f7d71-115">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="f7d71-116">Se il testo non può essere segmentato in più righe, viene visualizzato su una sola riga, che può superare la larghezza massima della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="f7d71-116">If the text cannot be segmented into multiple lines, it is displayed on a single line, which may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d71-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7d71-117">Requirements</span></span>



| <span data-ttu-id="f7d71-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7d71-118">Requirement</span></span> | <span data-ttu-id="f7d71-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f7d71-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d71-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7d71-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d71-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7d71-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7d71-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7d71-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d71-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7d71-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7d71-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7d71-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d71-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d71-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d71-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7d71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d71-127">**\_GETMAXTIPWIDTH TTM**</span><span class="sxs-lookup"><span data-stu-id="f7d71-127">**TTM\_GETMAXTIPWIDTH**</span></span>](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





