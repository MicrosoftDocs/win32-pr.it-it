---
title: Messaggio CB_GETMINVISIBLE (COMmctrl. h)
description: Ottiene il numero minimo di elementi visibili nell'elenco a discesa di una casella combinata.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- Controlli di Windows Message CB_GETMINVISIBLE
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873794"
---
# <a name="cb_getminvisible-message"></a><span data-ttu-id="375e9-104">\_Messaggio GETMINVISIBLE CB</span><span class="sxs-lookup"><span data-stu-id="375e9-104">CB\_GETMINVISIBLE message</span></span>

<span data-ttu-id="375e9-105">Ottiene il numero minimo di elementi visibili nell'elenco a discesa di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="375e9-105">Gets the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="375e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="375e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="375e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="375e9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="375e9-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="375e9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="375e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="375e9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="375e9-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="375e9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="375e9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="375e9-111">Return value</span></span>

<span data-ttu-id="375e9-112">Il valore restituito è il numero minimo di elementi visibili.</span><span class="sxs-lookup"><span data-stu-id="375e9-112">The return value is the minimum number of visible items.</span></span>

## <a name="remarks"></a><span data-ttu-id="375e9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="375e9-113">Remarks</span></span>

<span data-ttu-id="375e9-114">Quando il numero di elementi nell'elenco a discesa è maggiore del valore minimo, la casella combinata utilizza una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="375e9-114">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span>

<span data-ttu-id="375e9-115">Questo messaggio viene ignorato se il controllo casella combinata ha lo stile [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="375e9-115">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="375e9-116">Per usare **CB \_ GETMINVISIBLE**, l'applicazione deve specificare comctl32.dll versione 6 nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="375e9-116">To use **CB\_GETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="375e9-117">Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="375e9-117">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="375e9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="375e9-118">Requirements</span></span>



| <span data-ttu-id="375e9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="375e9-119">Requirement</span></span> | <span data-ttu-id="375e9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="375e9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="375e9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="375e9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="375e9-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="375e9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="375e9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="375e9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="375e9-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="375e9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="375e9-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="375e9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="375e9-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="375e9-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="375e9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="375e9-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="375e9-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="375e9-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="375e9-129">**CB \_ SETMINVISIBLE**</span><span class="sxs-lookup"><span data-stu-id="375e9-129">**CB\_SETMINVISIBLE**</span></span>](cb-setminvisible.md)
</dt> <dt>

[<span data-ttu-id="375e9-130">**\_GetMinVisible ComboBox**</span><span class="sxs-lookup"><span data-stu-id="375e9-130">**ComboBox\_GetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





