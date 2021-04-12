---
description: La \_ struttura ADDJOB info \_ 1 identifica un processo di stampa, nonché la directory e il file in cui un'applicazione può archiviare il processo.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Struttura ADDJOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233732"
---
# <a name="addjob_info_1-structure"></a><span data-ttu-id="e2d67-103">\_Struttura ADDJOB info \_ 1</span><span class="sxs-lookup"><span data-stu-id="e2d67-103">ADDJOB\_INFO\_1 structure</span></span>

<span data-ttu-id="e2d67-104">La struttura **ADDJOB \_ info \_ 1** identifica un processo di stampa, nonché la directory e il file in cui un'applicazione può archiviare il processo.</span><span class="sxs-lookup"><span data-stu-id="e2d67-104">The **ADDJOB\_INFO\_1** structure identifies a print job as well as the directory and file in which an application can store that job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d67-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2d67-105">Syntax</span></span>


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="e2d67-106">Members</span><span class="sxs-lookup"><span data-stu-id="e2d67-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2d67-107">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="e2d67-107">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="e2d67-108">Puntatore a una stringa con terminazione null che contiene il percorso e il nome del file che l'applicazione può utilizzare per archiviare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="e2d67-108">Pointer to a null-terminated string that contains the path and file name that the application can use to store the print job.</span></span>

</dd> <dt>

<span data-ttu-id="e2d67-109">**JobId**</span><span class="sxs-lookup"><span data-stu-id="e2d67-109">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="e2d67-110">Handle per il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="e2d67-110">A handle to the print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2d67-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2d67-111">Requirements</span></span>



| <span data-ttu-id="e2d67-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d67-112">Requirement</span></span> | <span data-ttu-id="e2d67-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e2d67-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d67-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2d67-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d67-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e2d67-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e2d67-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2d67-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d67-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e2d67-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e2d67-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2d67-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2d67-119"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2d67-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e2d67-120">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e2d67-120">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e2d67-121">**\_ ADDJOB \_ info \_ 1W** (Unicode) e **\_ ADDJOB \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e2d67-121">**\_ADDJOB\_INFO\_1W** (Unicode) and **\_ADDJOB\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="e2d67-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2d67-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d67-123">Stampa</span><span class="sxs-lookup"><span data-stu-id="e2d67-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e2d67-124">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="e2d67-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e2d67-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="e2d67-125">**AddJob**</span></span>](addjob.md)
</dt> </dl>

 

 




