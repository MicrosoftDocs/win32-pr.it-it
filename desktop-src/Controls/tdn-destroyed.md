---
title: Codice di notifica TDN_DESTROYED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando viene eliminato definitivamente e il relativo handle di finestra non è più valido. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- Controlli di Windows per il codice di notifica TDN_DESTROYED
topic_type:
- apiref
api_name:
- TDN_DESTROYED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d3da93435371e696de3d4dce8deeea43926b73b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874562"
---
# <a name="tdn_destroyed-notification-code"></a><span data-ttu-id="04c66-105">TDN \_ codice di notifica distrutto</span><span class="sxs-lookup"><span data-stu-id="04c66-105">TDN\_DESTROYED notification code</span></span>

<span data-ttu-id="04c66-106">Inviato da una finestra di dialogo attività quando viene eliminato definitivamente e il relativo handle di finestra non è più valido.</span><span class="sxs-lookup"><span data-stu-id="04c66-106">Sent by a task dialog when it is destroyed and its window handle is no longer valid.</span></span> <span data-ttu-id="04c66-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="04c66-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DESTROYED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="04c66-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="04c66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04c66-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04c66-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04c66-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="04c66-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="04c66-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04c66-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04c66-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="04c66-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04c66-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04c66-113">Return value</span></span>

<span data-ttu-id="04c66-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="04c66-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="04c66-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04c66-115">Requirements</span></span>



| <span data-ttu-id="04c66-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="04c66-116">Requirement</span></span> | <span data-ttu-id="04c66-117">Valore</span><span class="sxs-lookup"><span data-stu-id="04c66-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04c66-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04c66-118">Minimum supported client</span></span><br/> | <span data-ttu-id="04c66-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04c66-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04c66-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04c66-120">Minimum supported server</span></span><br/> | <span data-ttu-id="04c66-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04c66-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04c66-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04c66-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="04c66-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="04c66-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





