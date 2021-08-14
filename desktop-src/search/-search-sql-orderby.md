---
description: Altre informazioni sulla clausola ORDER BY
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Clausola ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3815ddecc659a47d7cf2c8547b49e878c54ba6bf8537e2589eea4441d9d3f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227186"
---
# <a name="order-by-clause"></a>Clausola ORDER BY

La clausola ORDER BY ordina i risultati in base al valore di una o più colonne specificate. Di seguito è riportata la sintassi della clausola ORDER BY:


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



L'identificatore di colonna deve essere una colonna valida. È possibile usare l'identificatore di colonna per fare riferimento alle colonne in base all'ordine in cui vengono visualizzate nella query. La prima colonna della query è numerata 1. È possibile includere più colonne nella clausola ORDER BY, separate da virgole.

L'identificatore di direzione facoltativo può essere "ASC" per l'ordine crescente (da basso a alto) o "DESC" per l'ordine decrescente (dall'alto al basso). Se non si specifica un identificatore di direzione, viene usato il valore predefinito crescente. Se si specifica più di una colonna, ma non si specificano tutte le direzioni, la direzione specificata per ultima viene applicata a ogni colonna fino a quando non si modifica in modo esplicito la direzione.

Nella clausola ORDER BY seguente, ad esempio, le colonne A, B, C e G vengono ordinate in ordine crescente, mentre le colonne D, E e F vengono ordinate in ordine decrescente.


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Clausola FROM](-search-sql-from.md)
</dt> <dt>

[Clausola RANK BY](-search-sql-rankby.md)
</dt> <dt>

[Istruzione SELECT](-search-sql-select.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



