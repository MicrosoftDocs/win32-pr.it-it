---
description: WMI dispone di diversi tipi di qualificatori di classe e di proprietà. I qualificatori possono anche modificare le varianti.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: Qualificatori WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b14dc8f1f73571fc2c449e55c30034f86c2453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226799"
---
# <a name="wmi-qualifiers"></a><span data-ttu-id="d7df2-104">Qualificatori WMI</span><span class="sxs-lookup"><span data-stu-id="d7df2-104">WMI Qualifiers</span></span>

<span data-ttu-id="d7df2-105">WMI dispone di diversi tipi di [*qualificatori*](gloss-q.md)di classe e di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d7df2-105">WMI has several types of class and property [*qualifiers*](gloss-q.md).</span></span> <span data-ttu-id="d7df2-106">I qualificatori possono anche modificare le [*varianti*](gloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="d7df2-106">Qualifiers can also have modifying [*flavors*](gloss-f.md).</span></span> <span data-ttu-id="d7df2-107">In WMI vengono utilizzati i seguenti tipi di qualificatori e gusti.</span><span class="sxs-lookup"><span data-stu-id="d7df2-107">The following types of qualifiers and flavors are used in WMI.</span></span>

<span data-ttu-id="d7df2-108">Il nome di ogni qualificatore viene visualizzato con il tipo di dati e indica se il qualificatore può essere applicato a una classe, un'istanza, una proprietà o un metodo.</span><span class="sxs-lookup"><span data-stu-id="d7df2-108">The name of each qualifier appears with its data type and an indicator of whether the qualifier can be applied to a class, instance, property, or method.</span></span> <span data-ttu-id="d7df2-109">Per i qualificatori, ad esempio **Association** (discussa in [meta Qualifiers](meta-qualifiers.md)), è presente una regola di utilizzo implicita che deve essere presente anche per il qualificatore meta.</span><span class="sxs-lookup"><span data-stu-id="d7df2-109">For qualifiers such as **Association** (discussed under [Meta Qualifiers](meta-qualifiers.md)), there is an implied usage rule that the meta qualifier must also be present.</span></span> <span data-ttu-id="d7df2-110">Ad esempio, la regola di utilizzo implicita per i qualificatori di **aggregazione** è che deve essere presente anche il qualificatore dell' **associazione** .</span><span class="sxs-lookup"><span data-stu-id="d7df2-110">For example, the implicit usage rule for the **Aggregation** qualifiers is that the **Association** qualifier must also be present.</span></span>



| <span data-ttu-id="d7df2-111">Tipo di qualificatore</span><span class="sxs-lookup"><span data-stu-id="d7df2-111">Qualifier type</span></span>                              | <span data-ttu-id="d7df2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7df2-112">Description</span></span>                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7df2-113">Meta</span><span class="sxs-lookup"><span data-stu-id="d7df2-113">Meta</span></span>](meta-qualifiers.md)                 | <span data-ttu-id="d7df2-114">Perfeziona la definizione dei metacostrutti chiarendo l'utilizzo effettivo di una classe o di una dichiarazione di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d7df2-114">Refines the definition of meta-constructs by clarifying the actual usage of a class or property declaration.</span></span>                          |
| [<span data-ttu-id="d7df2-115">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="d7df2-115">Optional</span></span>](optional-qualifiers.md)         | <span data-ttu-id="d7df2-116">Risolve le situazioni non comuni a tutte le implementazioni conformi a CIM.</span><span class="sxs-lookup"><span data-stu-id="d7df2-116">Addresses situations not common to all CIM-compliant implementations.</span></span>                                                                 |
| [<span data-ttu-id="d7df2-117">Versioni qualificatore</span><span class="sxs-lookup"><span data-stu-id="d7df2-117">Qualifier Flavors</span></span>](qualifier-flavors.md)  | <span data-ttu-id="d7df2-118">Fornisce ulteriori informazioni su un qualificatore, ad esempio se una classe o un'istanza derivata può eseguire l'override del valore originale del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="d7df2-118">Provides more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span> |
| [<span data-ttu-id="d7df2-119">Standard</span><span class="sxs-lookup"><span data-stu-id="d7df2-119">Standard</span></span>](standard-qualifiers.md)         | <span data-ttu-id="d7df2-120">Supporta le descrizioni che devono essere gestite da tutte le implementazioni conformi a CIM.</span><span class="sxs-lookup"><span data-stu-id="d7df2-120">Supports the descriptions that all CIM-compliant implementations must handle.</span></span>                                                         |
| [<span data-ttu-id="d7df2-121">Specifiche di WMI</span><span class="sxs-lookup"><span data-stu-id="d7df2-121">WMI-specific</span></span>](wmi-specific-qualifiers.md) | <span data-ttu-id="d7df2-122">Vengono descritti i qualificatori specifici di WMI, ad esempio i qualificatori della classe del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d7df2-122">Describes qualifiers specific to WMI, such as performance counter class qualifiers.</span></span>                                                   |



 

<span data-ttu-id="d7df2-123">Per ulteriori informazioni sull'applicazione dei qualificatori alle classi WMI, vedere [aggiunta di un qualificatore](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="d7df2-123">For more information on applying qualifiers to your WMI classes, see [Adding a Qualifier](adding-a-qualifier.md).</span></span> <span data-ttu-id="d7df2-124">Per informazioni su come esaminare i qualificatori nelle classi WMI esistenti, vedere il codice di esempio riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d7df2-124">To see how to examine qualifiers on existing WMI classes, see the example code below.</span></span>

## <a name="example"></a><span data-ttu-id="d7df2-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="d7df2-125">Example</span></span>

<span data-ttu-id="d7df2-126">Il codice di PowerShell seguente, tratto dalla [Raccolta TechNet](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), descrive come recuperare i qualificatori da una classe WMI.</span><span class="sxs-lookup"><span data-stu-id="d7df2-126">The following PowerShell code, taken from the [TechNet gallery](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), describes how to retrieve qualifiers from a WMI class.</span></span>


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 



