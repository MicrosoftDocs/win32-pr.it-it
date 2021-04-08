---
description: "\\_Se si verifica un errore durante un'operazione di eliminazione di file, la notifica SPFILENOTIFY DELETEERROR viene inviata alla routine di callback."
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: Messaggio SPFILENOTIFY_DELETEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058272"
---
# <a name="spfilenotify_deleteerror-message"></a><span data-ttu-id="cd40b-103">\_Messaggio SPFILENOTIFY DELETEERROR</span><span class="sxs-lookup"><span data-stu-id="cd40b-103">SPFILENOTIFY\_DELETEERROR message</span></span>

<span data-ttu-id="cd40b-104">Se si verifica un errore durante un'operazione di eliminazione di file, la notifica **SPFILENOTIFY \_ DELETEERROR** viene inviata alla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="cd40b-104">The **SPFILENOTIFY\_DELETEERROR** notification is sent to the callback routine if an error occurs during a file delete operation.</span></span>


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="cd40b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd40b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd40b-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="cd40b-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="cd40b-107">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="cd40b-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd40b-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="cd40b-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="cd40b-109">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cd40b-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd40b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd40b-110">Return value</span></span>

<span data-ttu-id="cd40b-111">La routine di callback deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="cd40b-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="cd40b-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cd40b-112">Return code</span></span>                                                                                  | <span data-ttu-id="cd40b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd40b-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd40b-114"><dt>**\_interruzione FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="cd40b-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="cd40b-115">L'elaborazione della coda deve essere annullata.</span><span class="sxs-lookup"><span data-stu-id="cd40b-115">Queue processing should be canceled.</span></span> <span data-ttu-id="cd40b-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce informazioni estese sull'errore, ad esempio errore \_ annullato (se l'utente è stato annullato) o errore di \_ \_ memoria insufficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="cd40b-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="cd40b-117"><dt>**FILEOP \_ nuovo tentativo**</dt></span><span class="sxs-lookup"><span data-stu-id="cd40b-117"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="cd40b-118">L'utente sta tentando di eseguire di nuovo l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="cd40b-118">The user is attempting the delete operation again.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="cd40b-119"><dt>**\_Ignora FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="cd40b-119"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="cd40b-120">L'utente sta ignorando l'operazione di eliminazione del file.</span><span class="sxs-lookup"><span data-stu-id="cd40b-120">The user is skipping the file delete operation.</span></span><br/>                                                                                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="cd40b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd40b-121">Requirements</span></span>



| <span data-ttu-id="cd40b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd40b-122">Requirement</span></span> | <span data-ttu-id="cd40b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="cd40b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd40b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd40b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cd40b-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cd40b-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cd40b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd40b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cd40b-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd40b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd40b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd40b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd40b-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd40b-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd40b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd40b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd40b-131">Overview</span><span class="sxs-lookup"><span data-stu-id="cd40b-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="cd40b-132">Notifications</span><span class="sxs-lookup"><span data-stu-id="cd40b-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="cd40b-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="cd40b-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="cd40b-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="cd40b-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="cd40b-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="cd40b-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

