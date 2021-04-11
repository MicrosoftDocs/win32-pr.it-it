---
title: Messaggio EM_SETREADONLY (winuser. h)
description: Imposta o rimuove lo stile di sola lettura \_ di un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Controlli di Windows Message EM_SETREADONLY
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119659"
---
# <a name="em_setreadonly-message"></a><span data-ttu-id="01c19-105">Messaggio di sola \_ lettura em</span><span class="sxs-lookup"><span data-stu-id="01c19-105">EM\_SETREADONLY message</span></span>

<span data-ttu-id="01c19-106">Imposta o rimuove lo stile di sola lettura di [**un \_**](edit-control-styles.md)controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="01c19-106">Sets or removes the read-only style ([**ES\_READONLY**](edit-control-styles.md)) of an edit control.</span></span> <span data-ttu-id="01c19-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="01c19-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="01c19-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="01c19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01c19-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01c19-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01c19-110">Specifica se impostare o rimuovere lo stile di sola [**\_ lettura di es**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="01c19-110">Specifies whether to set or remove the [**ES\_READONLY**](edit-control-styles.md) style.</span></span> <span data-ttu-id="01c19-111">Il valore **true** imposta lo stile di sola **\_ lettura di es** . il valore **false** rimuove lo stile di sola **\_ lettura** .</span><span class="sxs-lookup"><span data-stu-id="01c19-111">A value of **TRUE** sets the **ES\_READONLY** style; a value of **FALSE** removes the **ES\_READONLY** style.</span></span>

</dd> <dt>

<span data-ttu-id="01c19-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01c19-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01c19-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="01c19-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01c19-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01c19-114">Return value</span></span>

<span data-ttu-id="01c19-115">Se l'operazione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="01c19-115">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="01c19-116">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="01c19-116">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="01c19-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="01c19-117">Remarks</span></span>

<span data-ttu-id="01c19-118">Quando un controllo di modifica ha lo stile di sola [**\_ lettura**](edit-control-styles.md) , l'utente non può modificare il testo nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="01c19-118">When an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, the user cannot change the text within the edit control.</span></span>

<span data-ttu-id="01c19-119">Per determinare se un controllo di modifica ha lo stile di sola [**\_ lettura di es**](edit-control-styles.md) , usare la funzione [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con il \_ flag di stile GWL.</span><span class="sxs-lookup"><span data-stu-id="01c19-119">To determine whether an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_STYLE flag.</span></span>

<span data-ttu-id="01c19-120">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="01c19-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="01c19-121">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="01c19-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01c19-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01c19-122">Requirements</span></span>



| <span data-ttu-id="01c19-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c19-123">Requirement</span></span> | <span data-ttu-id="01c19-124">Valore</span><span class="sxs-lookup"><span data-stu-id="01c19-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c19-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01c19-125">Minimum supported client</span></span><br/> | <span data-ttu-id="01c19-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01c19-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="01c19-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01c19-127">Minimum supported server</span></span><br/> | <span data-ttu-id="01c19-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01c19-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="01c19-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01c19-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c19-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01c19-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c19-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01c19-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c19-132">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="01c19-132">**GetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

