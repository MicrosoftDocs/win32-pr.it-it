---
description: La funzione LoadStringAddr trasforma una stringa (ad esempio &\# 0034; 157.54.32.45&\# 0034;) e crea un indirizzo DWORD.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: Funzione LoadStringAddr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307723"
---
# <a name="loadstringaddr-function"></a>LoadStringAddr (funzione)

La funzione **LoadStringAddr** trasforma una stringa (ad esempio "157.54.32.45") e crea un indirizzo **DWORD** .

## <a name="syntax"></a>Sintassi


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAddress* 
</dt> <dd>

Puntatore a un **valore DWORD**.

</dd> <dt>

*str* 
</dt> <dd>

Puntatore a una stringa di caratteri con rappresentazione x. x.x. x di un indirizzo IP (ad esempio, 127.0.0.1).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (il nome dell'indirizzo è stato trovato); il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




