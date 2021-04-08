---
title: Codice di notifica TDN_BUTTON_CLICKED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante o un collegamento al comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- Controlli di Windows per il codice di notifica TDN_BUTTON_CLICKED
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964934"
---
# <a name="tdn_button_clicked-notification-code"></a><span data-ttu-id="b45a0-105">\_Codice di \_ notifica fatto clic sul pulsante TDN</span><span class="sxs-lookup"><span data-stu-id="b45a0-105">TDN\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="b45a0-106">Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante o un collegamento al comando nella finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="b45a0-106">Sent by a task dialog when the user selects a button or command link in the task dialog.</span></span> <span data-ttu-id="b45a0-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="b45a0-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b45a0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b45a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b45a0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b45a0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b45a0-110">Valore **int** che specifica l'ID del pulsante o del collegamento di Comand selezionato.</span><span class="sxs-lookup"><span data-stu-id="b45a0-110">An **int** that specifies the ID of the button or comand link that was selected.</span></span>

</dd> <dt>

<span data-ttu-id="b45a0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b45a0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b45a0-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b45a0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b45a0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b45a0-113">Return value</span></span>

<span data-ttu-id="b45a0-114">Per evitare la chiusura della finestra di dialogo attività, l'applicazione deve restituire **S \_ false**. in caso contrario, la finestra di dialogo attività viene chiusa e l'ID del pulsante viene restituito tramite la chiamata all'applicazione originale.</span><span class="sxs-lookup"><span data-stu-id="b45a0-114">To prevent the task dialog from closing, the application must return **S\_FALSE**, otherwise the task dialog is closed and the button ID is returned via the original application call.</span></span>

## <a name="requirements"></a><span data-ttu-id="b45a0-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b45a0-115">Requirements</span></span>



| <span data-ttu-id="b45a0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b45a0-116">Requirement</span></span> | <span data-ttu-id="b45a0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b45a0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b45a0-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b45a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b45a0-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b45a0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b45a0-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b45a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b45a0-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b45a0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b45a0-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b45a0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b45a0-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b45a0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





