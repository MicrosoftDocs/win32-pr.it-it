---
title: Script con valori delimitati da virgole (CSV)
description: Windows 2000 include un'utilità da riga di comando, CSVDE, per importare gli oggetti directory usando i file CSV ed esportare gli oggetti directory come file con estensione CSV.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Script AD con valori delimitati da virgole
- Script, valore delimitato da virgole AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec737f971bd7e462b8f6f0ef6e9e3df786a207cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707201"
---
# <a name="comma-separated-value-csv-scripts"></a>Script con valori delimitati da virgole (CSV)

Windows 2000 include un'utilità da riga di comando, CSVDE, per importare gli oggetti directory usando i file CSV ed esportare gli oggetti directory come file con estensione CSV. Gli script CSV vengono creati per facilitarne l'uso. La prima riga nello script identifica gli attributi nelle righe che seguono. Le colonne sono separate da virgole. Il formato del file è compatibile con il formato Microsoft Excel. csv, in modo che i file vengano creati facilmente. Utilizzare Excel o qualsiasi altro strumento in grado di leggere e scrivere file con estensione CSV. CSVDE supporta Unicode.

## <a name="example-csv-file"></a>File CSV di esempio

L'esempio di codice seguente è un file CSV che aggiunge una classe ausiliaria.

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




