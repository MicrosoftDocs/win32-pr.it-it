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
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a>Recupero della documentazione per oggetti dati sulle prestazioni non elaborati e formattati

Nell'argomento seguente viene illustrato come recuperare la documentazione di programmazione online per un oggetto dati non elaborato o formattato in modo dinamico.

WMI contiene una serie di oggetti che tengono traccia delle prestazioni. Le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contengono dati sulle prestazioni non elaborati o "non cotti" e sono supportate dal [provider del contatore delle prestazioni](performance-counter-provider.md). Al contrario, le classi derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contengono dati "cotti" o formattati e sono supportati dal [provider di dati delle prestazioni formattato](formatted-performance-data-provider.md).

Tuttavia, entrambi i provider supportano diverse classi figlio create dinamicamente. Poiché le proprietà vengono aggiunte in fase di esecuzione, queste classi possono contenere proprietà non documentate. È possibile usare il codice seguente per identificare le proprietà di una determinata classe creata dinamicamente.

**Per recuperare una descrizione di una classe creata dinamicamente**

1.  Creare un'istanza dell'elemento e impostare il qualificatore modificato su true.

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  Recuperare le proprietà della classe.

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  Visualizzare le proprietà.

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

Il codice seguente recupera le descrizioni delle proprietà per l' [**oggetto \_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) specificato.


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



 

 
