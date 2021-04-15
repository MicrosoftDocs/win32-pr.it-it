---
description: La \_ notifica SPFILENOTIFY STARTDELETE viene inviata alla funzione di callback quando la coda avvia un'operazione di eliminazione di file.
ms.assetid: 244714ad-dde7-4b5a-b3f3-78aa4cc901f5
title: Messaggio SPFILENOTIFY_STARTDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a4a0d362a1c1c3824154fb02e0bb9cf01b24d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529772"
---
# <a name="spfilenotify_startdelete-message"></a><span data-ttu-id="8bf99-103">\_Messaggio SPFILENOTIFY STARTDELETE</span><span class="sxs-lookup"><span data-stu-id="8bf99-103">SPFILENOTIFY\_STARTDELETE message</span></span>

<span data-ttu-id="8bf99-104">La notifica **SPFILENOTIFY \_ STARTDELETE** viene inviata alla funzione di callback quando la coda avvia un'operazione di eliminazione di file.</span><span class="sxs-lookup"><span data-stu-id="8bf99-104">The **SPFILENOTIFY\_STARTDELETE** notification is sent to the callback function when the queue starts a file delete operation.</span></span>


```C++
SPFILENOTIFY_STARTDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="8bf99-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bf99-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf99-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="8bf99-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf99-107">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="8bf99-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8bf99-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="8bf99-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf99-109">Il valore di FILEOP è sempre \_ Delete.</span><span class="sxs-lookup"><span data-stu-id="8bf99-109">Always has the value FILEOP\_DELETE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf99-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bf99-110">Return value</span></span>

<span data-ttu-id="8bf99-111">La routine di callback deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8bf99-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="8bf99-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8bf99-112">Return code</span></span>                                                                                  | <span data-ttu-id="8bf99-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bf99-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8bf99-114"><dt>**\_interruzione FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf99-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="8bf99-115">Interrompere il commit della coda.</span><span class="sxs-lookup"><span data-stu-id="8bf99-115">Abort the queue commit.</span></span> <span data-ttu-id="8bf99-116">La routine di callback deve chiamare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per indicare il motivo dell'interruzione.</span><span class="sxs-lookup"><span data-stu-id="8bf99-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for aborting.</span></span> <span data-ttu-id="8bf99-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce **false** e una chiamata successiva a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore impostato dalla routine di callback durante la chiamata a **SetLastError**.</span><span class="sxs-lookup"><span data-stu-id="8bf99-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="8bf99-118"><dt>**\_doit FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf99-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="8bf99-119">Eseguire l'operazione di copia del file.</span><span class="sxs-lookup"><span data-stu-id="8bf99-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="8bf99-120"><dt>**\_Ignora FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf99-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="8bf99-121">Ignora l'operazione di copia corrente.</span><span class="sxs-lookup"><span data-stu-id="8bf99-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="8bf99-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bf99-122">Requirements</span></span>



| <span data-ttu-id="8bf99-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf99-123">Requirement</span></span> | <span data-ttu-id="8bf99-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8bf99-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf99-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bf99-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf99-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8bf99-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8bf99-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bf99-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf99-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8bf99-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8bf99-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bf99-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf99-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf99-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf99-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bf99-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf99-132">Overview</span><span class="sxs-lookup"><span data-stu-id="8bf99-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="8bf99-133">Notifications</span><span class="sxs-lookup"><span data-stu-id="8bf99-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="8bf99-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="8bf99-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="8bf99-135">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="8bf99-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="8bf99-136">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="8bf99-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

