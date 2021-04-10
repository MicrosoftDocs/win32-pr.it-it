---
title: Messaggio TB_SETDRAWTEXTFLAGS (COMmctrl. h)
description: Imposta i flag di disegno del testo per la barra degli strumenti.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- Controlli di Windows Message TB_SETDRAWTEXTFLAGS
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964629"
---
# <a name="tb_setdrawtextflags-message"></a><span data-ttu-id="0949f-104">TB \_ SETDRAWTEXTFLAGS messaggio</span><span class="sxs-lookup"><span data-stu-id="0949f-104">TB\_SETDRAWTEXTFLAGS message</span></span>

<span data-ttu-id="0949f-105">Imposta i flag di disegno del testo per la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="0949f-105">Sets the text drawing flags for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0949f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0949f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0949f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0949f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0949f-108">Uno o più \_ flag DT, specificati in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), che indicano quali bit in *lParam* verranno utilizzati durante il disegno del testo.</span><span class="sxs-lookup"><span data-stu-id="0949f-108">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate which bits in *lParam* will be used when drawing the text.</span></span>

</dd> <dt>

<span data-ttu-id="0949f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0949f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0949f-110">Uno o più \_ flag DT, specificati in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), che indicano come verrà disegnato il testo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="0949f-110">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate how the button text will be drawn.</span></span> <span data-ttu-id="0949f-111">Questo valore verrà passato alla funzione **DrawText** quando viene disegnato il testo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="0949f-111">This value will be passed to the **DrawText** function when the button text is drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0949f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0949f-112">Return value</span></span>

<span data-ttu-id="0949f-113">Restituisce i flag di disegno del testo precedenti.</span><span class="sxs-lookup"><span data-stu-id="0949f-113">Returns the previous text drawing flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="0949f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0949f-114">Remarks</span></span>

<span data-ttu-id="0949f-115">Il parametro *wParam* consente di specificare i flag che verranno usati durante la creazione del testo, anche se questi flag sono disattivati.</span><span class="sxs-lookup"><span data-stu-id="0949f-115">The *wParam* parameter allows you to specify which flags will be used when drawing the text, even if these flags are turned off.</span></span> <span data-ttu-id="0949f-116">Se, ad esempio, non si desidera utilizzare il \_ flag DT Center durante il disegno del testo, è necessario aggiungere il \_ flag DT Center a *wParam* e non specificare il \_ flag DT Center in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="0949f-116">For example, if you do not want the DT\_CENTER flag used when drawing text, you would add the DT\_CENTER flag to *wParam* and not specify the DT\_CENTER flag in *lParam*.</span></span> <span data-ttu-id="0949f-117">In questo modo si impedisce al controllo di passare il \_ flag DT Center alla funzione [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="0949f-117">This prevents the control from passing the DT\_CENTER flag to the [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0949f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0949f-118">Requirements</span></span>



| <span data-ttu-id="0949f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0949f-119">Requirement</span></span> | <span data-ttu-id="0949f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0949f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0949f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0949f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0949f-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0949f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0949f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0949f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0949f-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0949f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0949f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0949f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0949f-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0949f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

