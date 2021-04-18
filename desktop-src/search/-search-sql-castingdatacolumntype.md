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
# <a name="casting-the-data-type-of-a-column"></a>Cast del tipo di dati di una colonna

In alcuni casi potrebbe essere necessario eseguire il cast dei dati di tipo stringa estratti da documenti come un altro tipo di dati, in modo da poter effettuare un confronto appropriato. Eseguire il cast di un identificatore o un valore letterale come un altro tipo di dati usando la sintassi seguente:


```
CAST (<identifier> | <literal> AS <datatype>)
```



Ad esempio:


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping dei tipi di dati](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



