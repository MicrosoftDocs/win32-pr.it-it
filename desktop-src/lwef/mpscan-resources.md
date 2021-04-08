---
title: Struttura MPSCAN_RESOURCES (MpClient. h)
description: Informazioni sulle risorse passate durante un'operazione di analisi.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- Struttura MPSCAN_RESOURCES le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSCAN_RESOURCES
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964947"
---
# <a name="mpscan_resources-structure"></a><span data-ttu-id="fec29-105">\_Struttura delle risorse di MPSCAN</span><span class="sxs-lookup"><span data-stu-id="fec29-105">MPSCAN\_RESOURCES structure</span></span>

<span data-ttu-id="fec29-106">Informazioni sulle risorse passate durante un'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="fec29-106">Resource information passed during a scan operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec29-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fec29-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a><span data-ttu-id="fec29-108">Members</span><span class="sxs-lookup"><span data-stu-id="fec29-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fec29-109">**dwResourceCount**</span><span class="sxs-lookup"><span data-stu-id="fec29-109">**dwResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="fec29-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="fec29-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="fec29-111">Numero di risorse.</span><span class="sxs-lookup"><span data-stu-id="fec29-111">Count of resources.</span></span>

</dd> <dt>

<span data-ttu-id="fec29-112">**origine dati**</span><span class="sxs-lookup"><span data-stu-id="fec29-112">**pResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="fec29-113">Tipo: **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="fec29-113">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="fec29-114">Matrice di risorse.</span><span class="sxs-lookup"><span data-stu-id="fec29-114">Array of resources.</span></span> <span data-ttu-id="fec29-115">Vedere [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="fec29-115">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fec29-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fec29-116">Requirements</span></span>



| <span data-ttu-id="fec29-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec29-117">Requirement</span></span> | <span data-ttu-id="fec29-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fec29-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fec29-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fec29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fec29-120">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fec29-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fec29-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fec29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fec29-122">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fec29-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fec29-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fec29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fec29-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fec29-124"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec29-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fec29-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec29-126">**\_informazioni MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="fec29-126">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





