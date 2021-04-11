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
# <a name="set-statement"></a>Istruzione SET

L'istruzione SET specifica le opzioni PROPERTYNAME e RANKMETHOD per la query.

## <a name="propertyname"></a>PROPERTYNAME

È possibile associare una proprietà a un alias descrittivo per la query usando la sintassi seguente:


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a>RANKMETHOD

È possibile specificare il metodo Rank per le query con il termine l'oggetto usando la sintassi seguente:


```
SET RANKMETHOD <rankmethod>      
```



I metodi RANKMETHOD che possono essere specificati usando l'istruzione SET sono il coefficiente JACCARD, il coefficiente dei dadi e il prodotto interno.

 

 



