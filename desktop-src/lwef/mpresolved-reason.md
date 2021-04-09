---
title: Enumerazione MPRESOLVED_REASON (MpClient. h)
description: Possibili motivi per la risoluzione di un errore di correzione.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPRESOLVED_REASON
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPRESOLVED_REASON
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048529"
---
# <a name="mpresolved_reason-enumeration"></a><span data-ttu-id="45fb5-105">\_Enumerazione MPRESOLVED Reason</span><span class="sxs-lookup"><span data-stu-id="45fb5-105">MPRESOLVED\_REASON enumeration</span></span>

<span data-ttu-id="45fb5-106">Possibili motivi per la risoluzione di un errore di correzione.</span><span class="sxs-lookup"><span data-stu-id="45fb5-106">Possible reasons for a remediation failure being resolved.</span></span>

## <a name="syntax"></a><span data-ttu-id="45fb5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45fb5-107">Syntax</span></span>


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a><span data-ttu-id="45fb5-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="45fb5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="45fb5-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MPRESOLVED \_ motivo \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="45fb5-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MPRESOLVED\_REASON\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="45fb5-110">In uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="45fb5-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="45fb5-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED \_ motivo \_ dell' \_ analisi completa**</span><span class="sxs-lookup"><span data-stu-id="45fb5-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED\_REASON\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="45fb5-112">È stata eseguita un'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="45fb5-112">A full scan was performed.</span></span>

</dd> <dt>

<span data-ttu-id="45fb5-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**\_timeout del motivo MPRESOLVED \_ \_**</span><span class="sxs-lookup"><span data-stu-id="45fb5-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**MPRESOLVED\_REASON\_TIMED\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="45fb5-114">Tempo sufficiente.</span><span class="sxs-lookup"><span data-stu-id="45fb5-114">Enough time has passed.</span></span> <span data-ttu-id="45fb5-115">Il valore predefinito è una settimana.</span><span class="sxs-lookup"><span data-stu-id="45fb5-115">The default is one week.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45fb5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45fb5-116">Requirements</span></span>



| <span data-ttu-id="45fb5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="45fb5-117">Requirement</span></span> | <span data-ttu-id="45fb5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="45fb5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45fb5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45fb5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="45fb5-120">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="45fb5-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="45fb5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45fb5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="45fb5-122">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="45fb5-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45fb5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45fb5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="45fb5-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="45fb5-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





