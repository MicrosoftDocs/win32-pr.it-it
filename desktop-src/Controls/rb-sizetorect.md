---
title: Messaggio RB_SIZETORECT (COMmctrl. h)
description: Tenta di trovare il layout migliore delle bande per il rettangolo specificato.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- Controlli di Windows Message RB_SIZETORECT
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121486"
---
# <a name="rb_sizetorect-message"></a><span data-ttu-id="ce76f-104">\_Messaggio SIZETORECT RB</span><span class="sxs-lookup"><span data-stu-id="ce76f-104">RB\_SIZETORECT message</span></span>

<span data-ttu-id="ce76f-105">Tenta di trovare il layout migliore delle bande per il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="ce76f-105">Attempts to find the best layout of the bands for the given rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce76f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce76f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce76f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce76f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ce76f-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ce76f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ce76f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce76f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce76f-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica il rettangolo in cui deve essere ridimensionato il controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="ce76f-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the rectangle to which the rebar control should be sized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce76f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce76f-111">Return value</span></span>

<span data-ttu-id="ce76f-112">Restituisce un valore diverso da zero se si è verificata una modifica del layout oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ce76f-112">Returns nonzero if a layout change occurred, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce76f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce76f-113">Remarks</span></span>

<span data-ttu-id="ce76f-114">Le bande Rebar verranno disposte e incapsulate in base alle esigenze per adattarsi al rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ce76f-114">The rebar bands will be arranged and wrapped as necessary to fit the rectangle.</span></span> <span data-ttu-id="ce76f-115">Le bande con lo \_ stile VARIABLEHEIGHT RBBS verranno ridimensionate nel modo più uniforme possibile per adattarsi al rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ce76f-115">Bands that have the RBBS\_VARIABLEHEIGHT style will be resized as evenly as possible to fit the rectangle.</span></span> <span data-ttu-id="ce76f-116">L'altezza di un Rebar orizzontale o la larghezza di un Rebar verticale può variare a seconda del nuovo layout.</span><span class="sxs-lookup"><span data-stu-id="ce76f-116">The height of a horizontal rebar or the width of a vertical rebar may change, depending on the new layout.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce76f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce76f-117">Requirements</span></span>



| <span data-ttu-id="ce76f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce76f-118">Requirement</span></span> | <span data-ttu-id="ce76f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ce76f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce76f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce76f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ce76f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce76f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce76f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce76f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ce76f-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce76f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce76f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce76f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce76f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce76f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

