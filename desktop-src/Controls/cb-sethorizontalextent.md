---
title: Messaggio CB_SETHORIZONTALEXTENT (winuser. h)
description: Un'applicazione invia il \_ messaggio SETHORIZONTALEXTENT CB per impostare la larghezza, in pixel, in base alla quale è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- Controlli di Windows Message CB_SETHORIZONTALEXTENT
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476630"
---
# <a name="cb_sethorizontalextent-message"></a><span data-ttu-id="bd526-104">\_Messaggio SETHORIZONTALEXTENT CB</span><span class="sxs-lookup"><span data-stu-id="bd526-104">CB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="bd526-105">Un'applicazione invia il **messaggio \_ SETHORIZONTALEXTENT CB** per impostare la larghezza, in pixel, in base alla quale è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole).</span><span class="sxs-lookup"><span data-stu-id="bd526-105">An application sends the **CB\_SETHORIZONTALEXTENT** message to set the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="bd526-106">Se la larghezza della casella di riepilogo è inferiore a questo valore, la barra di scorrimento orizzontale scorre orizzontalmente gli elementi nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="bd526-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="bd526-107">Se la larghezza della casella di riepilogo è maggiore o uguale a questo valore, la barra di scorrimento orizzontale è nascosta o, se la casella combinata ha lo stile [**CBS \_ DISABLENOSCROLL**](combo-box-styles.md) , disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bd526-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden or, if the combo box has the [**CBS\_DISABLENOSCROLL**](combo-box-styles.md) style, disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd526-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd526-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd526-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd526-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd526-110">Specifica la larghezza scorrevole della casella di riepilogo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="bd526-110">Specifies the scrollable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bd526-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd526-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd526-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="bd526-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd526-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd526-113">Requirements</span></span>



| <span data-ttu-id="bd526-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd526-114">Requirement</span></span> | <span data-ttu-id="bd526-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bd526-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd526-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd526-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bd526-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd526-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bd526-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd526-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bd526-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd526-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd526-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd526-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd526-121"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd526-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd526-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd526-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd526-123">**CB \_ GETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="bd526-123">**CB\_GETHORIZONTALEXTENT**</span></span>](cb-gethorizontalextent.md)
</dt> </dl>

 

 





