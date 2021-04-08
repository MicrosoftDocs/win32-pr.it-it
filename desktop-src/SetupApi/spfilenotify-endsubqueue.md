---
description: La \_ notifica SPFILENOTIFY ENDSUBQUEUE viene inviata alla funzione di callback quando la coda completa tutte le operazioni nella coda secondaria Delete, Rename o Copy.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: Messaggio SPFILENOTIFY_ENDSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058270"
---
# <a name="spfilenotify_endsubqueue-message"></a><span data-ttu-id="b66f0-103">\_Messaggio SPFILENOTIFY ENDSUBQUEUE</span><span class="sxs-lookup"><span data-stu-id="b66f0-103">SPFILENOTIFY\_ENDSUBQUEUE message</span></span>

<span data-ttu-id="b66f0-104">La notifica **SPFILENOTIFY \_ ENDSUBQUEUE** viene inviata alla funzione di callback quando la coda completa tutte le operazioni nella coda secondaria Delete, Rename o Copy.</span><span class="sxs-lookup"><span data-stu-id="b66f0-104">The **SPFILENOTIFY\_ENDSUBQUEUE** notification is sent to the callback function when the queue completes all the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="b66f0-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b66f0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b66f0-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="b66f0-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b66f0-107">Coda secondaria completata.</span><span class="sxs-lookup"><span data-stu-id="b66f0-107">Subqueue that has been completed.</span></span> <span data-ttu-id="b66f0-108">Questo parametro può essere uno dei seguenti valori FILEOP \_ Delete, FILEOP \_ Rename o FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="b66f0-108">This parameter can be one of the following values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="b66f0-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b66f0-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b66f0-110">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b66f0-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b66f0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b66f0-111">Return value</span></span>

<span data-ttu-id="b66f0-112">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b66f0-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b66f0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b66f0-113">Requirements</span></span>



| <span data-ttu-id="b66f0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b66f0-114">Requirement</span></span> | <span data-ttu-id="b66f0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b66f0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b66f0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b66f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b66f0-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b66f0-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b66f0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b66f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b66f0-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b66f0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b66f0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b66f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b66f0-121"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b66f0-121"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b66f0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b66f0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b66f0-123">Overview</span><span class="sxs-lookup"><span data-stu-id="b66f0-123">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b66f0-124">Notifications</span><span class="sxs-lookup"><span data-stu-id="b66f0-124">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b66f0-125">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="b66f0-125">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="b66f0-126">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="b66f0-126">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




