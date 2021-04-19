---
description: Utilizzare l'operatore ISA nella clausola WHERE di una query di dati per richiedere oggetti incorporati in una gerarchia di classi.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Operatore ISA per query di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315209"
---
# <a name="isa-operator-for-data-queries"></a>Operatore ISA per query di dati

Utilizzare l'operatore ISA nella clausola WHERE di una query di dati per richiedere oggetti incorporati in una gerarchia di classi.

Nell'esempio seguente viene illustrata la sintassi per richiedere oggetti incorporati in una gerarchia di classi.


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



Il risultato include istanze della **classe** con oggetti incorporati derivati da **ParentClass** nella proprietà **EmbeddedProp** . Non tutte le istanze dell'oggetto **classe** sono derivate da **ParentClass**, ma il risultato restituisce gli oggetti incorporati derivati da **ParentClass**.

Ad esempio, nella query seguente, **ClassA** include la proprietà **EmbeddedObj** con tipizzazione debole. La classe **ClassA** ha dieci istanze. Cinque di queste istanze hanno oggetti incorporati con un tipo derivato da **ClassZ**. Gli altri cinque hanno oggetti incorporati di altri tipi.

Nell'esempio seguente viene illustrata la query che restituisce le cinque istanze di che includono gli oggetti derivati da **ClassZ**.


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



