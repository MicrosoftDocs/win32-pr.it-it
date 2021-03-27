---
description: Questa classe è la classe padre per gli eventi di configurazione hardware. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 9da1a7ec-89b5-462b-a336-544e4b7adf96
title: Classe SystemConfig_V0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0
api_type:
- NA
api_location: ''
ms.openlocfilehash: 92d77d1ad3effdd2bf22a7df8112187b27666238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880894"
---
# <a name="systemconfig_v0-class"></a><span data-ttu-id="cc8b3-104">\_Classe SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="cc8b3-104">SystemConfig\_V0 class</span></span>

<span data-ttu-id="cc8b3-105">Questa classe è la classe padre per gli eventi di configurazione hardware.</span><span class="sxs-lookup"><span data-stu-id="cc8b3-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="cc8b3-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="cc8b3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc8b3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc8b3-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="cc8b3-108">Members</span><span class="sxs-lookup"><span data-stu-id="cc8b3-108">Members</span></span>

<span data-ttu-id="cc8b3-109">La classe **SystemConfig \_ V0** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="cc8b3-109">The **SystemConfig\_V0** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc8b3-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc8b3-110">Remarks</span></span>

<span data-ttu-id="cc8b3-111">Per gli eventi di configurazione hardware in Windows XP, vedere la classe [**HWConfig**](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="cc8b3-111">For hardware configuration events on Windows XP, see the [**HWConfig**](hwconfig.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc8b3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc8b3-112">Requirements</span></span>



| <span data-ttu-id="cc8b3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc8b3-113">Requirement</span></span> | <span data-ttu-id="cc8b3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cc8b3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc8b3-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc8b3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cc8b3-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cc8b3-116">None supported</span></span><br/>                            |
| <span data-ttu-id="cc8b3-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc8b3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cc8b3-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cc8b3-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc8b3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc8b3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc8b3-120">**\_SYSTEMTRACE MSNT**</span><span class="sxs-lookup"><span data-stu-id="cc8b3-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="cc8b3-121">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="cc8b3-121">**SystemConfig**</span></span>](systemconfig.md)
</dt> <dt>

[<span data-ttu-id="cc8b3-122">**\_CPU SystemConfig V0 \_**</span><span class="sxs-lookup"><span data-stu-id="cc8b3-122">**SystemConfig\_V0\_CPU**</span></span>](systemconfig-v0-cpu.md)
</dt> <dt>

[<span data-ttu-id="cc8b3-123">**SystemConfig \_ V0 \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="cc8b3-123">**SystemConfig\_V0\_LogDisk**</span></span>](systemconfig-v0-logdisk.md)
</dt> <dt>

[<span data-ttu-id="cc8b3-124">**Scheda di interfaccia di rete SystemConfig \_ V0 \_**</span><span class="sxs-lookup"><span data-stu-id="cc8b3-124">**SystemConfig\_V0\_NIC**</span></span>](systemconfig-v0-nic.md)
</dt> <dt>

[<span data-ttu-id="cc8b3-125">**SystemConfig \_ V0 \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="cc8b3-125">**SystemConfig\_V0\_PhyDisk**</span></span>](systemconfig-v0-phydisk.md)
</dt> <dt>

[<span data-ttu-id="cc8b3-126">**\_Potenza SystemConfig V0 \_**</span><span class="sxs-lookup"><span data-stu-id="cc8b3-126">**SystemConfig\_V0\_Power**</span></span>](systemconfig-v0-power.md)
</dt> <dt>

[<span data-ttu-id="cc8b3-127">**\_Servizi SystemConfig V0 \_**</span><span class="sxs-lookup"><span data-stu-id="cc8b3-127">**SystemConfig\_V0\_Services**</span></span>](systemconfig-v0-services.md)
</dt> <dt>

[<span data-ttu-id="cc8b3-128">**\_Video SystemConfig V0 \_**</span><span class="sxs-lookup"><span data-stu-id="cc8b3-128">**SystemConfig\_V0\_Video**</span></span>](systemconfig-v0-video.md)
</dt> </dl>

 

 




