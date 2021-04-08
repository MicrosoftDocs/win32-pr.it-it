---
description: La \_ notifica SPFILENOTIFY QUEUESCAN \_ ex viene inviata a una routine di callback da SetupScanFileQueue per ogni nodo nella coda secondaria di copia della coda di file.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Messaggio SPFILENOTIFY_QUEUESCAN_EX (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880834"
---
# <a name="spfilenotify_queuescan_ex-message"></a><span data-ttu-id="ee100-103">\_Messaggio SPFILENOTIFY QUEUESCAN \_ ex</span><span class="sxs-lookup"><span data-stu-id="ee100-103">SPFILENOTIFY\_QUEUESCAN\_EX message</span></span>

<span data-ttu-id="ee100-104">La notifica **SPFILENOTIFY \_ QUEUESCAN \_ ex** viene inviata a una routine di callback da [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) per ogni nodo nella coda secondaria di copia della coda di file.</span><span class="sxs-lookup"><span data-stu-id="ee100-104">The **SPFILENOTIFY\_QUEUESCAN\_EX** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="ee100-105">Questo errore si verifica solo se è stata chiamata la funzione **SetupScanFileQueue** specificando il flag SPQ \_ Scan \_ use \_ CALLBACKEX.</span><span class="sxs-lookup"><span data-stu-id="ee100-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACKEX.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="ee100-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee100-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee100-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="ee100-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="ee100-108">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="ee100-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="ee100-109">Il membro di **destinazione** è il nome del file di destinazione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ee100-109">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="ee100-110">Il membro di **origine** è il percorso previsto del file di origine.</span><span class="sxs-lookup"><span data-stu-id="ee100-110">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="ee100-111">Il membro **Win32Error** è l'errore di firma.</span><span class="sxs-lookup"><span data-stu-id="ee100-111">The **Win32Error** member is the signing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee100-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee100-112">Return value</span></span>

<span data-ttu-id="ee100-113">La routine di callback deve restituire un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ee100-113">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="ee100-114">Se la routine di callback non restituisce alcun \_ errore, l'analisi della coda continua.</span><span class="sxs-lookup"><span data-stu-id="ee100-114">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="ee100-115">Se la routine restituisce un altro codice di errore, l'analisi della coda viene interrotta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) restituisce false.</span><span class="sxs-lookup"><span data-stu-id="ee100-115">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="ee100-116">Questa notifica non viene gestita dalla funzione [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="ee100-116">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee100-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee100-117">Requirements</span></span>



| <span data-ttu-id="ee100-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee100-118">Requirement</span></span> | <span data-ttu-id="ee100-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ee100-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee100-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee100-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ee100-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ee100-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ee100-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee100-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ee100-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee100-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee100-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee100-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee100-125"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee100-125"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee100-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee100-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee100-127">Overview</span><span class="sxs-lookup"><span data-stu-id="ee100-127">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="ee100-128">Notifications</span><span class="sxs-lookup"><span data-stu-id="ee100-128">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="ee100-129">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="ee100-129">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

