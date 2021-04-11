---
description: 'Altre informazioni su: clausola ORDER BY'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Clausola ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128535"
---
# <a name="order-by-clause"></a>Clausola ORDER BY

La clausola ORDER BY ordina i risultati in base al valore di una o più colonne specificate. Di seguito è riportata la sintassi della clausola ORDER BY:


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



L'identificatore di colonna deve essere una colonna valida. È possibile utilizzare l'identificatore di colonna per fare riferimento alle colonne in base all'ordine in cui sono visualizzate nella query. La prima colonna della query è numerata 1. È possibile includere più di una colonna nella clausola ORDER BY, separate da virgole.

L'identificatore di direzione facoltativo può essere "ASC" per l'ordine crescente (da basso a alto) o "DESC" per la decrescente (da alto a basso). Se non si specifica un identificatore di direzione, viene usato il valore predefinito Ascending. Se si specifica più di una colonna, ma non si specificano tutte le direzioni, la direzione specificata per ultima viene applicata a ogni colonna fino a quando non si modifica in modo esplicito la direzione.

Nella clausola ORDER BY seguente, ad esempio, le colonne A, B, C e G vengono ordinate in ordine crescente, mentre le colonne D, E e F sono ordinate in ordine decrescente.


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Clausola FROM](-search-sql-from.md)
</dt> <dt>

[RANGO per clausola](-search-sql-rankby.md)
</dt> <dt>

[SELECT (istruzione)](-search-sql-select.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



