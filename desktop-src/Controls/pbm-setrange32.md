---
title: Messaggio PBM_SETRANGE32 (COMmctrl. h)
description: Imposta i valori minimo e massimo per un indicatore di stato su valori a 32 bit e ridisegnato la barra in modo da riflettere il nuovo intervallo.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- Controlli di Windows Message PBM_SETRANGE32
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742530"
---
# <a name="pbm_setrange32-message"></a><span data-ttu-id="64fd0-104">\_Messaggio SETRANGE32 PBM</span><span class="sxs-lookup"><span data-stu-id="64fd0-104">PBM\_SETRANGE32 message</span></span>

<span data-ttu-id="64fd0-105">Imposta i valori minimo e massimo per un indicatore di stato su valori a 32 bit e ridisegnato la barra in modo da riflettere il nuovo intervallo.</span><span class="sxs-lookup"><span data-stu-id="64fd0-105">Sets the minimum and maximum values for a progress bar to 32-bit values, and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="64fd0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64fd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64fd0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64fd0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64fd0-108">Valore minimo dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="64fd0-108">Minimum range value.</span></span> <span data-ttu-id="64fd0-109">Per impostazione predefinita, il valore minimo è zero.</span><span class="sxs-lookup"><span data-stu-id="64fd0-109">By default, the minimum value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="64fd0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64fd0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64fd0-111">Valore massimo dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="64fd0-111">Maximum range value.</span></span> <span data-ttu-id="64fd0-112">Questo valore deve essere maggiore di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="64fd0-112">This value must be greater than *wParam*.</span></span> <span data-ttu-id="64fd0-113">Per impostazione predefinita, il valore massimo è 100.</span><span class="sxs-lookup"><span data-stu-id="64fd0-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64fd0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64fd0-114">Return value</span></span>

<span data-ttu-id="64fd0-115">Restituisce un valore **DWORD** che include il limite minimo a 16 bit precedente nel relativo [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e il limite massimo a 16 bit precedente nel [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64fd0-115">Returns a **DWORD** value that holds the previous 16-bit low limit in its [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous 16-bit high limit in its [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="64fd0-116">Se gli intervalli precedenti sono valori a 32 bit, il valore restituito è costituito da **LOWORD** s di entrambi i limiti a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="64fd0-116">If the previous ranges were 32-bit values, the return value consists of the **LOWORD** s of both 32-bit limits.</span></span>

## <a name="remarks"></a><span data-ttu-id="64fd0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="64fd0-117">Remarks</span></span>

<span data-ttu-id="64fd0-118">Per recuperare tutti i valori a 32 bit massimi e Bassi, usare il messaggio [**PBM \_ GetRange**](pbm-getrange.md) .</span><span class="sxs-lookup"><span data-stu-id="64fd0-118">To retrieve the entire high and low 32-bit values, use the [**PBM\_GETRANGE**](pbm-getrange.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="64fd0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64fd0-119">Requirements</span></span>



| <span data-ttu-id="64fd0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="64fd0-120">Requirement</span></span> | <span data-ttu-id="64fd0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="64fd0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64fd0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64fd0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="64fd0-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64fd0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64fd0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64fd0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="64fd0-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64fd0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64fd0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64fd0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="64fd0-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="64fd0-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

