---
title: Messaggio EM_SETEXTENDEDSTYLE (COMmctrl. h)
description: Informa il controllo di modifica per impostare gli stili estesi. Inviare questo messaggio o usare la macro Edit \_ SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- Controlli di Windows Message EM_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121031"
---
# <a name="em_setextendedstyle-message"></a><span data-ttu-id="7d8af-105">\_Messaggio SETEXTENDEDSTYLE em</span><span class="sxs-lookup"><span data-stu-id="7d8af-105">EM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="7d8af-106">Informa il controllo di modifica per impostare gli stili estesi.</span><span class="sxs-lookup"><span data-stu-id="7d8af-106">Informs the edit control to set extended styles.</span></span> <span data-ttu-id="7d8af-107">Inviare questo messaggio o usare la macro [**Edit \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="7d8af-107">Send this message or use the macro [**Edit\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="7d8af-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d8af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8af-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d8af-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d8af-110">Maschera utilizzata per selezionare gli stili da impostare.</span><span class="sxs-lookup"><span data-stu-id="7d8af-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="7d8af-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d8af-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d8af-112">Valore che indica lo stile esteso.</span><span class="sxs-lookup"><span data-stu-id="7d8af-112">Value that indicates the extended style.</span></span> <span data-ttu-id="7d8af-113">Per altre informazioni sugli stili, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="7d8af-113">For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8af-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d8af-114">Return value</span></span>

<span data-ttu-id="7d8af-115">Se il messaggio ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7d8af-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d8af-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7d8af-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d8af-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d8af-117">Remarks</span></span>

<span data-ttu-id="7d8af-118">Gli stili estesi per un controllo di modifica non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)funzione.</span><span class="sxs-lookup"><span data-stu-id="7d8af-118">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8af-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d8af-119">Requirements</span></span>



| <span data-ttu-id="7d8af-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d8af-120">Requirement</span></span> | <span data-ttu-id="7d8af-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7d8af-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8af-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d8af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7d8af-123">Solo app desktop Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d8af-123">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7d8af-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d8af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7d8af-125">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="7d8af-125">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d8af-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d8af-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d8af-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d8af-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

