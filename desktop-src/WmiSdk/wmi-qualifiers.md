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
# <a name="wmi-qualifiers"></a>Qualificatori WMI

WMI dispone di diversi tipi di [*qualificatori*](gloss-q.md)di classe e di proprietà. I qualificatori possono anche modificare le [*varianti*](gloss-f.md). In WMI vengono utilizzati i seguenti tipi di qualificatori e gusti.

Il nome di ogni qualificatore viene visualizzato con il tipo di dati e indica se il qualificatore può essere applicato a una classe, un'istanza, una proprietà o un metodo. Per i qualificatori, ad esempio **Association** (discussa in [meta Qualifiers](meta-qualifiers.md)), è presente una regola di utilizzo implicita che deve essere presente anche per il qualificatore meta. Ad esempio, la regola di utilizzo implicita per i qualificatori di **aggregazione** è che deve essere presente anche il qualificatore dell' **associazione** .



| Tipo di qualificatore                              | Descrizione                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Meta](meta-qualifiers.md)                 | Perfeziona la definizione dei metacostrutti chiarendo l'utilizzo effettivo di una classe o di una dichiarazione di proprietà.                          |
| [Facoltativo](optional-qualifiers.md)         | Risolve le situazioni non comuni a tutte le implementazioni conformi a CIM.                                                                 |
| [Versioni qualificatore](qualifier-flavors.md)  | Fornisce ulteriori informazioni su un qualificatore, ad esempio se una classe o un'istanza derivata può eseguire l'override del valore originale del qualificatore. |
| [Standard](standard-qualifiers.md)         | Supporta le descrizioni che devono essere gestite da tutte le implementazioni conformi a CIM.                                                         |
| [Specifiche di WMI](wmi-specific-qualifiers.md) | Vengono descritti i qualificatori specifici di WMI, ad esempio i qualificatori della classe del contatore delle prestazioni.                                                   |



 

Per ulteriori informazioni sull'applicazione dei qualificatori alle classi WMI, vedere [aggiunta di un qualificatore](adding-a-qualifier.md). Per informazioni su come esaminare i qualificatori nelle classi WMI esistenti, vedere il codice di esempio riportato di seguito.

## <a name="example"></a>Esempio

Il codice di PowerShell seguente, tratto dalla [Raccolta TechNet](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), descrive come recuperare i qualificatori da una classe WMI.


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



 

 



