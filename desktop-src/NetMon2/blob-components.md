---
description: Componenti BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componenti BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bd9ab8389cdd49a266855106891a91fcfbd0b4f69c7d22b5855143b34f376c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367483"
---
# <a name="blob-components"></a>Componenti BLOB

Un BLOB (Binary Large Object) include i componenti gerarchici seguenti:

-   Proprietari
-   Categorie
-   Tag
-   Valori

## <a name="textual-representation"></a>Rappresentazione testuale

Per praticità, i BLOB vengono visualizzati nel formato Owner:Category:Tag:Value in cui vengono visualizzati quando vengono salvati in un file. La struttura interna del BLOB è opaca perché rappresenta puntatori e tabelle. Ad esempio, ecco una voce da un BLOB che può essere usata per configurare un NPP:

``` syntax
NPP:Configure:BufferSize=32768
```

Il proprietario è NPP. La categoria è Configura, il tag è BufferSize e il valore è 32768.

 

 



