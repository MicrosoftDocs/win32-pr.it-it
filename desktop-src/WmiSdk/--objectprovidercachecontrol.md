---
description: Controlla quando viene scaricato un provider di classi o istanze.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: Classe __ObjectProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317583"
---
# <a name="__objectprovidercachecontrol-class"></a><span data-ttu-id="1c490-103">\_\_Classe ObjectProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="1c490-103">\_\_ObjectProviderCacheControl class</span></span>

<span data-ttu-id="1c490-104">La classe di sistema **\_ \_ ObjectProviderCacheControl** controlla quando viene scaricato un provider di classi o istanze.</span><span class="sxs-lookup"><span data-stu-id="1c490-104">The **\_\_ObjectProviderCacheControl** system class controls when a class or instance provider is unloaded.</span></span> <span data-ttu-id="1c490-105">Si trova solo nello \\ spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="1c490-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="1c490-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1c490-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1c490-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1c490-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c490-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c490-108">Syntax</span></span>

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="1c490-109">Members</span><span class="sxs-lookup"><span data-stu-id="1c490-109">Members</span></span>

<span data-ttu-id="1c490-110">La classe **\_ \_ ObjectProviderCacheControl** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1c490-110">The **\_\_ObjectProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="1c490-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c490-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c490-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c490-112">Properties</span></span>

<span data-ttu-id="1c490-113">La classe **\_ \_ ObjectProviderCacheControl** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c490-113">The **\_\_ObjectProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c490-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="1c490-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c490-115">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c490-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c490-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1c490-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1c490-117">Intervallo di tempo dopo il quale WMI rilascia un'istanza, una classe o un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="1c490-117">Time interval after which WMI releases an instance, class, or method provider.</span></span> <span data-ttu-id="1c490-118">L'ora è in [Formato intervallo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="1c490-118">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c490-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c490-119">Remarks</span></span>

<span data-ttu-id="1c490-120">La classe **\_ \_ ObjectProviderCacheControl** deriva da [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="1c490-120">The **\_\_ObjectProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="1c490-121">Per ulteriori informazioni sull'utilizzo di questa classe, vedere [scaricamento di un provider](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1c490-121">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c490-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c490-122">Requirements</span></span>



| <span data-ttu-id="1c490-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c490-123">Requirement</span></span> | <span data-ttu-id="1c490-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1c490-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1c490-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c490-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1c490-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c490-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1c490-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c490-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1c490-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c490-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1c490-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c490-129">Namespace</span></span><br/>                | <span data-ttu-id="1c490-130">Radice</span><span class="sxs-lookup"><span data-stu-id="1c490-130">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1c490-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c490-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c490-132">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="1c490-132">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="1c490-133">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="1c490-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="1c490-134">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="1c490-134">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

