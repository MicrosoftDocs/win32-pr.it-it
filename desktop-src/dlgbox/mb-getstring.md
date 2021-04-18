---
title: Funzione MB_GetString (User. h)
description: Restituisce le stringhe per i pulsanti standard della finestra di messaggio.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Finestre di dialogo MB_GetString funzione
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331573"
---
# <a name="mb_getstring-function"></a>MB- \_ funzione GetString

Restituisce le stringhe per i pulsanti standard della finestra di messaggio.

## <a name="syntax"></a>Sintassi


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wBtn* 
</dt> <dd>

ID della stringa da restituire. Sono identificati dai valori ID del comando della finestra di dialogo elencati in winuser. h.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa o NULL se non viene trovato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Utente. h</dt> </dl>     |
| Libreria<br/> | <dl> <dt>User32. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>User32.dll</dt> </dl> |



 

 





