---
title: BNS (objidl. h)
description: Un blocco di nome stringa (BNS) è un puntatore a una matrice di puntatori alle stringhe che termina con un puntatore NULL.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- BNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963992"
---
# <a name="snb"></a>BNS

Un blocco di nome stringa (**BNS**) è un puntatore a una matrice di puntatori alle stringhe che termina con un puntatore **null** . I blocchi dei nomi di stringa vengono usati dall'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e dalle chiamate di funzione che aprono gli oggetti di archiviazione. Le stringhe puntano a oggetti o flussi di archiviazione contenuti che devono essere esclusi nelle chiamate aperte.


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

**BNS**
</dt> <dd>

\[\_marshalling Wire (wireSNB)\]

</dd> </dl>

## <a name="remarks"></a>Commenti

È necessario creare la **BNS** allocando un blocco di memoria contiguo in cui i puntatori alle stringhe sono seguiti da un puntatore **null** , seguito dalle stringhe effettive.

Il marshalling di un **BNS** si basa sul presupposto che la **BNS** passata è stata creata in questo modo. Sebbene possa essere archiviato in altri modi, il **BNS** creato in questo modo presenta il vantaggio di richiedere solo un'operazione di allocazione e una libera memoria per tutte le stringhe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Objidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Objidl. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





