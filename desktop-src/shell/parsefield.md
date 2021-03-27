---
description: Legge una riga dal file Setup. inf ed estrae il campo specificato dalla stringa.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Funzione ParseField (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232111"
---
# <a name="parsefield-function"></a>ParseField (funzione)

\[La funzione **ParseField** è attualmente prevista per l'utilizzo nella versione successiva del sistema operativo Microsoft Windows. Potrebbe essere modificato o non disponibile nelle versioni successive.\]

Legge una riga dal file Setup. inf ed estrae il campo specificato dalla stringa.

## <a name="syntax"></a>Sintassi


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szData* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR \** _

Puntatore alla riga da Setup. inf.

</dd> <dt>

_n * \[ in\]
</dt> <dd>

Tipo: **int**

**Int** che indica il campo da estrarre.

<dt>



  (0)


</dt> <dd>

Indica il campo prima di un segno di uguale (=).

</dd> <dt>



 (1)


</dt> <dd>

Indica il primo campo.

</dd> </dl> </dd> <dt>

*szBuf* \[ in\]
</dt> <dd>

Tipo: **LPTSTR \** _

Puntatore al buffer che riceve il campo Estratto.

</dd> <dt>

_iBufLen * \[ in\]
</dt> <dd>

Tipo: **int**

**Int** che riceve la dimensione del buffer che riceve il campo Estratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Restituisce **true** se la funzione ha esito positivo e **false** in caso di esito negativo.

## <a name="remarks"></a>Commenti

I campi nella stringa devono essere separati da virgole.

Gli spazi iniziali e finali vengono rimossi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Util. h</dt> </dl>                             |
| Libreria<br/>                  | <dl> <dt>Shell32. lib</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



 

 




