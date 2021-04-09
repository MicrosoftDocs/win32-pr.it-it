---
title: Messaggio CB_SETMINVISIBLE (COMmctrl. h)
description: Un'applicazione invia un \_ messaggio SETMINVISIBLE CB per impostare il numero minimo di elementi visibili nell'elenco a discesa di una casella combinata.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- Controlli di Windows Message CB_SETMINVISIBLE
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119091"
---
# <a name="cb_setminvisible-message"></a><span data-ttu-id="f5ffc-104">\_Messaggio SETMINVISIBLE CB</span><span class="sxs-lookup"><span data-stu-id="f5ffc-104">CB\_SETMINVISIBLE message</span></span>

<span data-ttu-id="f5ffc-105">Un'applicazione invia un **messaggio \_ SETMINVISIBLE CB** per impostare il numero minimo di elementi visibili nell'elenco a discesa di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="f5ffc-105">An application sends a **CB\_SETMINVISIBLE** message to set the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5ffc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5ffc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5ffc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5ffc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5ffc-108">Specifica il numero minimo di elementi visibili.</span><span class="sxs-lookup"><span data-stu-id="f5ffc-108">Specifies the minimum number of visible items.</span></span>

</dd> <dt>

<span data-ttu-id="f5ffc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5ffc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5ffc-110">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f5ffc-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5ffc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5ffc-111">Return value</span></span>

<span data-ttu-id="f5ffc-112">Se il messaggio ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="f5ffc-112">If the message is successful, the return value is **TRUE**.</span></span> <span data-ttu-id="f5ffc-113">In caso contrario, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="f5ffc-113">Otherwise the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5ffc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5ffc-114">Remarks</span></span>

<span data-ttu-id="f5ffc-115">Quando il numero di elementi nell'elenco a discesa è maggiore del valore minimo, la casella combinata utilizza una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="f5ffc-115">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span> <span data-ttu-id="f5ffc-116">Per impostazione predefinita, 30 è il numero minimo di elementi visibili.</span><span class="sxs-lookup"><span data-stu-id="f5ffc-116">By default, 30 is the minimum number of visible items.</span></span>

<span data-ttu-id="f5ffc-117">Questo messaggio viene ignorato se il controllo casella combinata ha lo stile [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f5ffc-117">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="f5ffc-118">Per usare **CB \_ SETMINVISIBLE**, l'applicazione deve specificare comctl32.dll versione 6 nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="f5ffc-118">To use **CB\_SETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="f5ffc-119">Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f5ffc-119">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ffc-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5ffc-120">Requirements</span></span>



| <span data-ttu-id="f5ffc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ffc-121">Requirement</span></span> | <span data-ttu-id="f5ffc-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f5ffc-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ffc-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5ffc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ffc-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5ffc-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5ffc-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5ffc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ffc-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5ffc-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5ffc-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5ffc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5ffc-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ffc-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ffc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5ffc-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5ffc-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f5ffc-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f5ffc-131">**CB \_ GETMINVISIBLE**</span><span class="sxs-lookup"><span data-stu-id="f5ffc-131">**CB\_GETMINVISIBLE**</span></span>](cb-getminvisible.md)
</dt> <dt>

[<span data-ttu-id="f5ffc-132">**\_SetMinVisible ComboBox**</span><span class="sxs-lookup"><span data-stu-id="f5ffc-132">**ComboBox\_SetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





