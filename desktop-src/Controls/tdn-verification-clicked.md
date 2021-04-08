---
title: Codice di notifica TDN_VERIFICATION_CLICKED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando l'utente fa clic sulla casella di controllo Verifica finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- Controlli di Windows per il codice di notifica TDN_VERIFICATION_CLICKED
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7887a4d696f5294ebffc6fc6cc7183ff2c0aed8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964929"
---
# <a name="tdn_verification_clicked-notification-code"></a><span data-ttu-id="36cd5-105">TDN \_ verifica \_ clic sul codice di notifica</span><span class="sxs-lookup"><span data-stu-id="36cd5-105">TDN\_VERIFICATION\_CLICKED notification code</span></span>

<span data-ttu-id="36cd5-106">Inviato da una finestra di dialogo attività quando l'utente fa clic sulla casella di controllo Verifica finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="36cd5-106">Sent by a task dialog when the user clicks the task dialog verification check box.</span></span> <span data-ttu-id="36cd5-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="36cd5-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="36cd5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="36cd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36cd5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36cd5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36cd5-110">**Bool** che specifica lo stato della casella di controllo di verifica.</span><span class="sxs-lookup"><span data-stu-id="36cd5-110">A **BOOL** that specifies the status of the verification checkbox.</span></span> <span data-ttu-id="36cd5-111">È **true** se la casella di controllo verifica è selezionata oppure **false** se è deselezionata.</span><span class="sxs-lookup"><span data-stu-id="36cd5-111">It is **TRUE** if the verification checkbox is checked, or **FALSE** if it is unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="36cd5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36cd5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36cd5-113">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="36cd5-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36cd5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36cd5-114">Return value</span></span>

<span data-ttu-id="36cd5-115">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="36cd5-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="36cd5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36cd5-116">Requirements</span></span>



| <span data-ttu-id="36cd5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="36cd5-117">Requirement</span></span> | <span data-ttu-id="36cd5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="36cd5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36cd5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36cd5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36cd5-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36cd5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36cd5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36cd5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36cd5-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36cd5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36cd5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36cd5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36cd5-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36cd5-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cd5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36cd5-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="36cd5-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="36cd5-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="36cd5-127">*TaskDialogCallbackProc*</span><span class="sxs-lookup"><span data-stu-id="36cd5-127">*TaskDialogCallbackProc*</span></span>](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

