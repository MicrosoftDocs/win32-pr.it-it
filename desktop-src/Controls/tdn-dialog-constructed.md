---
title: Codice di notifica TDN_DIALOG_CONSTRUCTED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività dopo che la finestra di dialogo è stata creata e prima che venga visualizzata. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: e8556039-a74d-4e33-931d-a63ad5b2d4b0
keywords:
- Controlli di Windows per il codice di notifica TDN_DIALOG_CONSTRUCTED
topic_type:
- apiref
api_name:
- TDN_DIALOG_CONSTRUCTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d3360a8cee3542037ea927363de8cab69977e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964933"
---
# <a name="tdn_dialog_constructed-notification-code"></a><span data-ttu-id="4758f-105">\_Codice di \_ notifica creato dalla finestra di dialogo TDN</span><span class="sxs-lookup"><span data-stu-id="4758f-105">TDN\_DIALOG\_CONSTRUCTED notification code</span></span>

<span data-ttu-id="4758f-106">Inviato da una finestra di dialogo attività dopo che la finestra di dialogo è stata creata e prima che venga visualizzata.</span><span class="sxs-lookup"><span data-stu-id="4758f-106">Sent by a task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="4758f-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="4758f-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DIALOG_CONSTRUCTED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="4758f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4758f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4758f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4758f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4758f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4758f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4758f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4758f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4758f-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4758f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4758f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4758f-113">Return value</span></span>

<span data-ttu-id="4758f-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4758f-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4758f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4758f-115">Requirements</span></span>



| <span data-ttu-id="4758f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4758f-116">Requirement</span></span> | <span data-ttu-id="4758f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4758f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4758f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4758f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4758f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4758f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4758f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4758f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4758f-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4758f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4758f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4758f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4758f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4758f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





