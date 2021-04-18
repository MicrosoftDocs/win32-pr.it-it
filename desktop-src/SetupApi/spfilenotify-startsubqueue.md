---
description: La \_ notifica SPFILENOTIFY STARTSUBQUEUE viene inviata alla funzione di callback quando la coda inizia a elaborare le operazioni nella coda secondaria Delete, Rename o Copy.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Messaggio SPFILENOTIFY_STARTSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318210"
---
# <a name="spfilenotify_startsubqueue-message"></a><span data-ttu-id="af2da-103">\_Messaggio SPFILENOTIFY STARTSUBQUEUE</span><span class="sxs-lookup"><span data-stu-id="af2da-103">SPFILENOTIFY\_STARTSUBQUEUE message</span></span>

<span data-ttu-id="af2da-104">La notifica **SPFILENOTIFY \_ STARTSUBQUEUE** viene inviata alla funzione di callback quando la coda inizia a elaborare le operazioni nella coda secondaria Delete, Rename o Copy.</span><span class="sxs-lookup"><span data-stu-id="af2da-104">The **SPFILENOTIFY\_STARTSUBQUEUE** notification is sent to the callback function when the queue starts to process the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a><span data-ttu-id="af2da-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="af2da-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af2da-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="af2da-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="af2da-107">Coda secondaria avviata.</span><span class="sxs-lookup"><span data-stu-id="af2da-107">Subqueue that has been started.</span></span> <span data-ttu-id="af2da-108">Questo parametro può essere uno dei valori FILEOP \_ Delete, FILEOP \_ Rename o FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="af2da-108">This parameter can be any one of the values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="af2da-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="af2da-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="af2da-110">Numero di operazioni di copia, ridenominazione o eliminazione di file nella coda secondaria.</span><span class="sxs-lookup"><span data-stu-id="af2da-110">Number of file copy, rename, or delete operations in the subqueue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af2da-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af2da-111">Return value</span></span>

<span data-ttu-id="af2da-112">Se si verifica un errore, la routine di callback deve chiamare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specificando l'errore e quindi restituire zero.</span><span class="sxs-lookup"><span data-stu-id="af2da-112">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="af2da-113">La funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituirà **false** e una chiamata successiva a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il codice di errore impostato dalla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="af2da-113">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="af2da-114">Se non si verificano errori, la routine di callback deve restituire un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="af2da-114">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="af2da-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af2da-115">Requirements</span></span>



| <span data-ttu-id="af2da-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af2da-116">Requirement</span></span> | <span data-ttu-id="af2da-117">Valore</span><span class="sxs-lookup"><span data-stu-id="af2da-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af2da-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af2da-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af2da-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="af2da-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="af2da-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af2da-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af2da-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af2da-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af2da-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af2da-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af2da-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="af2da-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af2da-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af2da-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af2da-125">Overview</span><span class="sxs-lookup"><span data-stu-id="af2da-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="af2da-126">Notifications</span><span class="sxs-lookup"><span data-stu-id="af2da-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="af2da-127">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="af2da-127">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="af2da-128">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="af2da-128">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

