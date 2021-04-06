---
description: La \_ \_ struttura di monitoraggio info 2 identifica un monitoraggio.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Struttura MONITOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759656"
---
# <a name="monitor_info_2-structure"></a><span data-ttu-id="cf32e-103">Struttura di monitoraggio \_ info \_ 2</span><span class="sxs-lookup"><span data-stu-id="cf32e-103">MONITOR\_INFO\_2 structure</span></span>

<span data-ttu-id="cf32e-104">La struttura di **monitoraggio \_ info \_ 2** identifica un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="cf32e-104">The **MONITOR\_INFO\_2** structure identifies a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf32e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf32e-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="cf32e-106">Members</span><span class="sxs-lookup"><span data-stu-id="cf32e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cf32e-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="cf32e-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="cf32e-108">Puntatore a una stringa con terminazione null che rappresenta il nome del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="cf32e-108">A pointer to a null-terminated string that is the name of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="cf32e-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="cf32e-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="cf32e-110">Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il monitoraggio (ad esempio, Windows NT x86, Windows IA64, Windows x64).</span><span class="sxs-lookup"><span data-stu-id="cf32e-110">A pointer to a null-terminated string that specifies the environment for which the monitor was written (for example, Windows NT x86, Windows IA64, Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="cf32e-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="cf32e-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="cf32e-112">Puntatore a una stringa con terminazione null che rappresenta il nome della DLL di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="cf32e-112">A pointer to a null-terminated string that is the name of the monitor DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf32e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf32e-113">Requirements</span></span>



| <span data-ttu-id="cf32e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf32e-114">Requirement</span></span> | <span data-ttu-id="cf32e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="cf32e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf32e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf32e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cf32e-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf32e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cf32e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf32e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cf32e-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf32e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cf32e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf32e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf32e-121"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf32e-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cf32e-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="cf32e-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cf32e-123">**\_ Monitorare le \_ informazioni \_ 2W** (Unicode) e le **\_ informazioni di monitoraggio \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cf32e-123">**\_MONITOR\_INFO\_2W** (Unicode) and **\_MONITOR\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="cf32e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf32e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf32e-125">Stampa</span><span class="sxs-lookup"><span data-stu-id="cf32e-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cf32e-126">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="cf32e-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="cf32e-127">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="cf32e-127">**AddMonitor**</span></span>](addmonitor.md)
</dt> <dt>

[<span data-ttu-id="cf32e-128">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="cf32e-128">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="cf32e-129">**Informazioni di monitoraggio \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="cf32e-129">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> </dl>

 

 




