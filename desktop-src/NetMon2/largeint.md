---
description: Il tipo di dati LARGEINT definisce un valore LARGE \_ INTEGER.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (Netmon.h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6eedf739d9d0b4285d0198ae905672dbbb7848a2b7d9ba106abb6a59fcdc4d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742651"
---
# <a name="largeint"></a>LARGEINT

Il **tipo di dati LARGEINT** definisce un valore [**LARGE \_**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) INTEGER.


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>Commenti

Il **membro lpLargeIntTable** della struttura [**SET**](set.md) punta a una matrice di strutture **SET** che definiscono uno o più valori LARGEINT. Quando si specifica questo tipo di struttura **SET,** Network Monitor visualizza una delle etichette seguenti con ogni valore LARGEINT trovato nel pacchetto del protocollo.

-   Corrisponde al valore impostato. Il valore LARGEINT è incluso nel set.
-   Valore impostato sconosciuto. Il valore LARGEINT non è incluso nel set.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

