---
title: Messaggio PBM_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo nell'indicatore di stato.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- Controlli di Windows Message PBM_SETBKCOLOR
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742538"
---
# <a name="pbm_setbkcolor-message"></a><span data-ttu-id="7ffd1-104">\_Messaggio SETBKCOLOR PBM</span><span class="sxs-lookup"><span data-stu-id="7ffd1-104">PBM\_SETBKCOLOR message</span></span>

<span data-ttu-id="7ffd1-105">Imposta il colore di sfondo nell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="7ffd1-105">Sets the background color in the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ffd1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ffd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ffd1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ffd1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ffd1-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7ffd1-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7ffd1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ffd1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ffd1-110">Valore **COLORREF** che specifica il nuovo colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="7ffd1-110">**COLORREF** value that specifies the new background color.</span></span> <span data-ttu-id="7ffd1-111">Specificare il \_ valore predefinito CLR per fare in modo che l'indicatore di stato utilizzi il colore di sfondo predefinito.</span><span class="sxs-lookup"><span data-stu-id="7ffd1-111">Specify the CLR\_DEFAULT value to cause the progress bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ffd1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ffd1-112">Return value</span></span>

<span data-ttu-id="7ffd1-113">Restituisce il colore di sfondo precedente oppure il \_ valore predefinito CLR se il colore di sfondo è il colore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7ffd1-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ffd1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ffd1-114">Remarks</span></span>

<span data-ttu-id="7ffd1-115">Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="7ffd1-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ffd1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ffd1-116">Requirements</span></span>



| <span data-ttu-id="7ffd1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ffd1-117">Requirement</span></span> | <span data-ttu-id="7ffd1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7ffd1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffd1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ffd1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7ffd1-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ffd1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ffd1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ffd1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7ffd1-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ffd1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ffd1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ffd1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ffd1-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ffd1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





