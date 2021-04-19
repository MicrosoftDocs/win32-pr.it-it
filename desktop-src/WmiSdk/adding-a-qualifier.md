---
description: Un qualificatore è una stringa di dati che fornisce ulteriori informazioni su una classe, un'istanza, una proprietà, un metodo o un parametro.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Aggiunta di un qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319806"
---
# <a name="adding-a-qualifier"></a><span data-ttu-id="90c7c-103">Aggiunta di un qualificatore</span><span class="sxs-lookup"><span data-stu-id="90c7c-103">Adding a Qualifier</span></span>

<span data-ttu-id="90c7c-104">Un qualificatore è una stringa di dati che fornisce ulteriori informazioni su una classe, un'istanza, una proprietà, un metodo o un parametro.</span><span class="sxs-lookup"><span data-stu-id="90c7c-104">A qualifier is a data string that provides more information about a class, instance, property, method, or parameter.</span></span>

<span data-ttu-id="90c7c-105">La definizione di classe seguente è un esempio di classe derivata con qualificatori di classe.</span><span class="sxs-lookup"><span data-stu-id="90c7c-105">The following class definition is an example of a derived class that has class qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

<span data-ttu-id="90c7c-106">I qualificatori possono essere divisi in qualificatori standard, qualificatori CIM e qualificatori esclusivi includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="90c7c-106">Qualifiers can be divided into standard qualifiers, CIM qualifiers, and unique qualifiers include the following:</span></span>

-   <span data-ttu-id="90c7c-107">Qualificatore standard</span><span class="sxs-lookup"><span data-stu-id="90c7c-107">Standard qualifier</span></span>

    <span data-ttu-id="90c7c-108">Un qualificatore standard è un qualificatore definito da WMI e comunemente utilizzato nel codice MOF.</span><span class="sxs-lookup"><span data-stu-id="90c7c-108">A standard qualifier is a qualifier defined by WMI and commonly used in MOF code.</span></span> <span data-ttu-id="90c7c-109">Ad esempio, i qualificatori [**dinamici**](dynamic-qualifier.md) e di [**lettura**](standard-qualifiers.md) sono entrambi qualificatori standard.</span><span class="sxs-lookup"><span data-stu-id="90c7c-109">For example, the [**Dynamic**](dynamic-qualifier.md) and [**Read**](standard-qualifiers.md) qualifiers are both standard qualifiers.</span></span> <span data-ttu-id="90c7c-110">Per ulteriori informazioni, vedere [qualificatori WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="90c7c-110">For more information, see [WMI Qualifiers](wmi-qualifiers.md).</span></span>

-   <span data-ttu-id="90c7c-111">Qualificatore CIM</span><span class="sxs-lookup"><span data-stu-id="90c7c-111">CIM qualifier</span></span>

    <span data-ttu-id="90c7c-112">Un qualificatore CIM è un qualificatore incluso nella specifica CIM.</span><span class="sxs-lookup"><span data-stu-id="90c7c-112">A CIM qualifier is a qualifier included in the CIM specification.</span></span> <span data-ttu-id="90c7c-113">Sebbene usino i qualificatori CIM nel codice MOF, i qualificatori standard sono progettati specificamente con WMI.</span><span class="sxs-lookup"><span data-stu-id="90c7c-113">While use CIM qualifiers in MOF code, the standard qualifiers are designed specifically with WMI in mind.</span></span> <span data-ttu-id="90c7c-114">Per ulteriori informazioni, vedere la [specifica DMTF CIM](https://www.dmtf.org/spec/cims.html/).</span><span class="sxs-lookup"><span data-stu-id="90c7c-114">For more information, see the DMTF [CIM Specification](https://www.dmtf.org/spec/cims.html/).</span></span>

-   <span data-ttu-id="90c7c-115">Qualificatore univoco</span><span class="sxs-lookup"><span data-stu-id="90c7c-115">Unique qualifier</span></span>

    <span data-ttu-id="90c7c-116">Un qualificatore univoco è un qualificatore definito in modo specifico per una nuova classe da un provider di classi.</span><span class="sxs-lookup"><span data-stu-id="90c7c-116">A unique qualifier is a qualifier defined specifically for a new class by a class provider.</span></span> <span data-ttu-id="90c7c-117">Ad esempio, il qualificatore [**unità**](standard-qualifiers.md) è un qualificatore specifico del provider non standard.</span><span class="sxs-lookup"><span data-stu-id="90c7c-117">For example, the [**Units**](standard-qualifiers.md) qualifier is a nonstandard, provider-specific qualifier.</span></span> <span data-ttu-id="90c7c-118">È possibile creare qualificatori personalizzati da usare con il provider.</span><span class="sxs-lookup"><span data-stu-id="90c7c-118">You can create your own qualifiers for use with your provider.</span></span> <span data-ttu-id="90c7c-119">Per ulteriori informazioni sulla creazione di un provider, vedere [sviluppo di un provider WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="90c7c-119">For more information about creating a provider, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

<span data-ttu-id="90c7c-120">Indipendentemente dal qualificatore, il processo principale da eseguire è usare il qualificatore nel codice MOF.</span><span class="sxs-lookup"><span data-stu-id="90c7c-120">Whatever your qualifier does, the main process you perform is to use the qualifier in your MOF code.</span></span> <span data-ttu-id="90c7c-121">Per ulteriori informazioni, vedere [applying a Qualifier](applying-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="90c7c-121">For more information, see [Applying a Qualifier](applying-a-qualifier.md).</span></span> <span data-ttu-id="90c7c-122">È possibile descrivere ulteriormente un qualificatore con una versione del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="90c7c-122">You can further describe a qualifier with a qualifier flavor.</span></span> <span data-ttu-id="90c7c-123">Una versione qualificatore contiene ulteriori informazioni sulla modalità di utilizzo di un qualificatore da un provider.</span><span class="sxs-lookup"><span data-stu-id="90c7c-123">A qualifier flavor contains more information regarding how a provider should use a qualifier.</span></span> <span data-ttu-id="90c7c-124">Per ulteriori informazioni, vedere [Descrizione di un qualificatore con una versione del qualificatore](describing-a-qualifier-with-a-qualifier-flavor.md).</span><span class="sxs-lookup"><span data-stu-id="90c7c-124">For more information, see [Describing a Qualifier with a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90c7c-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90c7c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90c7c-126">Progettazione di classi Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="90c7c-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



