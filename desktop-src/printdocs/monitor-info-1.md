---
description: La \_ \_ struttura di monitoraggio informazioni 1 identifica un monitoraggio installato.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: Struttura MONITOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6af1e1b9111ac6221273f2faf68fc6ed70e07a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311821"
---
# <a name="monitor_info_1-structure"></a><span data-ttu-id="071b8-103">Struttura di monitoraggio \_ informazioni \_ 1</span><span class="sxs-lookup"><span data-stu-id="071b8-103">MONITOR\_INFO\_1 structure</span></span>

<span data-ttu-id="071b8-104">La struttura di **monitoraggio \_ informazioni \_ 1** identifica un monitoraggio installato.</span><span class="sxs-lookup"><span data-stu-id="071b8-104">The **MONITOR\_INFO\_1** structure identifies an installed monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="071b8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="071b8-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="071b8-106">Members</span><span class="sxs-lookup"><span data-stu-id="071b8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="071b8-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="071b8-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="071b8-108">Puntatore a una stringa con terminazione null che identifica un monitoraggio installato.</span><span class="sxs-lookup"><span data-stu-id="071b8-108">A pointer to a null-terminated string that identifies an installed monitor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="071b8-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="071b8-109">Requirements</span></span>



| <span data-ttu-id="071b8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="071b8-110">Requirement</span></span> | <span data-ttu-id="071b8-111">Valore</span><span class="sxs-lookup"><span data-stu-id="071b8-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="071b8-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="071b8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="071b8-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="071b8-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="071b8-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="071b8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="071b8-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="071b8-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="071b8-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="071b8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="071b8-117"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="071b8-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="071b8-118">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="071b8-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="071b8-119">**\_ Informazioni di monitoraggio \_ \_ 1W** (Unicode) e **\_ monitoraggio \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="071b8-119">**\_MONITOR\_INFO\_1W** (Unicode) and **\_MONITOR\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="071b8-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="071b8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071b8-121">Stampa</span><span class="sxs-lookup"><span data-stu-id="071b8-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="071b8-122">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="071b8-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="071b8-123">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="071b8-123">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="071b8-124">**Informazioni sul monitoraggio \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="071b8-124">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

 




