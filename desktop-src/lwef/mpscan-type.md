---
title: Enumerazione MPSCAN_TYPE (MpClient. h)
description: Tipo di analisi eseguita.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPSCAN_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPSCAN_TYPE
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb89137dc9cfe5b8a4ff1f44a7a101239aa3a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740135"
---
# <a name="mpscan_type-enumeration"></a><span data-ttu-id="c10bf-105">\_Enumerazione del tipo MPSCAN</span><span class="sxs-lookup"><span data-stu-id="c10bf-105">MPSCAN\_TYPE enumeration</span></span>

<span data-ttu-id="c10bf-106">Tipo di analisi eseguita.</span><span class="sxs-lookup"><span data-stu-id="c10bf-106">Type of scan performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c10bf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c10bf-107">Syntax</span></span>


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c10bf-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="c10bf-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c10bf-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**\_tipo MPSCAN \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="c10bf-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**MPSCAN\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="c10bf-110">Solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="c10bf-110">Internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="c10bf-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN \_ tipo \_ rapido**</span><span class="sxs-lookup"><span data-stu-id="c10bf-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN\_TYPE\_QUICK**</span></span>
</dt> <dd>

<span data-ttu-id="c10bf-112">Esegue l'analisi dei processi in esecuzione e di diversi punti di l'oggetto in cui il malware si nasconde in genere.</span><span class="sxs-lookup"><span data-stu-id="c10bf-112">Scans running processes and various ASEP points in the system where malware typically hides.</span></span>

</dd> <dt>

<span data-ttu-id="c10bf-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**tipo di MPSCAN \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="c10bf-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN\_TYPE\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="c10bf-114">Esegue un'analisi veloce seguita dall'analisi di tutte le unità fisse del sistema.</span><span class="sxs-lookup"><span data-stu-id="c10bf-114">Performs a quick scan followed by scan of all fixed drives of the system.</span></span>

</dd> <dt>

<span data-ttu-id="c10bf-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**\_risorsa di tipo MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="c10bf-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**MPSCAN\_TYPE\_RESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="c10bf-116">Analizza risorse specifiche, ad esempio file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="c10bf-116">Scans specific resources, such as files or folders.</span></span>

</dd> <dt>

<span data-ttu-id="c10bf-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN di \_ tipo \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="c10bf-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="c10bf-118">Valore massimo possibile.</span><span class="sxs-lookup"><span data-stu-id="c10bf-118">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c10bf-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c10bf-119">Requirements</span></span>



| <span data-ttu-id="c10bf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c10bf-120">Requirement</span></span> | <span data-ttu-id="c10bf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c10bf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c10bf-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c10bf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c10bf-123">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c10bf-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c10bf-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c10bf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c10bf-125">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c10bf-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c10bf-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c10bf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c10bf-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c10bf-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





