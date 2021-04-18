---
description: Un provider di proprietà utilizza i metodi IWbemPropertyProvider come interfaccia principale di WMI. Con IWbemPropertyProvider è possibile implementare il codice per recuperare e modificare le proprietà di classe e istanza.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia primaria per un provider di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315213"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a><span data-ttu-id="09cb9-104">Implementazione dell'interfaccia primaria per un provider di proprietà</span><span class="sxs-lookup"><span data-stu-id="09cb9-104">Implementing the Primary Interface for a Property Provider</span></span>

<span data-ttu-id="09cb9-105">Un provider di proprietà utilizza i metodi [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) come interfaccia principale di WMI.</span><span class="sxs-lookup"><span data-stu-id="09cb9-105">A property provider uses the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods as the primary interface to WMI.</span></span> <span data-ttu-id="09cb9-106">Con **IWbemPropertyProvider** è possibile implementare il codice per recuperare e modificare le proprietà di classe e istanza.</span><span class="sxs-lookup"><span data-stu-id="09cb9-106">With **IWbemPropertyProvider**, you can implement the code to retrieve and modify class and instance properties.</span></span>

<span data-ttu-id="09cb9-107">Nella tabella seguente sono elencati i metodi [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) che è possibile implementare per un provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="09cb9-107">The following table lists the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods that you can implement for a property provider.</span></span>



| <span data-ttu-id="09cb9-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="09cb9-108">Method</span></span>                                                   | <span data-ttu-id="09cb9-109">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="09cb9-109">Feature</span></span>      |
|----------------------------------------------------------|--------------|
| [<span data-ttu-id="09cb9-110">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="09cb9-110">**GetProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | <span data-ttu-id="09cb9-111">Recupero</span><span class="sxs-lookup"><span data-stu-id="09cb9-111">Retrieval</span></span>    |
| [<span data-ttu-id="09cb9-112">**PutProperty**</span><span class="sxs-lookup"><span data-stu-id="09cb9-112">**PutProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | <span data-ttu-id="09cb9-113">Modifica</span><span class="sxs-lookup"><span data-stu-id="09cb9-113">Modification</span></span> |



 

> [!Note]  
> <span data-ttu-id="09cb9-114">È necessario implementare un provider di proprietà come provider in-process.</span><span class="sxs-lookup"><span data-stu-id="09cb9-114">You must implement a property provider as an in-process provider.</span></span> <span data-ttu-id="09cb9-115">WMI inizializza i provider di proprietà scritti come servizi o file eseguibili, ma non chiama mai i metodi [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) e [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) .</span><span class="sxs-lookup"><span data-stu-id="09cb9-115">WMI will initialize property providers written as services or executable files but will never call their [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) methods.</span></span>

 

<span data-ttu-id="09cb9-116">Se si sceglie di non supportare uno di questi metodi, il provider può fornire un'implementazione stub che restituisce **il \_ provider WBEM E \_ \_ non \_ idoneo**.</span><span class="sxs-lookup"><span data-stu-id="09cb9-116">If you choose not to support one of these methods, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span>

<span data-ttu-id="09cb9-117">Un provider di proprietà identifica una classe o un'istanza gestita da un set di tre qualificatori: **PropertyContext**, **InstanceContext** e **ClassContext**.</span><span class="sxs-lookup"><span data-stu-id="09cb9-117">A property provider identifies a managed class or instance by a set of three qualifiers: **PropertyContext**, **InstanceContext**, and **ClassContext**.</span></span> <span data-ttu-id="09cb9-118">WMI passerà le costanti stringa che descrivono questi tre qualificatori al provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="09cb9-118">WMI will pass in string constants describing these three qualifiers to your property provider.</span></span>

<span data-ttu-id="09cb9-119">Il provider di proprietà deve essere preparato a gestire i seguenti tipi di qualificatori di contesto:</span><span class="sxs-lookup"><span data-stu-id="09cb9-119">Your property provider must be prepared to handle the following types of context qualifiers:</span></span>

-   <span data-ttu-id="09cb9-120">Il qualificatore **InstanceContext** è associato a un'istanza e contiene informazioni che si applicano a ogni proprietà nell'istanza.</span><span class="sxs-lookup"><span data-stu-id="09cb9-120">The **InstanceContext** qualifier is attached to an instance and contains information that applies to every property in the instance.</span></span>
-   <span data-ttu-id="09cb9-121">Il qualificatore **ClassContext** è associato a una classe e contiene informazioni che si applicano a ogni istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="09cb9-121">The **ClassContext** qualifier is attached to a class and contains information that applies to every instance in the class.</span></span> <span data-ttu-id="09cb9-122">Ad esempio, in una classe utilizzata per archiviare i dati forniti dal provider del registro di sistema, **ClassContext** può essere il percorso della chiave del registro di sistema che contiene le proprietà da segnalare.</span><span class="sxs-lookup"><span data-stu-id="09cb9-122">For example, in a class used to store data supplied by the Registry provider, **ClassContext** can be the path to the registry key that contains the properties to be reported.</span></span>
-   <span data-ttu-id="09cb9-123">Il qualificatore **PropertyContext** specifica informazioni specifiche del contesto relative alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="09cb9-123">The **PropertyContext** qualifier specifies context-specific information that pertains to the property.</span></span> <span data-ttu-id="09cb9-124">Ad esempio, in una classe utilizzata per archiviare i dati forniti dal provider del registro di sistema, **PropertyContext** specifica il nome del valore del registro di sistema da archiviare con la proprietà.</span><span class="sxs-lookup"><span data-stu-id="09cb9-124">For example, in a class used to store data supplied by the Registry provider, **PropertyContext** specifies the name of the registry value to be stored by the property.</span></span>

<span data-ttu-id="09cb9-125">Questi qualificatori possono interagire tra loro.</span><span class="sxs-lookup"><span data-stu-id="09cb9-125">These qualifiers can work together.</span></span> <span data-ttu-id="09cb9-126">È possibile designare sia un valore **InstanceContext** che **PropertyContext** per indicare al provider come trattare particolari tipi di istanze.</span><span class="sxs-lookup"><span data-stu-id="09cb9-126">You can designate both an **InstanceContext** and **PropertyContext** value to tell the provider how to treat particular types of instances.</span></span> <span data-ttu-id="09cb9-127">È possibile, ad esempio, contrassegnare le istanze che il provider rileverà come leggibile, ma che disponga di una sola proprietà scrivibile.</span><span class="sxs-lookup"><span data-stu-id="09cb9-127">For example, you might want to mark instances the provider will recognize as readable but having only one writeable property.</span></span>

<span data-ttu-id="09cb9-128">Il qualificatore più comune usato è **PropertyContext**.</span><span class="sxs-lookup"><span data-stu-id="09cb9-128">The most common qualifier used is **PropertyContext**.</span></span> <span data-ttu-id="09cb9-129">Pertanto, WMI fornisce il qualificatore **DynProps** come collegamento.</span><span class="sxs-lookup"><span data-stu-id="09cb9-129">Therefore, WMI provides the **DynProps** qualifier as a shortcut.</span></span> <span data-ttu-id="09cb9-130">WMI considera ogni proprietà di un'istanza contrassegnata con **DynProps** per avere anche i qualificatori **Dynamic**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)e **PropertyContext** .</span><span class="sxs-lookup"><span data-stu-id="09cb9-130">WMI considers each property in an instance marked with **DynProps** to also have the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** qualifiers.</span></span>

 

 



