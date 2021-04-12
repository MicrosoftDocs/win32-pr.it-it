---
description: Controlla la cache quando viene scaricato un provider di proprietà.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: Classe __PropertyProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231828"
---
# <a name="__propertyprovidercachecontrol-class"></a><span data-ttu-id="e4fe8-103">\_\_Classe PropertyProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="e4fe8-103">\_\_PropertyProviderCacheControl class</span></span>

<span data-ttu-id="e4fe8-104">La classe **\_ \_ PropertyProviderCacheControl** controlla la cache quando viene scaricato un provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4fe8-104">The **\_\_PropertyProviderCacheControl** class controls the cache when a property provider is unloaded.</span></span> <span data-ttu-id="e4fe8-105">Questa classe esiste solo nello \\ spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="e4fe8-105">This class exists only in the \\root namespace.</span></span>

<span data-ttu-id="e4fe8-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e4fe8-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e4fe8-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e4fe8-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fe8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4fe8-108">Syntax</span></span>

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="e4fe8-109">Members</span><span class="sxs-lookup"><span data-stu-id="e4fe8-109">Members</span></span>

<span data-ttu-id="e4fe8-110">La classe **\_ \_ PropertyProviderCacheControl** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e4fe8-110">The **\_\_PropertyProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="e4fe8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4fe8-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4fe8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4fe8-112">Properties</span></span>

<span data-ttu-id="e4fe8-113">La classe **\_ \_ PropertyProviderCacheControl** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4fe8-113">The **\_\_PropertyProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4fe8-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="e4fe8-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fe8-115">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e4fe8-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e4fe8-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e4fe8-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4fe8-117">Intervallo di tempo dopo il rilascio di un provider di proprietà da WMI.</span><span class="sxs-lookup"><span data-stu-id="e4fe8-117">Time interval after WMI releases a property provider.</span></span> <span data-ttu-id="e4fe8-118">L'ora è nel formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="e4fe8-118">The time is in the interval format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4fe8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4fe8-119">Remarks</span></span>

<span data-ttu-id="e4fe8-120">La classe **\_ \_ PropertyProviderCacheControl** deriva da [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="e4fe8-120">The **\_\_PropertyProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="e4fe8-121">Per ulteriori informazioni, vedere [scaricamento di un provider](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e4fe8-121">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fe8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4fe8-122">Requirements</span></span>



| <span data-ttu-id="e4fe8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4fe8-123">Requirement</span></span> | <span data-ttu-id="e4fe8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e4fe8-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e4fe8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4fe8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e4fe8-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4fe8-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e4fe8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4fe8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e4fe8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4fe8-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e4fe8-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4fe8-129">Namespace</span></span><br/>                | <span data-ttu-id="e4fe8-130">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="e4fe8-130">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e4fe8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4fe8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fe8-132">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="e4fe8-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




