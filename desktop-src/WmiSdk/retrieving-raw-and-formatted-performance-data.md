---
description: Nell'argomento seguente viene illustrato come recuperare la documentazione di programmazione online per un oggetto dati non elaborato o formattato in modo dinamico.
ms.assetid: B3CD7E2C-9FCF-42FB-8713-01A696E905B0
ms.tgt_platform: multiple
title: Recupero della documentazione per oggetti dati sulle prestazioni non elaborati e formattati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ab9cf66aa4536da25102511fdcbcab6bdd5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349241"
---
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a><span data-ttu-id="e88a4-103">Recupero della documentazione per oggetti dati sulle prestazioni non elaborati e formattati</span><span class="sxs-lookup"><span data-stu-id="e88a4-103">Retrieving Documentation for Raw and Formatted Performance Data Objects</span></span>

<span data-ttu-id="e88a4-104">Nell'argomento seguente viene illustrato come recuperare la documentazione di programmazione online per un oggetto dati non elaborato o formattato in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="e88a4-104">The following topic describes how to retrieve the on-line programming documentation for a dynamically-created raw or formatted data object.</span></span>

<span data-ttu-id="e88a4-105">WMI contiene una serie di oggetti che tengono traccia delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e88a4-105">WMI contains a number of objects that track performance.</span></span> <span data-ttu-id="e88a4-106">Le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contengono dati sulle prestazioni non elaborati o "non cotti" e sono supportate dal [provider del contatore delle prestazioni](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e88a4-106">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contain raw, or "uncooked" performance data, and are supported by the [Performance Counter provider](performance-counter-provider.md).</span></span> <span data-ttu-id="e88a4-107">Al contrario, le classi derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contengono dati "cotti" o formattati e sono supportati dal [provider di dati delle prestazioni formattato](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e88a4-107">In contrast, classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contain "cooked", or formatted data, and are supported by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="e88a4-108">Tuttavia, entrambi i provider supportano diverse classi figlio create dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="e88a4-108">However, both providers support a number of dynamically-created child classes.</span></span> <span data-ttu-id="e88a4-109">Poiché le proprietà vengono aggiunte in fase di esecuzione, queste classi possono contenere proprietà non documentate.</span><span class="sxs-lookup"><span data-stu-id="e88a4-109">Because the properties are added at run-time, these classes may contain undocumented properties.</span></span> <span data-ttu-id="e88a4-110">È possibile usare il codice seguente per identificare le proprietà di una determinata classe creata dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="e88a4-110">You can use the following code to identify what properties a given dynamically-created class has.</span></span>

<span data-ttu-id="e88a4-111">**Per recuperare una descrizione di una classe creata dinamicamente**</span><span class="sxs-lookup"><span data-stu-id="e88a4-111">**To retrieve a description of a dynamically-created class**</span></span>

1.  <span data-ttu-id="e88a4-112">Creare un'istanza dell'elemento e impostare il qualificatore modificato su true.</span><span class="sxs-lookup"><span data-stu-id="e88a4-112">Create an instance of the item, and set the amended qualifier to true.</span></span>

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  <span data-ttu-id="e88a4-113">Recuperare le proprietà della classe.</span><span class="sxs-lookup"><span data-stu-id="e88a4-113">Retrieve the properties of the class.</span></span>

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  <span data-ttu-id="e88a4-114">Visualizzare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="e88a4-114">Display the properties.</span></span>

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

<span data-ttu-id="e88a4-115">Il codice seguente recupera le descrizioni delle proprietà per l' [**oggetto \_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) specificato.</span><span class="sxs-lookup"><span data-stu-id="e88a4-115">The following code retrieves the property descriptions for the specified [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) object.</span></span>


```PowerShell
$osClass = New-Object System.Management.ManagementClass Win32_PerfFormattedData_APPPOOLCountersProvider_APPPOOLWAS  
$osClass.Options.UseAmendedQualifiers = $true  
  
# Get the Properties in the class  
$properties = $osClass.Properties  
"This class has {0} properties as follows:" -f $properties.count  
  
  
# display the Property name, description, type, qualifiers and instance values  
  
foreach ($property in $properties) {  
"Property Name: {0}" -f $property.Name  
"Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
"Type:          {0}" -f $property.Type  
"-------"  
}
```



 

 
