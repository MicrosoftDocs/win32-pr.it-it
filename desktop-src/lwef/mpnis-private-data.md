---
title: Struttura MPNIS_PRIVATE_DATA (MpClient. h)
description: Notifiche NIS private.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- Struttura MPNIS_PRIVATE_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPNIS_PRIVATE_DATA
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740138"
---
# <a name="mpnis_private_data-structure"></a><span data-ttu-id="c5bb6-105">\_Struttura di \_ dati privati MPNIS</span><span class="sxs-lookup"><span data-stu-id="c5bb6-105">MPNIS\_PRIVATE\_DATA structure</span></span>

<span data-ttu-id="c5bb6-106">Notifiche NIS private.</span><span class="sxs-lookup"><span data-stu-id="c5bb6-106">Private NIS notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5bb6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5bb6-107">Syntax</span></span>


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a><span data-ttu-id="c5bb6-108">Members</span><span class="sxs-lookup"><span data-stu-id="c5bb6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5bb6-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="c5bb6-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="c5bb6-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c5bb6-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c5bb6-111">Tipo di notifica.</span><span class="sxs-lookup"><span data-stu-id="c5bb6-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="c5bb6-112">**cbDataSize**</span><span class="sxs-lookup"><span data-stu-id="c5bb6-112">**cbDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="c5bb6-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c5bb6-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c5bb6-114">Dimensioni in byte dei dati riservati.</span><span class="sxs-lookup"><span data-stu-id="c5bb6-114">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c5bb6-115">**pbData**</span><span class="sxs-lookup"><span data-stu-id="c5bb6-115">**pbData**</span></span>
</dt> <dd>

<span data-ttu-id="c5bb6-116">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="c5bb6-116">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="c5bb6-117">Puntatore ai dati riservati.</span><span class="sxs-lookup"><span data-stu-id="c5bb6-117">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5bb6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5bb6-118">Requirements</span></span>



| <span data-ttu-id="c5bb6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5bb6-119">Requirement</span></span> | <span data-ttu-id="c5bb6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c5bb6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bb6-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5bb6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5bb6-122">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c5bb6-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c5bb6-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5bb6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c5bb6-124">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c5bb6-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5bb6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5bb6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5bb6-126"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5bb6-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





