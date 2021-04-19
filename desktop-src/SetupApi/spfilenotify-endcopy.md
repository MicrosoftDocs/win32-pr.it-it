---
description: La \_ notifica SPFILENOTIFY ENDCOPY viene passata alla funzione di callback quando la coda completa un'operazione di copia. Questa notifica viene inviata anche se l'utente annulla o se si verifica un errore.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: Messaggio SPFILENOTIFY_ENDCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75dba56c4a38ac87003a3b59b594135e55a462f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319910"
---
# <a name="spfilenotify_endcopy-message"></a><span data-ttu-id="e07dc-104">\_Messaggio SPFILENOTIFY ENDCOPY</span><span class="sxs-lookup"><span data-stu-id="e07dc-104">SPFILENOTIFY\_ENDCOPY message</span></span>

<span data-ttu-id="e07dc-105">La notifica **SPFILENOTIFY \_ ENDCOPY** viene passata alla funzione di callback quando la coda completa un'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="e07dc-105">The **SPFILENOTIFY\_ENDCOPY** notification is passed to the callback function when the queue completes a copy operation.</span></span> <span data-ttu-id="e07dc-106">Questa notifica viene inviata anche se l'utente annulla o se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="e07dc-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="e07dc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e07dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07dc-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="e07dc-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="e07dc-109">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="e07dc-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="e07dc-110">Il membro **Win32Error** della struttura **filePaths** indica il risultato dell'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="e07dc-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="e07dc-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="e07dc-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="e07dc-112">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e07dc-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e07dc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e07dc-113">Return value</span></span>

<span data-ttu-id="e07dc-114">Il codice restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e07dc-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e07dc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e07dc-115">Requirements</span></span>



| <span data-ttu-id="e07dc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e07dc-116">Requirement</span></span> | <span data-ttu-id="e07dc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e07dc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e07dc-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e07dc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e07dc-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e07dc-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e07dc-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e07dc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e07dc-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e07dc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e07dc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e07dc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e07dc-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e07dc-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e07dc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e07dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07dc-125">Overview</span><span class="sxs-lookup"><span data-stu-id="e07dc-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="e07dc-126">Notifications</span><span class="sxs-lookup"><span data-stu-id="e07dc-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="e07dc-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="e07dc-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="e07dc-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="e07dc-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="e07dc-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="e07dc-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




