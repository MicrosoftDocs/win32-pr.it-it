---
title: Messaggio MCM_SIZERECTTOMIN (COMmctrl. h)
description: Calcola il numero di calendari che si adattano al rettangolo specificato, quindi restituisce la dimensione minima che un rettangolo deve contenere per adattarsi a tale numero di calendari. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- Controlli di Windows Message MCM_SIZERECTTOMIN
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121306"
---
# <a name="mcm_sizerecttomin-message"></a><span data-ttu-id="42834-105">\_Messaggio SIZERECTTOMIN MCM</span><span class="sxs-lookup"><span data-stu-id="42834-105">MCM\_SIZERECTTOMIN message</span></span>

<span data-ttu-id="42834-106">Calcola il numero di calendari che si adattano al rettangolo specificato, quindi restituisce la dimensione minima che un rettangolo deve contenere per adattarsi a tale numero di calendari.</span><span class="sxs-lookup"><span data-stu-id="42834-106">Calculates how many calendars will fit in the given rectangle, and then returns the minimum size that a rectangle needs to be to fit that number of calendars.</span></span> <span data-ttu-id="42834-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) .</span><span class="sxs-lookup"><span data-stu-id="42834-107">You can send this message explicitly or by using the [**MonthCal\_SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="42834-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="42834-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42834-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42834-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42834-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="42834-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="42834-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42834-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42834-112">On entry, contiene un puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che descrive un'area maggiore o uguale alla dimensione necessaria per adattarsi al numero desiderato di calendari.</span><span class="sxs-lookup"><span data-stu-id="42834-112">On entry, contains a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that describes a region that is greater than or equal to the size necessary to fit the desired number of calendars.</span></span> <span data-ttu-id="42834-113">Quando questa funzione viene restituita, contiene la struttura **Rect** minima che corrisponde a questo numero di calendari.</span><span class="sxs-lookup"><span data-stu-id="42834-113">When this function returns, contains the minimum **RECT** structure that fits this number of calendars.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42834-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42834-114">Return value</span></span>

<span data-ttu-id="42834-115">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="42834-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="42834-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42834-116">Requirements</span></span>



| <span data-ttu-id="42834-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="42834-117">Requirement</span></span> | <span data-ttu-id="42834-118">Valore</span><span class="sxs-lookup"><span data-stu-id="42834-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42834-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42834-119">Minimum supported client</span></span><br/> | <span data-ttu-id="42834-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42834-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42834-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42834-121">Minimum supported server</span></span><br/> | <span data-ttu-id="42834-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42834-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42834-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42834-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="42834-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42834-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

