---
title: Messaggio PBM_SETBARCOLOR (COMmctrl. h)
description: Imposta il colore della barra indicatore di stato nel controllo indicatore di stato.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- Controlli di Windows Message PBM_SETBARCOLOR
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518286"
---
# <a name="pbm_setbarcolor-message"></a><span data-ttu-id="027f2-104">\_Messaggio SETBARCOLOR PBM</span><span class="sxs-lookup"><span data-stu-id="027f2-104">PBM\_SETBARCOLOR message</span></span>

<span data-ttu-id="027f2-105">Imposta il colore della barra indicatore di stato nel controllo indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="027f2-105">Sets the color of the progress indicator bar in the progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="027f2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="027f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027f2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="027f2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="027f2-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="027f2-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="027f2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="027f2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="027f2-110">Valore **COLORREF** che specifica il nuovo colore della barra dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="027f2-110">The **COLORREF** value that specifies the new progress indicator bar color.</span></span> <span data-ttu-id="027f2-111">Se si specifica il \_ valore predefinito CLR, l'indicatore di stato utilizzerà il colore predefinito della barra dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="027f2-111">Specifying the CLR\_DEFAULT value causes the progress bar to use its default progress indicator bar color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="027f2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="027f2-112">Return value</span></span>

<span data-ttu-id="027f2-113">Restituisce il colore della barra dell'indicatore di stato precedente oppure il \_ valore predefinito CLR se il colore della barra dell'indicatore di stato è il colore predefinito.</span><span class="sxs-lookup"><span data-stu-id="027f2-113">Returns the previous progress indicator bar color, or CLR\_DEFAULT if the progress indicator bar color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="027f2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="027f2-114">Remarks</span></span>

<span data-ttu-id="027f2-115">Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="027f2-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="027f2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="027f2-116">Requirements</span></span>



| <span data-ttu-id="027f2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="027f2-117">Requirement</span></span> | <span data-ttu-id="027f2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="027f2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="027f2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="027f2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="027f2-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="027f2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="027f2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="027f2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="027f2-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="027f2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="027f2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="027f2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="027f2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="027f2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





