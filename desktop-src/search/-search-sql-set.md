---
description: L'istruzione SET specifica le opzioni PROPERTYNAME e RANKMETHOD per la query.
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: Istruzione SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128530"
---
# <a name="set-statement"></a><span data-ttu-id="6cebb-103">Istruzione SET</span><span class="sxs-lookup"><span data-stu-id="6cebb-103">SET Statement</span></span>

<span data-ttu-id="6cebb-104">L'istruzione SET specifica le opzioni PROPERTYNAME e RANKMETHOD per la query.</span><span class="sxs-lookup"><span data-stu-id="6cebb-104">The SET statement specifies PROPERTYNAME and RANKMETHOD options for the query.</span></span>

## <a name="propertyname"></a><span data-ttu-id="6cebb-105">PROPERTYNAME</span><span class="sxs-lookup"><span data-stu-id="6cebb-105">PROPERTYNAME</span></span>

<span data-ttu-id="6cebb-106">È possibile associare una proprietà a un alias descrittivo per la query usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="6cebb-106">You can associate a property with a friendly alias for the query by using the following syntax:</span></span>


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a><span data-ttu-id="6cebb-107">RANKMETHOD</span><span class="sxs-lookup"><span data-stu-id="6cebb-107">RANKMETHOD</span></span>

<span data-ttu-id="6cebb-108">È possibile specificare il metodo Rank per le query con il termine l'oggetto usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="6cebb-108">You can specify the rank method for queries with the ISABOUT term by using the following syntax:</span></span>


```
SET RANKMETHOD <rankmethod>      
```



<span data-ttu-id="6cebb-109">I metodi RANKMETHOD che possono essere specificati usando l'istruzione SET sono il coefficiente JACCARD, il coefficiente dei dadi e il prodotto interno.</span><span class="sxs-lookup"><span data-stu-id="6cebb-109">The RANKMETHOD methods that can be specified by using the SET statement are JACCARD COEFFICIENT, DICE COEFFICIENT, and INNER PRODUCT.</span></span>

 

 



