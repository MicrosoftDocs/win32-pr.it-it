---
title: SNB (Objidl.h)
description: Un blocco di nomi di stringa (SNB) è un puntatore a una matrice di puntatori a stringhe, che termina con un puntatore NULL.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- Bns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49a7868912b9d7d1e3d9f3b1f82805e6e285d815eacbc559c887febd23e9e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682781"
---
# <a name="snb"></a>Bns

Un blocco di nomi di stringa (**SNB**) è un puntatore a una matrice di puntatori a stringhe, che termina con un **puntatore NULL.** I blocchi di nomi di stringa vengono usati [**dall'interfaccia IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e dalle chiamate di funzione che aprono oggetti di archiviazione. Le stringhe puntano a flussi o oggetti di archiviazione contenuti che devono essere esclusi nelle chiamate aperte.


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

**Bns**
</dt> <dd>

\[wire \_ marshal(wireSNB)\]

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'SNB** deve essere creato allocando un blocco contiguo di memoria in cui i puntatori alle stringhe sono seguiti da un puntatore **NULL,** seguito quindi dalle stringhe effettive.

Il marshalling di **un SNB** si basa sul presupposto che il **servizio SNB** passato sia stato creato in questo modo. Sebbene possa essere archiviato in altri modi, il **servizio SNB** creato in questo modo ha il vantaggio di richiedere una sola operazione di allocazione e una di liberare memoria per tutte le stringhe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows app desktop di Windows 2000 Server \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Objidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Objidl.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





