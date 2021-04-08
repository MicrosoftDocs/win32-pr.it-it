---
title: Codice di notifica TDN_CREATED (COMmctrl. h)
description: Inviato dalla finestra di dialogo attività dopo che la finestra di dialogo è stata creata e prima che venga visualizzata. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: cfe13db3-9c3c-425c-a6ef-17c5cb33eeb6
keywords:
- Controlli di Windows per il codice di notifica TDN_CREATED
topic_type:
- apiref
api_name:
- TDN_CREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25aa40af6b2cb002f2da7aab7c71fd68702ae65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964935"
---
# <a name="tdn_created-notification-code"></a><span data-ttu-id="6cdc5-105">\_Codice di notifica creato da TDN</span><span class="sxs-lookup"><span data-stu-id="6cdc5-105">TDN\_CREATED notification code</span></span>

<span data-ttu-id="6cdc5-106">Inviato dalla finestra di dialogo attività dopo che la finestra di dialogo è stata creata e prima che venga visualizzata.</span><span class="sxs-lookup"><span data-stu-id="6cdc5-106">Sent by the task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="6cdc5-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="6cdc5-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_CREATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="6cdc5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6cdc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cdc5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cdc5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cdc5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6cdc5-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6cdc5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cdc5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cdc5-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6cdc5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cdc5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6cdc5-113">Return value</span></span>

<span data-ttu-id="6cdc5-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="6cdc5-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cdc5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cdc5-115">Requirements</span></span>



| <span data-ttu-id="6cdc5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cdc5-116">Requirement</span></span> | <span data-ttu-id="6cdc5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6cdc5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdc5-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cdc5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6cdc5-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cdc5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cdc5-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cdc5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6cdc5-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6cdc5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cdc5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cdc5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cdc5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cdc5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





