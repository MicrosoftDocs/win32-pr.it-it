---
title: Messaggio PSM_SETFINISHTEXT (Prsht. h)
description: Imposta il testo del pulsante fine in una procedura guidata, Mostra e Abilita il pulsante e nasconde i pulsanti avanti e indietro. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- Controlli di Windows Message PSM_SETFINISHTEXT
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740098"
---
# <a name="psm_setfinishtext-message"></a><span data-ttu-id="2c3de-105">\_Messaggio SETFINISHTEXT di PSM</span><span class="sxs-lookup"><span data-stu-id="2c3de-105">PSM\_SETFINISHTEXT message</span></span>

<span data-ttu-id="2c3de-106">Imposta il testo del pulsante **fine** in una procedura guidata, Mostra e Abilita il pulsante e nasconde i pulsanti **Avanti** e **indietro** .</span><span class="sxs-lookup"><span data-stu-id="2c3de-106">Sets the text of the **Finish** button in a wizard, shows and enables the button, and hides the **Next** and **Back** buttons.</span></span> <span data-ttu-id="2c3de-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .</span><span class="sxs-lookup"><span data-stu-id="2c3de-107">You can send this message explicitly or by using the [**PropSheet\_SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c3de-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c3de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c3de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c3de-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c3de-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2c3de-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2c3de-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c3de-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c3de-112">Puntatore al nuovo testo per il pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="2c3de-112">Pointer to the new text for the **Finish** button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c3de-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c3de-113">Return value</span></span>

<span data-ttu-id="2c3de-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2c3de-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c3de-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c3de-115">Remarks</span></span>

<span data-ttu-id="2c3de-116">Per impostazione predefinita, il pulsante **fine** non dispone di un tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="2c3de-116">By default, the **Finish** button does not have a keyboard accelerator.</span></span> <span data-ttu-id="2c3de-117">È possibile creare un tasto di scelta rapida con questo messaggio includendo una e commerciale (&) nella stringa di testo assegnata a *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2c3de-117">You can create a keyboard accelerator with this message by including an ampersand (&) in the text string that you assign to *lParam*.</span></span> <span data-ttu-id="2c3de-118">Ad esempio, "&Finish" definisce F come tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="2c3de-118">For example, "&Finish" defines F as the accelerator key.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c3de-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c3de-119">Requirements</span></span>



| <span data-ttu-id="2c3de-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c3de-120">Requirement</span></span> | <span data-ttu-id="2c3de-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2c3de-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c3de-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c3de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2c3de-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c3de-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2c3de-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c3de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2c3de-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c3de-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2c3de-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c3de-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c3de-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c3de-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="2c3de-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2c3de-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2c3de-129">**PSM \_ SETFINISHTEXTW** (Unicode) e **PSM \_ SETFINISHTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2c3de-129">**PSM\_SETFINISHTEXTW** (Unicode) and **PSM\_SETFINISHTEXTA** (ANSI)</span></span><br/>    |



 

 





