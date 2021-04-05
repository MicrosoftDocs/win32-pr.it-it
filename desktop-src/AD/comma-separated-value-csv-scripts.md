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
# <a name="comma-separated-value-csv-scripts"></a><span data-ttu-id="4afbc-105">Script con valori delimitati da virgole (CSV)</span><span class="sxs-lookup"><span data-stu-id="4afbc-105">Comma-separated Value (CSV) Scripts</span></span>

<span data-ttu-id="4afbc-106">Windows 2000 include un'utilità da riga di comando, CSVDE, per importare gli oggetti directory usando i file CSV ed esportare gli oggetti directory come file con estensione CSV.</span><span class="sxs-lookup"><span data-stu-id="4afbc-106">Windows 2000 includes a command-line utility, CSVDE, to import directory objects using .csv files and export directory objects as .csv files.</span></span> <span data-ttu-id="4afbc-107">Gli script CSV vengono creati per facilitarne l'uso.</span><span class="sxs-lookup"><span data-stu-id="4afbc-107">CSV scripts are created for ease-of-use.</span></span> <span data-ttu-id="4afbc-108">La prima riga nello script identifica gli attributi nelle righe che seguono.</span><span class="sxs-lookup"><span data-stu-id="4afbc-108">The first line in the script identifies the attributes in the lines that follow.</span></span> <span data-ttu-id="4afbc-109">Le colonne sono separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="4afbc-109">Columns are separated by commas.</span></span> <span data-ttu-id="4afbc-110">Il formato del file è compatibile con il formato Microsoft Excel. csv, in modo che i file vengano creati facilmente.</span><span class="sxs-lookup"><span data-stu-id="4afbc-110">The file format is compatible with the Microsoft Excel .csv format, so that files are easily created.</span></span> <span data-ttu-id="4afbc-111">Utilizzare Excel o qualsiasi altro strumento in grado di leggere e scrivere file con estensione CSV.</span><span class="sxs-lookup"><span data-stu-id="4afbc-111">Use Excel or any other tool that can read and write .csv files.</span></span> <span data-ttu-id="4afbc-112">CSVDE supporta Unicode.</span><span class="sxs-lookup"><span data-stu-id="4afbc-112">CSVDE supports Unicode.</span></span>

## <a name="example-csv-file"></a><span data-ttu-id="4afbc-113">File CSV di esempio</span><span class="sxs-lookup"><span data-stu-id="4afbc-113">Example CSV File</span></span>

<span data-ttu-id="4afbc-114">L'esempio di codice seguente è un file CSV che aggiunge una classe ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="4afbc-114">The following code example is a CSV file that adds an auxiliary class.</span></span>

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




