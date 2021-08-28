---
description: Elimina una condivisione DDE dal gestore del database di condivisione DDE.
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Funzione NDdeShareDel (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 0efd5bb41712e8bee2ee7a5e789d1b006a490c932b48386de27f56a8b1150f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611101"
---
# <a name="nddesharedel-function"></a>Funzione NDdeShareDel

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Elimina una condivisione DDE dal gestore del database di condivisione DDE.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Nome del server il cui DSDM deve essere modificato.

</dd> <dt>

*lpszShareName* \[ Pollici\]
</dt> <dd>

Nome della condivisione da eliminare da DSDM. Questo parametro non può essere **NULL.**

</dd> <dt>

*wReserved* \[ Pollici\]
</dt> <dd>

Riservato. Questo parametro deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è un codice di errore che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Commenti

Per eliminare una condivisione DDE da DSDM, è necessario disporre del privilegio appropriato. L'autore della condivisione ha il privilegio di eliminazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeShareDelW** (Unicode) e **NDdeShareDelA** (ANSI)<br/>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> </dl>

 

 




