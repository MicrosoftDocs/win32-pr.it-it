---
description: "\\_Se si verifica un errore durante un'operazione di ridenominazione dei file, viene inviata la notifica SPFILENOTIFY RENAMEERROR alla routine di callback."
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: Messaggio SPFILENOTIFY_RENAMEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347246"
---
# <a name="spfilenotify_renameerror-message"></a><span data-ttu-id="56dd7-103">\_Messaggio SPFILENOTIFY RENAMEERROR</span><span class="sxs-lookup"><span data-stu-id="56dd7-103">SPFILENOTIFY\_RENAMEERROR message</span></span>

<span data-ttu-id="56dd7-104">Se si verifica un errore durante un'operazione di ridenominazione dei file, viene inviata la notifica **SPFILENOTIFY \_ RENAMEERROR** alla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="56dd7-104">The **SPFILENOTIFY\_RENAMEERROR** notification is sent to the callback routine if an error occurs during a file rename operation.</span></span>


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="56dd7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="56dd7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56dd7-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="56dd7-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="56dd7-107">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="56dd7-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="56dd7-108">Il membro **Win32Error** della struttura **filePaths** specifica l'errore che si è verificato durante l'operazione di ridenominazione.</span><span class="sxs-lookup"><span data-stu-id="56dd7-108">The **Win32Error** member of the **FILEPATHS** structure specifies the error that occurred during the rename operation.</span></span>

</dd> <dt>

<span data-ttu-id="56dd7-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="56dd7-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="56dd7-110">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="56dd7-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56dd7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56dd7-111">Return value</span></span>

<span data-ttu-id="56dd7-112">La routine di callback deve restituire uno dei seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="56dd7-112">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="56dd7-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="56dd7-113">Return code</span></span>                                                                                  | <span data-ttu-id="56dd7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56dd7-114">Description</span></span>                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56dd7-115"><dt>**FILEOP \_ nuovo tentativo**</dt></span><span class="sxs-lookup"><span data-stu-id="56dd7-115"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="56dd7-116">L'utente ha scelto di ritentare l'operazione di ridenominazione.</span><span class="sxs-lookup"><span data-stu-id="56dd7-116">The user chose to attempt the rename operation again.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="56dd7-117"><dt>**\_Ignora FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="56dd7-117"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="56dd7-118">L'utente ha scelto di ignorare l'operazione di ridenominazione dei file.</span><span class="sxs-lookup"><span data-stu-id="56dd7-118">The user chose to skip the file rename operation.</span></span><br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="56dd7-119"><dt>**\_interruzione FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="56dd7-119"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="56dd7-120">Arrestare il commit della coda.</span><span class="sxs-lookup"><span data-stu-id="56dd7-120">Stop the queue commit.</span></span> <span data-ttu-id="56dd7-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="56dd7-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE**.</span></span> <span data-ttu-id="56dd7-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce informazioni estese sull'errore, ad esempio errore \_ annullato (se l'utente è stato annullato) o errore \_ \_ memoria insufficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="56dd7-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="56dd7-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56dd7-123">Requirements</span></span>



| <span data-ttu-id="56dd7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="56dd7-124">Requirement</span></span> | <span data-ttu-id="56dd7-125">Valore</span><span class="sxs-lookup"><span data-stu-id="56dd7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56dd7-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56dd7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="56dd7-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="56dd7-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="56dd7-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56dd7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="56dd7-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56dd7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56dd7-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56dd7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="56dd7-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="56dd7-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56dd7-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56dd7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56dd7-133">Overview</span><span class="sxs-lookup"><span data-stu-id="56dd7-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="56dd7-134">Notifications</span><span class="sxs-lookup"><span data-stu-id="56dd7-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="56dd7-135">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="56dd7-135">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="56dd7-136">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="56dd7-136">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="56dd7-137">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="56dd7-137">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

