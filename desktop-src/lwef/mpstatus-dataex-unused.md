---
title: Struttura MPSTATUS_DATAEX_UNUSED (MpClient. h)
description: Struttura fittizia per non-SRP.
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- Struttura MPSTATUS_DATAEX_UNUSED le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSTATUS_DATAEX_UNUSED
topic_type:
- apiref
api_name:
- MPSTATUS_DATAEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfcbc987a97a8cc47501a24e633c5da2d776a42d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121514"
---
# <a name="mpstatus_dataex_unused-structure"></a><span data-ttu-id="5b8a1-105">\_Struttura MPSTATUS DATAEX \_ inutilizzata</span><span class="sxs-lookup"><span data-stu-id="5b8a1-105">MPSTATUS\_DATAEX\_UNUSED structure</span></span>

<span data-ttu-id="5b8a1-106">Struttura fittizia per non-SRP.</span><span class="sxs-lookup"><span data-stu-id="5b8a1-106">Dummy structure for non-SRP.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b8a1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b8a1-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATAEX_UNUSED {
  DWORD dwNone;
} MPSTATUS_DATAEX_UNUSED, *PMPSTATUS_DATAEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="5b8a1-108">Members</span><span class="sxs-lookup"><span data-stu-id="5b8a1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b8a1-109">**dwNone**</span><span class="sxs-lookup"><span data-stu-id="5b8a1-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="5b8a1-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5b8a1-110">Type: **DWORD**</span></span>

<span data-ttu-id="5b8a1-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5b8a1-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5b8a1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b8a1-112">Requirements</span></span>



| <span data-ttu-id="5b8a1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b8a1-113">Requirement</span></span> | <span data-ttu-id="5b8a1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5b8a1-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b8a1-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b8a1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5b8a1-116">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5b8a1-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5b8a1-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b8a1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5b8a1-118">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5b8a1-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b8a1-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b8a1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b8a1-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b8a1-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





