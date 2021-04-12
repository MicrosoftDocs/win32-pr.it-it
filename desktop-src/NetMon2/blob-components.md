---
description: Componenti BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componenti BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232678"
---
# <a name="blob-components"></a>Componenti BLOB

Un oggetto binario di grandi dimensioni (BLOB) include i componenti gerarchici seguenti:

-   Proprietari
-   Categorie
-   Tag
-   Valori

## <a name="textual-representation"></a>Rappresentazione testuale

Per praticità, i BLOB vengono visualizzati nel formato proprietario: Categoria: Tag: valore in cui compaiono quando vengono salvati in un file. La struttura interna del BLOB è opaca perché rappresenta i puntatori e le tabelle. Ecco ad esempio una voce di un BLOB che può essere usata per configurare un NPP:

``` syntax
NPP:Configure:BufferSize=32768
```

Il proprietario è NPP. La categoria è configure, il tag è BufferSize e il valore è 32768.

 

 



