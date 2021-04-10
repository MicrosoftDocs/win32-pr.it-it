---
title: Codice di notifica TDN_HELP (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando l'utente preme F1 sulla tastiera mentre la finestra di dialogo ha lo stato attivo. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: 207ba231-639d-4906-b5dc-1592f2717f1c
keywords:
- Controlli di Windows per il codice di notifica TDN_HELP
topic_type:
- apiref
api_name:
- TDN_HELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d5e08342094aec5adc3da42621307d1577cd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121475"
---
# <a name="tdn_help-notification-code"></a><span data-ttu-id="3a682-105">\_Codice di notifica della Guida TDN</span><span class="sxs-lookup"><span data-stu-id="3a682-105">TDN\_HELP notification code</span></span>

<span data-ttu-id="3a682-106">Inviato da una finestra di dialogo attività quando l'utente preme F1 sulla tastiera mentre la finestra di dialogo ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="3a682-106">Sent by a task dialog when the user presses F1 on the keyboard while the dialog has focus.</span></span> <span data-ttu-id="3a682-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="3a682-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HELP
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="3a682-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a682-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a682-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a682-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a682-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a682-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3a682-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a682-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a682-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a682-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a682-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a682-113">Return value</span></span>

<span data-ttu-id="3a682-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3a682-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a682-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a682-115">Requirements</span></span>



| <span data-ttu-id="3a682-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a682-116">Requirement</span></span> | <span data-ttu-id="3a682-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3a682-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a682-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a682-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a682-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a682-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a682-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a682-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a682-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a682-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a682-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a682-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a682-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a682-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





