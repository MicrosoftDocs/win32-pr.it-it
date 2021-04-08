---
title: Codice di notifica TDN_RADIO_BUTTON_CLICKED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante di opzione o un collegamento al comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- Controlli di Windows per il codice di notifica TDN_RADIO_BUTTON_CLICKED
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c8b16f738e4807c94a060b41b3932d0f3e07ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964930"
---
# <a name="tdn_radio_button_clicked-notification-code"></a><span data-ttu-id="52a1f-105">\_Codice di \_ \_ notifica clic sul pulsante di opzione TDN</span><span class="sxs-lookup"><span data-stu-id="52a1f-105">TDN\_RADIO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="52a1f-106">Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante di opzione o un collegamento al comando nella finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="52a1f-106">Sent by a task dialog when the user selects a radio button or command link in the task dialog.</span></span> <span data-ttu-id="52a1f-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="52a1f-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="52a1f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="52a1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52a1f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52a1f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52a1f-110">Valore **int** che specifica l'ID corrispondente al pulsante di opzione su cui è stato fatto clic.</span><span class="sxs-lookup"><span data-stu-id="52a1f-110">An **int** that specifies the ID corresponding to the radio button that was clicked.</span></span>

</dd> <dt>

<span data-ttu-id="52a1f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52a1f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52a1f-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="52a1f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52a1f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52a1f-113">Return value</span></span>

<span data-ttu-id="52a1f-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="52a1f-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="52a1f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52a1f-115">Requirements</span></span>



| <span data-ttu-id="52a1f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a1f-116">Requirement</span></span> | <span data-ttu-id="52a1f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="52a1f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52a1f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52a1f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="52a1f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52a1f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52a1f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52a1f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="52a1f-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52a1f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52a1f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52a1f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="52a1f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52a1f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





