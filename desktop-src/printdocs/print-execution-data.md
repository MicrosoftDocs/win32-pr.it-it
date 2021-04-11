---
description: Contiene il contesto di esecuzione del driver della stampante che chiama GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: Struttura PRINT_EXECUTION_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232895"
---
# <a name="print_execution_data-structure"></a><span data-ttu-id="536df-103">\_ \_ Struttura dei dati di esecuzione di stampa</span><span class="sxs-lookup"><span data-stu-id="536df-103">PRINT\_EXECUTION\_DATA structure</span></span>

<span data-ttu-id="536df-104">Contiene il contesto di esecuzione del driver della stampante che chiama [**GetPrintExecutionData**](getprintexecutiondata.md).</span><span class="sxs-lookup"><span data-stu-id="536df-104">Contains the execution context of the printer driver that calls [**GetPrintExecutionData**](getprintexecutiondata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="536df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="536df-105">Syntax</span></span>


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a><span data-ttu-id="536df-106">Members</span><span class="sxs-lookup"><span data-stu-id="536df-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="536df-107">**context**</span><span class="sxs-lookup"><span data-stu-id="536df-107">**context**</span></span>
</dt> <dd>

<span data-ttu-id="536df-108">Valore [**del \_ \_ contesto di esecuzione di stampa**](print-execution-context.md) che rappresenta il contesto di esecuzione corrente del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="536df-108">The [**PRINT\_EXECUTION\_CONTEXT**](print-execution-context.md) value that represents the current execution context of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="536df-109">**clientAppPID**</span><span class="sxs-lookup"><span data-stu-id="536df-109">**clientAppPID**</span></span>
</dt> <dd>

<span data-ttu-id="536df-110">Se il valore di **context** è **il \_ contesto di esecuzione di stampa \_ \_ WOW64**, **clientAppPID** identifica l'applicazione client per conto del quale il splwow64.exe processo ha caricato il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="536df-110">If the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** identifies the client application on whose behalf the splwow64.exe process loaded the printer driver.</span></span> <span data-ttu-id="536df-111">Se il valore di **context** non è **il \_ contesto di esecuzione di stampa \_ \_ WOW64**, **clientAppPID** è zero.</span><span class="sxs-lookup"><span data-stu-id="536df-111">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** is zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="536df-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="536df-112">Requirements</span></span>



| <span data-ttu-id="536df-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="536df-113">Requirement</span></span> | <span data-ttu-id="536df-114">Valore</span><span class="sxs-lookup"><span data-stu-id="536df-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536df-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="536df-115">Minimum supported client</span></span><br/> | <span data-ttu-id="536df-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="536df-116">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="536df-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="536df-117">Minimum supported server</span></span><br/> | <span data-ttu-id="536df-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="536df-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="536df-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="536df-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="536df-120"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="536df-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="536df-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="536df-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="536df-122">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="536df-122">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="536df-123">**\_contesto di esecuzione di stampa \_**</span><span class="sxs-lookup"><span data-stu-id="536df-123">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> </dl>

 

 




