---
description: Utilizzato per determinare quando WMI rilascia un puntatore IWbemUnboundObjectSink per i provider di consumer di eventi.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: Classe __EventSinkCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317598"
---
# <a name="__eventsinkcachecontrol-class"></a><span data-ttu-id="3c12f-103">\_\_Classe EventSinkCacheControl</span><span class="sxs-lookup"><span data-stu-id="3c12f-103">\_\_EventSinkCacheControl class</span></span>

<span data-ttu-id="3c12f-104">La classe di sistema **\_ \_ EventSinkCacheControl** viene utilizzata per determinare quando WMI rilascia un puntatore [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) del provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="3c12f-104">The **\_\_EventSinkCacheControl** system class is used to determine when WMI releases an event consumer provider's [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) pointer.</span></span> <span data-ttu-id="3c12f-105">La classe **\_ \_ EventSinkCacheControl** è una classe singleton.</span><span class="sxs-lookup"><span data-stu-id="3c12f-105">The **\_\_EventSinkCacheControl** class is a singleton class.</span></span> <span data-ttu-id="3c12f-106">Si trova solo nello \\ spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="3c12f-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="3c12f-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3c12f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3c12f-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3c12f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c12f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c12f-109">Syntax</span></span>

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="3c12f-110">Members</span><span class="sxs-lookup"><span data-stu-id="3c12f-110">Members</span></span>

<span data-ttu-id="3c12f-111">La classe **\_ \_ EventSinkCacheControl** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3c12f-111">The **\_\_EventSinkCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="3c12f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3c12f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c12f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3c12f-113">Properties</span></span>

<span data-ttu-id="3c12f-114">La classe **\_ \_ EventSinkCacheControl** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3c12f-114">The **\_\_EventSinkCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c12f-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="3c12f-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c12f-116">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3c12f-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3c12f-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c12f-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3c12f-118">Intervallo di tempo dopo il quale WMI rilascia un provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="3c12f-118">Time interval after which WMI releases an event provider.</span></span> <span data-ttu-id="3c12f-119">L'intervallo specificato per scaricare il provider può richiedere fino a due volte.</span><span class="sxs-lookup"><span data-stu-id="3c12f-119">It can take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="3c12f-120">L'ora è in [Formato intervallo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="3c12f-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c12f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c12f-121">Remarks</span></span>

<span data-ttu-id="3c12f-122">La classe **\_ \_ EventSinkCacheControl** deriva da [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="3c12f-122">The **\_\_EventSinkCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="3c12f-123">Per ulteriori informazioni sull'utilizzo di questa classe, vedere [scaricamento di un provider](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3c12f-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c12f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c12f-124">Requirements</span></span>



| <span data-ttu-id="3c12f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c12f-125">Requirement</span></span> | <span data-ttu-id="3c12f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3c12f-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3c12f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c12f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3c12f-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c12f-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3c12f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c12f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3c12f-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c12f-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3c12f-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c12f-131">Namespace</span></span><br/>                | <span data-ttu-id="3c12f-132">Radice</span><span class="sxs-lookup"><span data-stu-id="3c12f-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3c12f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c12f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c12f-134">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="3c12f-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




