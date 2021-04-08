---
description: Il qualificatore dinamico indica una classe le cui istanze vengono create dinamicamente. Il valore di questo qualificatore deve essere impostato su TRUE.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Qualificatore dinamico
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880666"
---
# <a name="dynamic-qualifier"></a><span data-ttu-id="5672e-104">Qualificatore dinamico</span><span class="sxs-lookup"><span data-stu-id="5672e-104">Dynamic Qualifier</span></span>

<span data-ttu-id="5672e-105">Il qualificatore **dinamico** indica una classe le cui istanze vengono create dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="5672e-105">The **Dynamic** qualifier indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="5672e-106">Il valore di questo qualificatore deve essere impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="5672e-106">The value of this qualifier must be set to **TRUE**.</span></span>

<span data-ttu-id="5672e-107">Il qualificatore **dinamico** deve essere specificato in tutte le classi che contengono dati e per le quali le istanze vengono create dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="5672e-107">The **Dynamic** qualifier must be specified on all classes that contain data and for which instances are created dynamically.</span></span> <span data-ttu-id="5672e-108">Il qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) viene in genere specificato anche per identificare il provider responsabile per fornire i dati.</span><span class="sxs-lookup"><span data-stu-id="5672e-108">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is typically also specified to identify the provider responsible for supplying the data.</span></span>

<span data-ttu-id="5672e-109">Le classi che contengono solo metodi che necessitano di implementazione non richiedono il qualificatore **dinamico** .</span><span class="sxs-lookup"><span data-stu-id="5672e-109">Classes that contain only methods that need implementation do not require the **Dynamic** qualifier.</span></span> <span data-ttu-id="5672e-110">Per specificare il nome del provider per fornire l'implementazione è necessario solo il qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="5672e-110">Only the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is required to specify the name of the provider to supply the implementation.</span></span>

<span data-ttu-id="5672e-111">Tutte le classi derivate da una classe dinamica devono essere dinamiche.</span><span class="sxs-lookup"><span data-stu-id="5672e-111">All classes derived from a dynamic class must be dynamic.</span></span> <span data-ttu-id="5672e-112">Non è possibile derivare una classe statica da una classe dinamica.</span><span class="sxs-lookup"><span data-stu-id="5672e-112">You cannot derive a static class from a dynamic class.</span></span>

<span data-ttu-id="5672e-113">Quando si specifica **Dynamic** in una proprietà di un'istanza, è necessario specificare anche il qualificatore **PropertyContext** .</span><span class="sxs-lookup"><span data-stu-id="5672e-113">When **Dynamic** is specified on a property of an instance, the **PropertyContext** qualifier must also be specified.</span></span>

## <a name="requirements"></a><span data-ttu-id="5672e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5672e-114">Requirements</span></span>



| <span data-ttu-id="5672e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5672e-115">Requirement</span></span> | <span data-ttu-id="5672e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5672e-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5672e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5672e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5672e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5672e-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5672e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5672e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5672e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5672e-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5672e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5672e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5672e-122">**Qualificatori WMI standard**</span><span class="sxs-lookup"><span data-stu-id="5672e-122">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="5672e-123">Qualificatori WMI</span><span class="sxs-lookup"><span data-stu-id="5672e-123">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="5672e-124">Aggiunta di un qualificatore</span><span class="sxs-lookup"><span data-stu-id="5672e-124">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




