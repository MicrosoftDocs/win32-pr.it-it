---
title: Messaggio PBM_DELTAPOS (COMmctrl. h)
description: Sposta in avanti la posizione corrente di un indicatore di stato in base a un incremento specificato e ridisegnato la barra per riflettere la nuova posizione.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- Controlli di Windows Message PBM_DELTAPOS
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048555"
---
# <a name="pbm_deltapos-message"></a><span data-ttu-id="9a4df-104">\_Messaggio DELTAPOS PBM</span><span class="sxs-lookup"><span data-stu-id="9a4df-104">PBM\_DELTAPOS message</span></span>

<span data-ttu-id="9a4df-105">Sposta in avanti la posizione corrente di un indicatore di stato in base a un incremento specificato e ridisegnato la barra per riflettere la nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="9a4df-105">Advances the current position of a progress bar by a specified increment and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a4df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a4df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a4df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a4df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a4df-108">Quantità per far avanzare la posizione.</span><span class="sxs-lookup"><span data-stu-id="9a4df-108">Amount to advance the position.</span></span>

</dd> <dt>

<span data-ttu-id="9a4df-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a4df-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9a4df-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9a4df-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a4df-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a4df-111">Return value</span></span>

<span data-ttu-id="9a4df-112">Restituisce la posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="9a4df-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a4df-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a4df-113">Remarks</span></span>

<span data-ttu-id="9a4df-114">Se l'incremento restituisce un valore non compreso nell'intervallo del controllo, la posizione viene impostata sul limite più vicino.</span><span class="sxs-lookup"><span data-stu-id="9a4df-114">If the increment results in a value outside the range of the control, the position is set to the nearest boundary.</span></span>

<span data-ttu-id="9a4df-115">Il comportamento di questo messaggio non è definito se viene inviato a un controllo con stile di [**\_ selezione PBS**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4df-115">The behavior of this message is undefined if it is sent to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a4df-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a4df-116">Requirements</span></span>



| <span data-ttu-id="9a4df-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a4df-117">Requirement</span></span> | <span data-ttu-id="9a4df-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9a4df-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a4df-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a4df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9a4df-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a4df-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a4df-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a4df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9a4df-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a4df-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a4df-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a4df-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a4df-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a4df-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





