---
description: Usare l'operatore ISA nella clausola WHERE di una query di dati per richiedere oggetti incorporati in una gerarchia di classi.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Operatore ISA per query di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b33c0bc4b78101a4b1e6a38997518fec543b9eb49e42b28cbb2500c321f56ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318303"
---
# <a name="isa-operator-for-data-queries"></a>Operatore ISA per query di dati

Usare l'operatore ISA nella clausola WHERE di una query di dati per richiedere oggetti incorporati in una gerarchia di classi.

Nell'esempio seguente viene illustrata la sintassi per richiedere oggetti incorporati in una gerarchia di classi.


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



Il risultato include le istanze **di Class** con oggetti incorporati derivati da **ParentClass** nella **proprietà EmbeddedProp.** Non tutte le istanze **dell'oggetto Class** derivano da **ParentClass**, ma il risultato restituisce gli oggetti incorporati derivati da **ParentClass**.

Nella query seguente, ad esempio, **ClassA** include la proprietà **EmbeddedObj** con tipi di dati deboli. La **classe ClassA** ha dieci istanze. Cinque di queste istanze hanno oggetti incorporati con un tipo derivato da **ClassZ**. Gli altri cinque hanno oggetti incorporati di altri tipi.

Nell'esempio seguente viene illustrata la query che restituisce le cinque istanze di , che includono gli oggetti derivati da **ClassZ**.


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



