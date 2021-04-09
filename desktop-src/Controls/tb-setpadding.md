---
title: Messaggio TB_SETPADDING (COMmctrl. h)
description: Imposta la spaziatura interna per un controllo Toolbar.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- Controlli di Windows Message TB_SETPADDING
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121151"
---
# <a name="tb_setpadding-message"></a><span data-ttu-id="67a5c-104">\_Messaggio di SEPADDING TB</span><span class="sxs-lookup"><span data-stu-id="67a5c-104">TB\_SETPADDING message</span></span>

<span data-ttu-id="67a5c-105">Imposta la spaziatura interna per un controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="67a5c-105">Sets the padding for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="67a5c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="67a5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a5c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67a5c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67a5c-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="67a5c-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67a5c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67a5c-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la spaziatura interna orizzontale, in pixel.</span><span class="sxs-lookup"><span data-stu-id="67a5c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the horizontal padding, in pixels.</span></span> <span data-ttu-id="67a5c-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la spaziatura interna verticale, in pixel.</span><span class="sxs-lookup"><span data-stu-id="67a5c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67a5c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67a5c-112">Return value</span></span>

<span data-ttu-id="67a5c-113">Restituisce un valore **DWORD** che contiene la spaziatura orizzontale precedente in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la spaziatura verticale precedente in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))in pixel.</span><span class="sxs-lookup"><span data-stu-id="67a5c-113">Returns a **DWORD** value that contains the previous horizontal padding in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous vertical padding in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="67a5c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="67a5c-114">Remarks</span></span>

<span data-ttu-id="67a5c-115">I valori di riempimento vengono usati per creare un'area vuota tra il bordo del pulsante e l'immagine del pulsante e/o il testo.</span><span class="sxs-lookup"><span data-stu-id="67a5c-115">The padding values are used to create a blank area between the edge of the button and the button's image and/or text.</span></span> <span data-ttu-id="67a5c-116">La posizione e la quantità di riempimento effettivamente applicate variano a seconda del tipo di pulsante e della presenza di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="67a5c-116">Where and how much padding is actually applied depends on the type of the button and whether it has an image.</span></span> <span data-ttu-id="67a5c-117">La spaziatura interna orizzontale viene applicata sia a destra che a sinistra del pulsante e la spaziatura interna verticale viene applicata sia alla parte superiore che alla parte inferiore del pulsante.</span><span class="sxs-lookup"><span data-stu-id="67a5c-117">The horizontal padding is applied to both the right and left of the button, and the vertical padding is applied to both the top and bottom of the button.</span></span> <span data-ttu-id="67a5c-118">La spaziatura interna viene applicata solo ai pulsanti con stile [**\_ AUTOSIZE TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="67a5c-118">Padding is only applied to buttons that have the [**TBSTYLE\_AUTOSIZE**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="67a5c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67a5c-119">Requirements</span></span>



| <span data-ttu-id="67a5c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="67a5c-120">Requirement</span></span> | <span data-ttu-id="67a5c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="67a5c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67a5c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67a5c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="67a5c-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67a5c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67a5c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67a5c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="67a5c-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="67a5c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67a5c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67a5c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="67a5c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="67a5c-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67a5c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67a5c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a5c-129">**TB \_ GETpadding**</span><span class="sxs-lookup"><span data-stu-id="67a5c-129">**TB\_GETPADDING**</span></span>](tb-getpadding.md)
</dt> </dl>

 

