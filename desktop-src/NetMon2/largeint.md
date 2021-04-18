---
description: Il tipo di dati LARGEINT definisce un \_ valore Integer grande.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (Netmon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302766"
---
# <a name="largeint"></a>LARGEINT

Il tipo di dati **largeInt** definisce un valore [**\_ Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) .


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>Commenti

Il membro **lpLargeIntTable** della struttura del [**set**](set.md) punta a una matrice di strutture **set** che definiscono uno o più valori LARGEINT. Quando questo tipo di struttura **set** viene specificato, Network Monitor visualizza una delle etichette seguenti con ogni valore largeInt trovato nel pacchetto del protocollo.

-   Corrisponde al valore impostato. Il valore LARGEINT è incluso nel set.
-   Valore impostato sconosciuto. Il valore LARGEINT non è incluso nel set.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

