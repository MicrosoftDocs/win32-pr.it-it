---
title: Messaggio LB_GETHORIZONTALEXTENT (winuser. h)
description: Ottiene la larghezza, in pixel, in cui è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole) se nella casella di riepilogo è presente una barra di scorrimento orizzontale.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- Controlli di Windows Message LB_GETHORIZONTALEXTENT
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964858"
---
# <a name="lb_gethorizontalextent-message"></a><span data-ttu-id="30693-104">\_Messaggio GETHORIZONTALEXTENT lb</span><span class="sxs-lookup"><span data-stu-id="30693-104">LB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="30693-105">Ottiene la larghezza, in pixel, in cui è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole) se nella casella di riepilogo è presente una barra di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="30693-105">Gets the width, in pixels, that a list box can be scrolled horizontally (the scrollable width) if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="30693-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="30693-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30693-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30693-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30693-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="30693-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="30693-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30693-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30693-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="30693-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30693-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30693-111">Return value</span></span>

<span data-ttu-id="30693-112">Il valore restituito è la larghezza dello scorrimento, in pixel, della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="30693-112">The return value is the scrollable width, in pixels, of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="30693-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="30693-113">Remarks</span></span>

<span data-ttu-id="30693-114">Per rispondere al messaggio **lb \_ GETHORIZONTALEXTENT** , è necessario che la casella di riepilogo sia stata definita con lo stile [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="30693-114">To respond to the **LB\_GETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="30693-115">Se l'applicazione non imposta l'extent orizzontale della casella di riepilogo (usando [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), l'extent orizzontale predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="30693-115">If the application does not set the horizontal extent of the list box (using [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), the default horizontal extent is zero.</span></span> <span data-ttu-id="30693-116">Si noti che la casella di riepilogo non aggiorna in modo dinamico l'extent orizzontale.</span><span class="sxs-lookup"><span data-stu-id="30693-116">Note that the list box does not update its horizontal extent dynamically.</span></span>

## <a name="requirements"></a><span data-ttu-id="30693-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30693-117">Requirements</span></span>



| <span data-ttu-id="30693-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30693-118">Requirement</span></span> | <span data-ttu-id="30693-119">Valore</span><span class="sxs-lookup"><span data-stu-id="30693-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30693-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30693-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30693-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30693-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="30693-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30693-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30693-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30693-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30693-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30693-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30693-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30693-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30693-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30693-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30693-127">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="30693-127">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

