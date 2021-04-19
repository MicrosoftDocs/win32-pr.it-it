---
description: La \_ notifica SPFILENOTIFY QUEUESCAN viene inviata a una routine di callback da SetupScanFileQueue per ogni nodo nella coda secondaria di copia della coda di file. Questo errore si verifica solo se è stata chiamata la funzione SetupScanFileQueue specificando il flag SPQ \_ Scan \_ use \_ callback.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: Messaggio SPFILENOTIFY_QUEUESCAN (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316077"
---
# <a name="spfilenotify_queuescan-message"></a><span data-ttu-id="a60e3-104">\_Messaggio SPFILENOTIFY QUEUESCAN</span><span class="sxs-lookup"><span data-stu-id="a60e3-104">SPFILENOTIFY\_QUEUESCAN message</span></span>

<span data-ttu-id="a60e3-105">La notifica **SPFILENOTIFY \_ QUEUESCAN** viene inviata a una routine di callback da [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) per ogni nodo nella coda secondaria di copia della coda di file.</span><span class="sxs-lookup"><span data-stu-id="a60e3-105">The **SPFILENOTIFY\_QUEUESCAN** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="a60e3-106">Questo errore si verifica solo se è stata chiamata la funzione **SetupScanFileQueue** specificando il flag SPQ \_ Scan \_ use \_ callback.</span><span class="sxs-lookup"><span data-stu-id="a60e3-106">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a><span data-ttu-id="a60e3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a60e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a60e3-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="a60e3-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="a60e3-109">Stringa con terminazione null che specifica le informazioni sul percorso di destinazione per il file in coda nel nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="a60e3-109">Null-terminated string that specifies the target path information for the file queued in the current node.</span></span>

</dd> <dt>

<span data-ttu-id="a60e3-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="a60e3-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="a60e3-111">Se il file nel nodo corrente della coda è in uso, *param2* acquisisce il valore SPQ \_ Retarded \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="a60e3-111">If the file in the current node of the queue is in use, *Param2* takes the value SPQ\_DELAYED\_COPY.</span></span> <span data-ttu-id="a60e3-112">Se il file non è in uso, il valore è zero.</span><span class="sxs-lookup"><span data-stu-id="a60e3-112">If the file is not in use, the value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a60e3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a60e3-113">Return value</span></span>

<span data-ttu-id="a60e3-114">La routine di callback deve restituire un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a60e3-114">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="a60e3-115">Se la routine di callback non restituisce alcun \_ errore, l'analisi della coda continua.</span><span class="sxs-lookup"><span data-stu-id="a60e3-115">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="a60e3-116">Se la routine restituisce un altro codice di errore, l'analisi della coda viene interrotta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="a60e3-116">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="a60e3-117">Questa notifica non viene gestita dalla funzione [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="a60e3-117">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a60e3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a60e3-118">Requirements</span></span>



| <span data-ttu-id="a60e3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a60e3-119">Requirement</span></span> | <span data-ttu-id="a60e3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a60e3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a60e3-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a60e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a60e3-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a60e3-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a60e3-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a60e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a60e3-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a60e3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a60e3-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a60e3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a60e3-126"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a60e3-126"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a60e3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a60e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a60e3-128">Overview</span><span class="sxs-lookup"><span data-stu-id="a60e3-128">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="a60e3-129">Notifications</span><span class="sxs-lookup"><span data-stu-id="a60e3-129">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="a60e3-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="a60e3-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

