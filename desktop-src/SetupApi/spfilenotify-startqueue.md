---
description: La \_ notifica SPFILENOTIFY STARTQUEUE viene inviata alla routine di callback all'avvio del processo di impegno della coda.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: Messaggio SPFILENOTIFY_STARTQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090e3f97dceb1843d75934dd99cca500e6f93086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316075"
---
# <a name="spfilenotify_startqueue-message"></a><span data-ttu-id="47ed4-103">\_Messaggio SPFILENOTIFY STARTQUEUE</span><span class="sxs-lookup"><span data-stu-id="47ed4-103">SPFILENOTIFY\_STARTQUEUE message</span></span>

<span data-ttu-id="47ed4-104">La notifica **SPFILENOTIFY \_ STARTQUEUE** viene inviata alla routine di callback all'avvio del processo di impegno della coda.</span><span class="sxs-lookup"><span data-stu-id="47ed4-104">The **SPFILENOTIFY\_STARTQUEUE** notification is sent to the callback routine when the queue commitment process starts.</span></span>


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="47ed4-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="47ed4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47ed4-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="47ed4-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="47ed4-107">Handle per la finestra che deve essere proprietaria delle finestre di dialogo generate dalla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="47ed4-107">Handle to the window that is to own the dialog boxes that the callback routine generates.</span></span>

</dd> <dt>

<span data-ttu-id="47ed4-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="47ed4-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="47ed4-109">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="47ed4-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47ed4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47ed4-110">Return value</span></span>

<span data-ttu-id="47ed4-111">Se si verifica un errore, la routine di callback deve chiamare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specificando l'errore e quindi restituire zero.</span><span class="sxs-lookup"><span data-stu-id="47ed4-111">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="47ed4-112">La funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituirà **false** e una chiamata successiva a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il codice di errore impostato dalla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="47ed4-112">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="47ed4-113">Se non si verificano errori, la routine di callback deve restituire un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="47ed4-113">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="47ed4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47ed4-114">Requirements</span></span>



| <span data-ttu-id="47ed4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="47ed4-115">Requirement</span></span> | <span data-ttu-id="47ed4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="47ed4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47ed4-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47ed4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="47ed4-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="47ed4-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="47ed4-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47ed4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="47ed4-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="47ed4-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47ed4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47ed4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="47ed4-122"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="47ed4-122"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47ed4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47ed4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47ed4-124">Overview</span><span class="sxs-lookup"><span data-stu-id="47ed4-124">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="47ed4-125">Notifications</span><span class="sxs-lookup"><span data-stu-id="47ed4-125">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="47ed4-126">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="47ed4-126">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="47ed4-127">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="47ed4-127">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

