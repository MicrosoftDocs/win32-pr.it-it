---
title: Messaggio PGM_SETBUTTONSIZE (COMmctrl. h)
description: Imposta la dimensione corrente del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro SetButtonSize del cercapersone.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- Controlli di Windows Message PGM_SETBUTTONSIZE
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517644"
---
# <a name="pgm_setbuttonsize-message"></a><span data-ttu-id="fc09b-105">\_Messaggio SETBUTTONSIZE PGM</span><span class="sxs-lookup"><span data-stu-id="fc09b-105">PGM\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="fc09b-106">Imposta la dimensione corrente del pulsante per il controllo pager.</span><span class="sxs-lookup"><span data-stu-id="fc09b-106">Sets the current button size for the pager control.</span></span> <span data-ttu-id="fc09b-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ SetButtonSize del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="fc09b-107">You can send this message explicitly or use the [**Pager\_SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc09b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc09b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc09b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc09b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fc09b-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fc09b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fc09b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc09b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc09b-112">Valore di tipo **int** che contiene le nuove dimensioni del pulsante, in pixel.</span><span class="sxs-lookup"><span data-stu-id="fc09b-112">Value of type **int** that contains the new button size, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc09b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc09b-113">Return value</span></span>

<span data-ttu-id="fc09b-114">Restituisce un valore **int** che contiene le dimensioni del pulsante precedenti, in pixel.</span><span class="sxs-lookup"><span data-stu-id="fc09b-114">Returns an **int** value that contains the previous button size, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc09b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc09b-115">Remarks</span></span>

<span data-ttu-id="fc09b-116">Se il controllo pager dispone dello [**stile \_ orizzontalmente PGS**](pager-control-styles.md) , le dimensioni del pulsante determinano la larghezza dei pulsanti del cercapersone.</span><span class="sxs-lookup"><span data-stu-id="fc09b-116">If the pager control has the [**PGS\_HORZ**](pager-control-styles.md) style, the button size determines the width of the pager buttons.</span></span> <span data-ttu-id="fc09b-117">Se il controllo pager presenta lo stile [**PGS \_ Vert**](pager-control-styles.md) , le dimensioni del pulsante determinano l'altezza dei pulsanti di spostamento.</span><span class="sxs-lookup"><span data-stu-id="fc09b-117">If the pager control has the [**PGS\_VERT**](pager-control-styles.md) style, the button size determines the height of the pager buttons.</span></span> <span data-ttu-id="fc09b-118">Per impostazione predefinita, il controllo pager imposta le dimensioni del pulsante su tre quarti della larghezza della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="fc09b-118">By default, the pager control sets its button size to three-fourths of the width of the scroll bar.</span></span>

<span data-ttu-id="fc09b-119">Il pulsante del cercapersone presenta una dimensione minima, attualmente 12 pixel.</span><span class="sxs-lookup"><span data-stu-id="fc09b-119">There is a minimum size to the pager button, currently 12 pixels.</span></span> <span data-ttu-id="fc09b-120">Tuttavia, questo può cambiare in modo da non dipendere da questo valore.</span><span class="sxs-lookup"><span data-stu-id="fc09b-120">However, this can change so you should not depend on this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc09b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc09b-121">Requirements</span></span>



| <span data-ttu-id="fc09b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc09b-122">Requirement</span></span> | <span data-ttu-id="fc09b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fc09b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc09b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc09b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fc09b-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc09b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc09b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc09b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fc09b-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc09b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc09b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc09b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc09b-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc09b-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc09b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc09b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc09b-131">**\_GETBUTTONSIZE PGM**</span><span class="sxs-lookup"><span data-stu-id="fc09b-131">**PGM\_GETBUTTONSIZE**</span></span>](pgm-getbuttonsize.md)
</dt> </dl>

 

 





