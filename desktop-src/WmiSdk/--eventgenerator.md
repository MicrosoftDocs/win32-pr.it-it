---
description: Funge da classe padre per le classi che controllano la generazione di eventi, ad esempio gli eventi del timer.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: Classe __EventGenerator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234161"
---
# <a name="__eventgenerator-class"></a><span data-ttu-id="b18e9-103">\_\_Classe EventGenerator</span><span class="sxs-lookup"><span data-stu-id="b18e9-103">\_\_EventGenerator class</span></span>

<span data-ttu-id="b18e9-104">La classe di sistema **\_ \_ EventGenerator** è una classe di base astratta che funge da classe padre per le classi che controllano la generazione di eventi, ad esempio [gli eventi del timer](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="b18e9-104">The **\_\_EventGenerator** system class is an abstract base class that serves as a parent class for classes that control the generation of events, such as [timer events](receiving-a-timed-or-repeating-event.md).</span></span>

<span data-ttu-id="b18e9-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b18e9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b18e9-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b18e9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b18e9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b18e9-107">Syntax</span></span>

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a><span data-ttu-id="b18e9-108">Members</span><span class="sxs-lookup"><span data-stu-id="b18e9-108">Members</span></span>

<span data-ttu-id="b18e9-109">La classe **\_ \_ EventGenerator** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="b18e9-109">The **\_\_EventGenerator** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="b18e9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b18e9-110">Remarks</span></span>

<span data-ttu-id="b18e9-111">La classe **\_ \_ EventGenerator** deriva da [**\_ \_ IndicationRelated**](--indicationrelated.md), che non dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="b18e9-111">The **\_\_EventGenerator** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="b18e9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b18e9-112">Requirements</span></span>



| <span data-ttu-id="b18e9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b18e9-113">Requirement</span></span> | <span data-ttu-id="b18e9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b18e9-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b18e9-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b18e9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b18e9-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b18e9-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b18e9-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b18e9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b18e9-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b18e9-118">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b18e9-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b18e9-119">Namespace</span></span><br/>                | <span data-ttu-id="b18e9-120">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="b18e9-120">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b18e9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b18e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b18e9-122">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="b18e9-122">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="b18e9-123">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="b18e9-123">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

