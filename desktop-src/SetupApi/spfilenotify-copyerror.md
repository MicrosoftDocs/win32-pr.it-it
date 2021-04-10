---
description: "\\_Quando si verifica un errore durante un'operazione di copia file, viene inviata la notifica SPFILENOTIFY COPYERROR alla routine di callback."
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: Messaggio SPFILENOTIFY_COPYERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882358"
---
# <a name="spfilenotify_copyerror-message"></a><span data-ttu-id="78721-103">\_Messaggio SPFILENOTIFY COPYERROR</span><span class="sxs-lookup"><span data-stu-id="78721-103">SPFILENOTIFY\_COPYERROR message</span></span>

<span data-ttu-id="78721-104">Quando si verifica un errore durante un'operazione di copia file, viene inviata la notifica **SPFILENOTIFY \_ COPYERROR** alla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="78721-104">The **SPFILENOTIFY\_COPYERROR** notification is sent to the callback routine if an error occurs during a file copy operation.</span></span>


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a><span data-ttu-id="78721-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="78721-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78721-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="78721-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="78721-107">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="78721-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="78721-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="78721-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="78721-109">Puntatore a un buffer, con dimensioni MASSIMe dei \_ caratteri di percorso, in cui sono archiviate le nuove informazioni sul percorso specificate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="78721-109">Pointer to a buffer, of size MAX\_PATH characters, that stores new path information specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78721-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78721-110">Return value</span></span>

<span data-ttu-id="78721-111">Il callback deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="78721-111">The callback should return one of the following values.</span></span>



| <span data-ttu-id="78721-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="78721-112">Return code</span></span>                                                                                    | <span data-ttu-id="78721-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78721-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78721-114"><dt>**\_interruzione FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="78721-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="78721-115">L'elaborazione della coda deve essere annullata.</span><span class="sxs-lookup"><span data-stu-id="78721-115">Queue processing should be canceled.</span></span> <span data-ttu-id="78721-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce informazioni estese sull'errore, ad esempio errore \_ annullato (se l'utente è stato annullato) o errore di \_ \_ memoria insufficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="78721-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="78721-117"><dt>**\_NEWPATH FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="78721-117"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="78721-118">Ripetere l'operazione di copia utilizzando il percorso della funzione di callback posizionata nel buffer a cui punta il parametro *param2* .</span><span class="sxs-lookup"><span data-stu-id="78721-118">Retry the copy operation using the path the callback function placed in the buffer pointed to by the *Param2* parameter.</span></span> <span data-ttu-id="78721-119">La routine di callback deve garantire che il percorso non superi le dimensioni del buffer di una matrice TCHAR di \_ elementi di percorso max.</span><span class="sxs-lookup"><span data-stu-id="78721-119">The callback routine should ensure that the path does not overflow the buffer size of a TCHAR array of MAX\_PATH elements.</span></span><br/>                |
| <dl> <span data-ttu-id="78721-120"><dt>**FILEOP \_ nuovo tentativo**</dt></span><span class="sxs-lookup"><span data-stu-id="78721-120"><dt>**FILEOP\_RETRY**</dt></span></span> </dl>   | <span data-ttu-id="78721-121">L'utente sta tentando di eseguire di nuovo l'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="78721-121">The user is attempting the copy operation again.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="78721-122"><dt>**\_Ignora FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="78721-122"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="78721-123">L'utente sta ignorando l'operazione di copia del file.</span><span class="sxs-lookup"><span data-stu-id="78721-123">The user is skipping the file copy operation.</span></span><br/>                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="78721-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78721-124">Requirements</span></span>



| <span data-ttu-id="78721-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="78721-125">Requirement</span></span> | <span data-ttu-id="78721-126">Valore</span><span class="sxs-lookup"><span data-stu-id="78721-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78721-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78721-127">Minimum supported client</span></span><br/> | <span data-ttu-id="78721-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="78721-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="78721-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78721-129">Minimum supported server</span></span><br/> | <span data-ttu-id="78721-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78721-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78721-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78721-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="78721-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="78721-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78721-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78721-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78721-134">Overview</span><span class="sxs-lookup"><span data-stu-id="78721-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="78721-135">Notifications</span><span class="sxs-lookup"><span data-stu-id="78721-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="78721-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="78721-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="78721-137">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="78721-137">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="78721-138">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="78721-138">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

