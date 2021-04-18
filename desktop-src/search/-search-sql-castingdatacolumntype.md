---
description: 'Altre informazioni su: cast del tipo di dati di una colonna'
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: Cast del tipo di dati di una colonna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71a72a84c915d066d4b088719808687a965d86b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306134"
---
# <a name="casting-the-data-type-of-a-column"></a><span data-ttu-id="e3203-103">Cast del tipo di dati di una colonna</span><span class="sxs-lookup"><span data-stu-id="e3203-103">Casting the Data Type of a Column</span></span>

<span data-ttu-id="e3203-104">In alcuni casi potrebbe essere necessario eseguire il cast dei dati di tipo stringa estratti da documenti come un altro tipo di dati, in modo da poter effettuare un confronto appropriato.</span><span class="sxs-lookup"><span data-stu-id="e3203-104">At times you may need to cast string data extracted from documents as another data type, so that an appropriate comparison can be made.</span></span> <span data-ttu-id="e3203-105">Eseguire il cast di un identificatore o un valore letterale come un altro tipo di dati usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="e3203-105">Cast an identifier or literal as another data type using the following syntax:</span></span>


```
CAST (<identifier> | <literal> AS <datatype>)
```



<span data-ttu-id="e3203-106">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e3203-106">For example:</span></span>


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a><span data-ttu-id="e3203-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3203-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3203-108">Mapping dei tipi di dati</span><span class="sxs-lookup"><span data-stu-id="e3203-108">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



