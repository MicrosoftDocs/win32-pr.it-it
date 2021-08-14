---
description: WMI dispone di diversi tipi di qualificatori di classe e proprietà. I qualificatori possono anche avere tipi di modifica.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: Qualificatori WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf51888592949aadefec7c864dc0a24df6a4fa68f6fb34c8e3cda880da6873
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502811"
---
# <a name="wmi-qualifiers"></a>Qualificatori WMI

WMI dispone di diversi tipi di qualificatori di classe [*e proprietà.*](gloss-q.md) I qualificatori possono anche avere tipi [*di modifica.*](gloss-f.md) In WMI vengono utilizzati i tipi seguenti di qualificatori e tipi.

Il nome di ogni qualificatore viene visualizzato con il tipo di dati e un indicatore che indica se il qualificatore può essere applicato a una classe, un'istanza, una proprietà o un metodo. Per i qualificatori, ad esempio **Association** (descritti in [Meta qualifiers),](meta-qualifiers.md)esiste una regola di utilizzo implicita in base alla quale deve essere presente anche il meta qualificatore. Ad esempio, la regola di utilizzo implicito per i **qualificatori di** aggregazione è che **deve** essere presente anche il qualificatore association.



| Tipo di qualificatore                              | Descrizione                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Meta](meta-qualifiers.md)                 | Affina la definizione dei meta-costrutti chiarindo l'utilizzo effettivo di una dichiarazione di classe o proprietà.                          |
| [Facoltativo](optional-qualifiers.md)         | Risolve situazioni non comuni a tutte le implementazioni conformi a CIM.                                                                 |
| [Qualificatori flavors](qualifier-flavors.md)  | Fornisce altre informazioni su un qualificatore, ad esempio se una classe derivata o un'istanza può eseguire l'override del valore originale del qualificatore. |
| [Standard](standard-qualifiers.md)         | Supporta le descrizioni che devono essere gestite da tutte le implementazioni conformi a CIM.                                                         |
| [Specifico di WMI](wmi-specific-qualifiers.md) | Descrive i qualificatori specifici di WMI, ad esempio i qualificatori della classe del contatore delle prestazioni.                                                   |



 

Per altre informazioni sull'applicazione di qualificatori alle classi WMI, vedere [Aggiunta di un qualificatore.](adding-a-qualifier.md) Per informazioni su come esaminare i qualificatori nelle classi WMI esistenti, vedere il codice di esempio riportato di seguito.

## <a name="example"></a>Esempio

Il codice di PowerShell seguente, tratto dalla [raccolta TechNet,](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7)descrive come recuperare qualificatori da una classe WMI.


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



 

 



