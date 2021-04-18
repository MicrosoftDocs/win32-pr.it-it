---
title: Codice di notifica TDN_TIMER (COMmctrl. h)
description: Inviato da una finestra di dialogo attività approssimativamente ogni 200 millisecondi.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- Controlli di Windows per il codice di notifica TDN_TIMER
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302636"
---
# <a name="tdn_timer-notification-code"></a><span data-ttu-id="0a13e-104">\_Codice di notifica del timer TDN</span><span class="sxs-lookup"><span data-stu-id="0a13e-104">TDN\_TIMER notification code</span></span>

<span data-ttu-id="0a13e-105">Inviato da una finestra di dialogo attività approssimativamente ogni 200 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0a13e-105">Sent by a task dialog approximately every 200 milliseconds.</span></span> <span data-ttu-id="0a13e-106">Questo codice di notifica viene inviato quando il \_ \_ flag del timer di callback TDF è stato impostato nel membro **DwFlags** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) che è stato passato alla funzione [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="0a13e-106">This notification code is sent when the TDF\_CALLBACK\_TIMER flag has been set in the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that was passed to the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="0a13e-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo **TaskDialogIndirect** .</span><span class="sxs-lookup"><span data-stu-id="0a13e-107">This notification code is received only through the task dialog callback function, which can be registered using the **TaskDialogIndirect** method.</span></span>


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0a13e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a13e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a13e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a13e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a13e-110">**DWORD** che specifica il numero di millisecondi trascorsi dal momento della creazione della finestra di dialogo oppure il codice di notifica ha restituito **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="0a13e-110">A **DWORD** that specifies the number of milliseconds since the dialog was created or this notification code returned **S\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0a13e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a13e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a13e-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0a13e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a13e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a13e-113">Return value</span></span>

<span data-ttu-id="0a13e-114">Per reimpostare il TickCount, l'applicazione deve restituire **S \_ false**, in caso contrario il TickCount continuerà ad aumentare.</span><span class="sxs-lookup"><span data-stu-id="0a13e-114">To reset the tickcount, the application must return **S\_FALSE**, otherwise the tickcount will continue to increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a13e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a13e-115">Requirements</span></span>



| <span data-ttu-id="0a13e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a13e-116">Requirement</span></span> | <span data-ttu-id="0a13e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0a13e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a13e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a13e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0a13e-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a13e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a13e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a13e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0a13e-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a13e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a13e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a13e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a13e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a13e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





