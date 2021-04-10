---
title: Messaggio PBM_STEPIT (COMmctrl. h)
description: Sposta in avanti la posizione corrente di un indicatore di stato in base all'incremento del passaggio e ridisegnato la barra per riflettere la nuova posizione. Un'applicazione consente di impostare l'incremento del passaggio inviando il \_ messaggio di SEPASSO PBM.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- Controlli di Windows Message PBM_STEPIT
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964560"
---
# <a name="pbm_stepit-message"></a><span data-ttu-id="add88-105">\_Messaggio STEPIT PBM</span><span class="sxs-lookup"><span data-stu-id="add88-105">PBM\_STEPIT message</span></span>

<span data-ttu-id="add88-106">Sposta in avanti la posizione corrente di un indicatore di stato in base all'incremento del passaggio e ridisegnato la barra per riflettere la nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="add88-106">Advances the current position for a progress bar by the step increment and redraws the bar to reflect the new position.</span></span> <span data-ttu-id="add88-107">Un'applicazione consente di impostare l'incremento del passaggio inviando il messaggio di [**\_ sepasso PBM**](pbm-setstep.md) .</span><span class="sxs-lookup"><span data-stu-id="add88-107">An application sets the step increment by sending the [**PBM\_SETSTEP**](pbm-setstep.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="add88-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="add88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add88-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="add88-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="add88-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="add88-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="add88-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="add88-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="add88-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="add88-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add88-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="add88-113">Return value</span></span>

<span data-ttu-id="add88-114">Restituisce la posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="add88-114">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="add88-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="add88-115">Remarks</span></span>

<span data-ttu-id="add88-116">Quando la posizione supera il valore di intervallo massimo, questo messaggio Reimposta la posizione corrente in modo che l'indicatore di stato ricominci dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="add88-116">When the position exceeds the maximum range value, this message resets the current position so that the progress indicator starts over again from the beginning.</span></span>

## <a name="requirements"></a><span data-ttu-id="add88-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="add88-117">Requirements</span></span>



| <span data-ttu-id="add88-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="add88-118">Requirement</span></span> | <span data-ttu-id="add88-119">Valore</span><span class="sxs-lookup"><span data-stu-id="add88-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="add88-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="add88-120">Minimum supported client</span></span><br/> | <span data-ttu-id="add88-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="add88-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="add88-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="add88-122">Minimum supported server</span></span><br/> | <span data-ttu-id="add88-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="add88-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="add88-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="add88-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="add88-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="add88-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





