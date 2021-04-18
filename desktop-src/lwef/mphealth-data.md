---
title: Struttura MPHEALTH_DATA (MpClient. h)
description: Dati di notifica dell'integrità.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- Struttura MPHEALTH_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPHEALTH_DATA
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302382"
---
# <a name="mphealth_data-structure"></a><span data-ttu-id="cc696-105">\_Struttura dei dati MPHEALTH</span><span class="sxs-lookup"><span data-stu-id="cc696-105">MPHEALTH\_DATA structure</span></span>

<span data-ttu-id="cc696-106">Dati di notifica dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="cc696-106">Health notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc696-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc696-107">Syntax</span></span>


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a><span data-ttu-id="cc696-108">Members</span><span class="sxs-lookup"><span data-stu-id="cc696-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc696-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="cc696-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="cc696-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cc696-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cc696-111">Tipo di notifica.</span><span class="sxs-lookup"><span data-stu-id="cc696-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="cc696-112">**dwNotificationFlag**</span><span class="sxs-lookup"><span data-stu-id="cc696-112">**dwNotificationFlag**</span></span>
</dt> <dd>

<span data-ttu-id="cc696-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cc696-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cc696-114">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cc696-114">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc696-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc696-115">Requirements</span></span>



| <span data-ttu-id="cc696-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc696-116">Requirement</span></span> | <span data-ttu-id="cc696-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cc696-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc696-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc696-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cc696-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cc696-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cc696-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc696-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cc696-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cc696-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc696-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc696-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc696-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc696-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





