---
title: Messaggio TB_SETBUTTONWIDTH (COMmctrl. h)
description: Imposta le larghezze minime e massime del pulsante nel controllo Toolbar.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- Controlli di Windows Message TB_SETBUTTONWIDTH
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119823"
---
# <a name="tb_setbuttonwidth-message"></a><span data-ttu-id="73866-104">TB \_ SETBUTTONWIDTH messaggio</span><span class="sxs-lookup"><span data-stu-id="73866-104">TB\_SETBUTTONWIDTH message</span></span>

<span data-ttu-id="73866-105">Imposta le larghezze minime e massime del pulsante nel controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="73866-105">Sets the minimum and maximum button widths in the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="73866-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="73866-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73866-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73866-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73866-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="73866-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="73866-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73866-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73866-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la larghezza minima del pulsante in pixel.</span><span class="sxs-lookup"><span data-stu-id="73866-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum button width, in pixels.</span></span> <span data-ttu-id="73866-111">I pulsanti della barra degli strumenti non saranno mai più stretti di questo valore.</span><span class="sxs-lookup"><span data-stu-id="73866-111">Toolbar buttons will never be narrower than this value.</span></span>

<span data-ttu-id="73866-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la larghezza massima del pulsante, in pixel.</span><span class="sxs-lookup"><span data-stu-id="73866-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum button width, in pixels.</span></span> <span data-ttu-id="73866-113">Se il testo del pulsante è troppo ampio, il controllo lo Visualizza con puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="73866-113">If button text is too wide, the control displays it with ellipsis points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73866-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73866-114">Return value</span></span>

<span data-ttu-id="73866-115">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="73866-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="73866-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="73866-116">Remarks</span></span>

<span data-ttu-id="73866-117">Usare **TB \_ SETBUTTONWIDTH** per impostare le larghezze massime e minime consentite per i pulsanti prima di aggiungerli.</span><span class="sxs-lookup"><span data-stu-id="73866-117">Use **TB\_SETBUTTONWIDTH** to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="73866-118">Usare [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) per impostare le dimensioni effettive dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="73866-118">Use [**TB\_SETBUTTONSIZE**](tb-setbuttonsize.md) to set the actual size of buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="73866-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73866-119">Requirements</span></span>



| <span data-ttu-id="73866-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="73866-120">Requirement</span></span> | <span data-ttu-id="73866-121">Valore</span><span class="sxs-lookup"><span data-stu-id="73866-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73866-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73866-122">Minimum supported client</span></span><br/> | <span data-ttu-id="73866-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73866-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73866-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73866-124">Minimum supported server</span></span><br/> | <span data-ttu-id="73866-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73866-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73866-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73866-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="73866-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73866-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

