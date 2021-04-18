---
description: La \_ notifica SPFILENOTIFY ENDRENAME viene inviata alla routine di callback quando la coda completa un'operazione di ridenominazione. Questa notifica viene inviata anche se l'utente annulla o se si verifica un errore.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: Messaggio SPFILENOTIFY_ENDRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a316d4dfe72ee9eb7d85fdb70eb90e1cf3d3f463
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318616"
---
# <a name="spfilenotify_endrename-message"></a><span data-ttu-id="1b965-104">\_Messaggio SPFILENOTIFY ENDRENAME</span><span class="sxs-lookup"><span data-stu-id="1b965-104">SPFILENOTIFY\_ENDRENAME message</span></span>

<span data-ttu-id="1b965-105">La notifica **SPFILENOTIFY \_ ENDRENAME** viene inviata alla routine di callback quando la coda completa un'operazione di ridenominazione.</span><span class="sxs-lookup"><span data-stu-id="1b965-105">The **SPFILENOTIFY\_ENDRENAME** notification is sent to the callback routine when the queue completes a rename operation.</span></span> <span data-ttu-id="1b965-106">Questa notifica viene inviata anche se l'utente annulla o se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="1b965-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="1b965-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b965-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b965-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="1b965-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="1b965-109">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="1b965-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="1b965-110">Il membro **Win32Error** della struttura **filePaths** indica il risultato dell'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="1b965-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="1b965-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="1b965-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="1b965-112">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1b965-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b965-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b965-113">Return value</span></span>

<span data-ttu-id="1b965-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="1b965-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b965-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b965-115">Requirements</span></span>



| <span data-ttu-id="1b965-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b965-116">Requirement</span></span> | <span data-ttu-id="1b965-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1b965-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b965-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b965-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b965-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1b965-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1b965-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b965-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b965-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b965-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b965-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b965-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b965-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b965-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b965-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b965-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b965-125">Overview</span><span class="sxs-lookup"><span data-stu-id="1b965-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="1b965-126">Notifications</span><span class="sxs-lookup"><span data-stu-id="1b965-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="1b965-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="1b965-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="1b965-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="1b965-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="1b965-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="1b965-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




