---
title: Script con valori delimitati da virgole (CSV)
description: Windows 2000 include un'utilità della riga di comando, CSVDE, per importare oggetti directory usando file .csv ed esportare oggetti directory come .csv file.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Script con valori delimitati da virgole AD
- Script, Valori delimitati da virgole AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3764593303f7f2a81c524df16665c74afd1c83909e8286511090ee6c84323bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022447"
---
# <a name="comma-separated-value-csv-scripts"></a>Script con valori delimitati da virgole (CSV)

Windows 2000 include un'utilità della riga di comando, CSVDE, per importare oggetti directory usando file .csv ed esportare oggetti directory come .csv file. Gli script CSV vengono creati per semplificarne l'uso. La prima riga dello script identifica gli attributi nelle righe che seguono. Le colonne sono separate da virgole. Il formato di file è compatibile con il Microsoft Excel .csv, in modo che i file siano facilmente creati. Usare Excel o qualsiasi altro strumento in grado di leggere e scrivere .csv file. CSVDE supporta Unicode.

## <a name="example-csv-file"></a>File CSV di esempio

L'esempio di codice seguente è un file CSV che aggiunge una classe ausiliaria.

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




