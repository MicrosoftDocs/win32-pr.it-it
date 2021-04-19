---
description: Determina quando WMI deve rilasciare un provider di consumer di eventi.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319324"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a><span data-ttu-id="d2017-103">\_\_Classe EventConsumerProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="d2017-103">\_\_EventConsumerProviderCacheControl class</span></span>

<span data-ttu-id="d2017-104">La classe di sistema **\_ \_ EventConsumerProviderCacheControl** determina quando WMI deve rilasciare un provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="d2017-104">The **\_\_EventConsumerProviderCacheControl** system class determines when WMI should release an event consumer provider.</span></span> <span data-ttu-id="d2017-105">La classe **\_ \_ EventConsumerProviderCacheControl** è una classe singleton.</span><span class="sxs-lookup"><span data-stu-id="d2017-105">The **\_\_EventConsumerProviderCacheControl** class is a singleton class.</span></span> <span data-ttu-id="d2017-106">Si trova solo nello \\ spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="d2017-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="d2017-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d2017-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d2017-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d2017-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2017-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2017-109">Syntax</span></span>

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="d2017-110">Members</span><span class="sxs-lookup"><span data-stu-id="d2017-110">Members</span></span>

<span data-ttu-id="d2017-111">La classe **\_ \_ EventConsumerProviderCacheControl** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d2017-111">The **\_\_EventConsumerProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="d2017-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2017-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2017-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2017-113">Properties</span></span>

<span data-ttu-id="d2017-114">La classe **\_ \_ EventConsumerProviderCacheControl** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2017-114">The **\_\_EventConsumerProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2017-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="d2017-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2017-116">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2017-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2017-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d2017-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d2017-118">Intervallo di tempo dopo il quale WMI rilascia un provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="d2017-118">Time interval after which WMI releases an event consumer provider.</span></span> <span data-ttu-id="d2017-119">L'intervallo specificato per lo scaricamento del provider potrebbe richiedere fino al doppio.</span><span class="sxs-lookup"><span data-stu-id="d2017-119">It may take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="d2017-120">L'ora è in [Formato intervallo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="d2017-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2017-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2017-121">Remarks</span></span>

<span data-ttu-id="d2017-122">La classe **\_ \_ EventConsumerProviderCacheControl** deriva da [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="d2017-122">The **\_\_EventConsumerProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="d2017-123">Per ulteriori informazioni sull'utilizzo di questa classe, vedere [scaricamento di un provider](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d2017-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2017-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2017-124">Requirements</span></span>



| <span data-ttu-id="d2017-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2017-125">Requirement</span></span> | <span data-ttu-id="d2017-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d2017-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d2017-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2017-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d2017-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2017-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d2017-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2017-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d2017-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2017-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d2017-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2017-131">Namespace</span></span><br/>                | <span data-ttu-id="d2017-132">Radice</span><span class="sxs-lookup"><span data-stu-id="d2017-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d2017-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2017-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2017-134">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d2017-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




