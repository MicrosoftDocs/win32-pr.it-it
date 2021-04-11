---
description: Controlla quando viene scaricato un provider di eventi.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: Classe __EventProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232408"
---
# <a name="__eventprovidercachecontrol-class"></a><span data-ttu-id="ef643-103">\_\_Classe EventProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="ef643-103">\_\_EventProviderCacheControl class</span></span>

<span data-ttu-id="ef643-104">La classe di sistema **\_ \_ EventProviderCacheControl** controlla quando viene scaricato un provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="ef643-104">The **\_\_EventProviderCacheControl** system class controls when an event provider is unloaded.</span></span> <span data-ttu-id="ef643-105">Si trova solo nello \\ spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="ef643-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="ef643-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ef643-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ef643-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ef643-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef643-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef643-108">Syntax</span></span>

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="ef643-109">Members</span><span class="sxs-lookup"><span data-stu-id="ef643-109">Members</span></span>

<span data-ttu-id="ef643-110">La classe **\_ \_ EventProviderCacheControl** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ef643-110">The **\_\_EventProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="ef643-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef643-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef643-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef643-112">Properties</span></span>

<span data-ttu-id="ef643-113">La classe **\_ \_ EventProviderCacheControl** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ef643-113">The **\_\_EventProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef643-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="ef643-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef643-115">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef643-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef643-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ef643-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef643-117">L'intervallo di tempo dopo la Strumentazione gestione Windows (WMI) rilascia un provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="ef643-117">Time interval after Windows Management Instrumentation (WMI) releases an event provider.</span></span> <span data-ttu-id="ef643-118">L'ora è in [Formato intervallo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="ef643-118">The time is in [interval format](interval-format.md).</span></span> <span data-ttu-id="ef643-119">L'intervallo specificato per lo scaricamento del provider potrebbe richiedere fino al doppio.</span><span class="sxs-lookup"><span data-stu-id="ef643-119">It may take up to twice the interval specified to unload the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef643-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef643-120">Remarks</span></span>

<span data-ttu-id="ef643-121">La classe **\_ \_ EventProviderCacheControl** deriva da [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="ef643-121">The **\_\_EventProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span>

<span data-ttu-id="ef643-122">Per ulteriori informazioni sull'utilizzo di questa classe, vedere [scaricamento di un provider](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ef643-122">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef643-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef643-123">Requirements</span></span>



| <span data-ttu-id="ef643-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef643-124">Requirement</span></span> | <span data-ttu-id="ef643-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ef643-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ef643-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef643-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ef643-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef643-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ef643-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef643-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ef643-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef643-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ef643-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ef643-130">Namespace</span></span><br/>                | <span data-ttu-id="ef643-131">Radice</span><span class="sxs-lookup"><span data-stu-id="ef643-131">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ef643-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef643-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef643-133">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="ef643-133">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="ef643-134">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="ef643-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

