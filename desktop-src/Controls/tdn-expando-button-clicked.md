---
title: Codice di notifica TDN_EXPANDO_BUTTON_CLICKED (COMmctrl. h)
description: Inviato dalla finestra di dialogo attività quando l'utente fa clic sul pulsante expando della finestra di dialogo. Questa notifica viene ricevuta solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- Controlli di Windows per il codice di notifica TDN_EXPANDO_BUTTON_CLICKED
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302638"
---
# <a name="tdn_expando_button_clicked-notification-code"></a><span data-ttu-id="610de-105">Il \_ pulsante TDN expando ha \_ \_ fatto clic sul codice di notifica</span><span class="sxs-lookup"><span data-stu-id="610de-105">TDN\_EXPANDO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="610de-106">Inviato dalla finestra di dialogo attività quando l'utente fa clic sul pulsante expando della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="610de-106">Sent by the task dialog when the user clicks on the dialog's expando button.</span></span> <span data-ttu-id="610de-107">Questa notifica viene ricevuta solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="610de-107">This notification is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="610de-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="610de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="610de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="610de-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="610de-110">**Bool** che è **true** se la finestra di dialogo è espansa o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="610de-110">A **BOOL** that is **TRUE** if the dialog is expanded, or **FALSE** if not.</span></span>

</dd> <dt>

<span data-ttu-id="610de-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="610de-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="610de-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="610de-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="610de-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="610de-113">Return value</span></span>

<span data-ttu-id="610de-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="610de-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="610de-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="610de-115">Remarks</span></span>

<span data-ttu-id="610de-116">Nell'esempio nella sezione Syntax viene illustrato il cast a wParam prima di inviare la notifica.</span><span class="sxs-lookup"><span data-stu-id="610de-116">The example in the Syntax section shows the cast to wParam before sending the notification.</span></span> <span data-ttu-id="610de-117">**LParam** non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="610de-117">**LPARAM** is not used and must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="610de-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="610de-118">Requirements</span></span>



| <span data-ttu-id="610de-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="610de-119">Requirement</span></span> | <span data-ttu-id="610de-120">Valore</span><span class="sxs-lookup"><span data-stu-id="610de-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="610de-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="610de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="610de-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="610de-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="610de-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="610de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="610de-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="610de-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="610de-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="610de-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="610de-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="610de-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





