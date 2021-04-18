---
description: Classe è la classe base astratta per le classi utilizzate per determinare quando WMI deve rilasciare un oggetto Component Object Model (COM).
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: Classe __CacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314097"
---
# <a name="__cachecontrol-class"></a><span data-ttu-id="71570-103">\_\_Classe CacheControl</span><span class="sxs-lookup"><span data-stu-id="71570-103">\_\_CacheControl class</span></span>

<span data-ttu-id="71570-104">La classe di sistema **\_ \_ CacheControl** è la classe di base astratta per le classi utilizzate per determinare quando WMI deve rilasciare un oggetto Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="71570-104">The **\_\_CacheControl** system class is the abstract base class for classes that are used to determine when WMI should release a Component Object Model (COM) object.</span></span> <span data-ttu-id="71570-105">Le istanze di questa classe non vengono mai create.</span><span class="sxs-lookup"><span data-stu-id="71570-105">Instances of this class are never created.</span></span> <span data-ttu-id="71570-106">La classe **\_ \_ CacheControl** si trova solo nello spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="71570-106">The **\_\_CacheControl** class is located only in the root namespace.</span></span> <span data-ttu-id="71570-107">Per ulteriori informazioni sull'utilizzo di questa classe, vedere [scaricamento di un provider](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="71570-107">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

<span data-ttu-id="71570-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="71570-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="71570-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="71570-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71570-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71570-110">Syntax</span></span>

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a><span data-ttu-id="71570-111">Members</span><span class="sxs-lookup"><span data-stu-id="71570-111">Members</span></span>

<span data-ttu-id="71570-112">La classe **\_ \_ CacheControl** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="71570-112">The **\_\_CacheControl** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="71570-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="71570-113">Remarks</span></span>

<span data-ttu-id="71570-114">La classe **\_ \_ CacheControl** deriva da [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="71570-114">The **\_\_CacheControl** class is derived from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71570-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71570-115">Requirements</span></span>



| <span data-ttu-id="71570-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="71570-116">Requirement</span></span> | <span data-ttu-id="71570-117">Valore</span><span class="sxs-lookup"><span data-stu-id="71570-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="71570-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71570-118">Minimum supported client</span></span><br/> | <span data-ttu-id="71570-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71570-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="71570-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71570-120">Minimum supported server</span></span><br/> | <span data-ttu-id="71570-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71570-121">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="71570-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="71570-122">Namespace</span></span><br/>                | <span data-ttu-id="71570-123">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="71570-123">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="71570-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71570-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71570-125">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="71570-125">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="71570-126">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="71570-126">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="71570-127">**\_\_EventConsumerProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="71570-127">**\_\_EventConsumerProviderCacheControl**</span></span>](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="71570-128">**\_\_EventProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="71570-128">**\_\_EventProviderCacheControl**</span></span>](--eventprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="71570-129">**\_\_EventSinkCacheControl**</span><span class="sxs-lookup"><span data-stu-id="71570-129">**\_\_EventSinkCacheControl**</span></span>](--eventsinkcachecontrol.md)
</dt> <dt>

[<span data-ttu-id="71570-130">**\_\_ObjectProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="71570-130">**\_\_ObjectProviderCacheControl**</span></span>](--objectprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="71570-131">\_\_PropertyProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="71570-131">\_\_PropertyProviderCacheControl</span></span>](--propertyprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="71570-132">Scaricamento di un provider</span><span class="sxs-lookup"><span data-stu-id="71570-132">Unloading a Provider</span></span>](unloading-a-provider.md)
</dt> </dl>

 

