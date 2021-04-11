---
description: Rappresenta il contesto di esecuzione quando viene chiamato GetPrintExecutionData.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: Enumerazione PRINT_EXECUTION_CONTEXT (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20b1050edc0088fb629ee10cf63dc9cffa07228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227462"
---
# <a name="print_execution_context-enumeration"></a><span data-ttu-id="3b8bf-103">Enumerazione del contesto di \_ esecuzione di stampa \_</span><span class="sxs-lookup"><span data-stu-id="3b8bf-103">PRINT\_EXECUTION\_CONTEXT enumeration</span></span>

<span data-ttu-id="3b8bf-104">Rappresenta il contesto di esecuzione quando viene chiamato [**GetPrintExecutionData**](getprintexecutiondata.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8bf-104">Represents the execution context when [**GetPrintExecutionData**](getprintexecutiondata.md) is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8bf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b8bf-105">Syntax</span></span>


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="3b8bf-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="3b8bf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3b8bf-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**\_applicazione del \_ contesto di esecuzione di stampa \_**</span><span class="sxs-lookup"><span data-stu-id="3b8bf-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**PRINT\_EXECUTION\_CONTEXT\_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="3b8bf-108">Il chiamante è in esecuzione in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-108">The caller is running in an application.</span></span>

</dd> <dt>

<span data-ttu-id="3b8bf-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ servizio spooler del contesto di esecuzione di \_ stampa \_**</span><span class="sxs-lookup"><span data-stu-id="3b8bf-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="3b8bf-110">Il chiamante è in esecuzione nel servizio spooler (spoolsv.exe).</span><span class="sxs-lookup"><span data-stu-id="3b8bf-110">The caller is running in the spooler service (spoolsv.exe).</span></span>

</dd> <dt>

<span data-ttu-id="3b8bf-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_ \_ \_ \_ host isolamento spooler del contesto di esecuzione di stampa \_**</span><span class="sxs-lookup"><span data-stu-id="3b8bf-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_ISOLATION\_HOST**</span></span>
</dt> <dd>

<span data-ttu-id="3b8bf-112">Il chiamante è in esecuzione nell'host di isolamento stampa (PrintIsolationHost.exe)</span><span class="sxs-lookup"><span data-stu-id="3b8bf-112">The caller is running in the print isolation host (PrintIsolationHost.exe)</span></span>

</dd> <dt>

<span data-ttu-id="3b8bf-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**\_ \_ pipeline filtro del contesto di esecuzione di \_ stampa \_**</span><span class="sxs-lookup"><span data-stu-id="3b8bf-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**PRINT\_EXECUTION\_CONTEXT\_FILTER\_PIPELINE**</span></span>
</dt> <dd>

<span data-ttu-id="3b8bf-114">Il chiamante è in esecuzione nella pipeline del filtro di stampa (printfilterpipelinesvc.exe)</span><span class="sxs-lookup"><span data-stu-id="3b8bf-114">The caller is running in the print filter pipeline (printfilterpipelinesvc.exe)</span></span>

</dd> <dt>

<span data-ttu-id="3b8bf-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**\_WOW64 del \_ contesto di esecuzione di stampa \_**</span><span class="sxs-lookup"><span data-stu-id="3b8bf-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**PRINT\_EXECUTION\_CONTEXT\_WOW64**</span></span>
</dt> <dd>

<span data-ttu-id="3b8bf-116">Il chiamante è in esecuzione in splwow64.exe</span><span class="sxs-lookup"><span data-stu-id="3b8bf-116">The caller is running in splwow64.exe</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b8bf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b8bf-117">Requirements</span></span>



| <span data-ttu-id="3b8bf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b8bf-118">Requirement</span></span> | <span data-ttu-id="3b8bf-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3b8bf-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8bf-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b8bf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b8bf-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3b8bf-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="3b8bf-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b8bf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b8bf-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b8bf-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3b8bf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b8bf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b8bf-125"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b8bf-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8bf-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b8bf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8bf-127">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="3b8bf-127">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="3b8bf-128">**STAMPA \_ dati di esecuzione \_**</span><span class="sxs-lookup"><span data-stu-id="3b8bf-128">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

 




