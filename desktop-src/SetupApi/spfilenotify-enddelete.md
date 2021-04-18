---
description: La \_ notifica ENDDELETE di SPFILENOTIFY viene restituita alla routine di callback quando una coda completa un'operazione di eliminazione. Questa notifica viene inviata anche se l'utente annulla o se si verifica un errore.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: Messaggio SPFILENOTIFY_ENDDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ee4762dc33f8b8ec16a6be273cb42f41aeafce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318619"
---
# <a name="spfilenotify_enddelete-message"></a><span data-ttu-id="8803f-104">\_Messaggio SPFILENOTIFY ENDDELETE</span><span class="sxs-lookup"><span data-stu-id="8803f-104">SPFILENOTIFY\_ENDDELETE message</span></span>

<span data-ttu-id="8803f-105">La **notifica \_ ENDDELETE di SPFILENOTIFY** viene restituita alla routine di callback quando una coda completa un'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="8803f-105">The **SPFILENOTIFY\_ENDDELETE** notification is returned to the callback routine when a queue completes a delete operation.</span></span> <span data-ttu-id="8803f-106">Questa notifica viene inviata anche se l'utente annulla o se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="8803f-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="8803f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8803f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8803f-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="8803f-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="8803f-109">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="8803f-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="8803f-110">Il membro **Win32Error** della struttura **filePaths** indica il risultato di un'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="8803f-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of a copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="8803f-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="8803f-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="8803f-112">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8803f-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8803f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8803f-113">Return value</span></span>

<span data-ttu-id="8803f-114">Il codice restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="8803f-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8803f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8803f-115">Requirements</span></span>



| <span data-ttu-id="8803f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8803f-116">Requirement</span></span> | <span data-ttu-id="8803f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8803f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8803f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8803f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8803f-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8803f-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8803f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8803f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8803f-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8803f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8803f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8803f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8803f-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8803f-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8803f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8803f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8803f-125">Overview</span><span class="sxs-lookup"><span data-stu-id="8803f-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="8803f-126">Notifications</span><span class="sxs-lookup"><span data-stu-id="8803f-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="8803f-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="8803f-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="8803f-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="8803f-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="8803f-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="8803f-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




