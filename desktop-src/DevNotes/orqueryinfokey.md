---
description: Recupera le informazioni sulla chiave del registro di sistema specificata in un hive del registro di sistema offline.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Funzione ORQueryInfoKey (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330426"
---
# <a name="orqueryinfokey-function"></a>ORQueryInfoKey (funzione)

Recupera le informazioni sulla chiave del registro di sistema specificata in un hive del registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*lpClass* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve la classe chiave. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che specifica la dimensione del buffer a cui punta il parametro *lpClass* , in caratteri.

La dimensione deve includere il carattere null di terminazione. Quando la funzione restituisce, questa variabile contiene le dimensioni della stringa di classe archiviata nel buffer. Il conteggio restituito non include il carattere null di terminazione. Se il buffer non è sufficientemente grande, la funzione restituisce l'errore \_ più \_ dati e la variabile contiene la dimensione della stringa, in caratteri, senza contare il carattere null di terminazione.

Se *lpClass* è **null**, *lpcClass* può essere **null**.

Se il parametro *lpClass* è un indirizzo valido, ma il parametro *lpcClass* non è (ad esempio, se il parametro *lpcClass* è **null**), la funzione restituisce l'errore \_ parametro non valido \_ .

</dd> <dt>

*lpcSubKeys* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di sottochiavi contenute nella chiave specificata. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcMaxSubKeyLen* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni della sottochiave della chiave con il nome più lungo, in caratteri Unicode, escluso il carattere null di terminazione. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcMaxClassLen* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve la dimensione della stringa più estesa che specifica una classe della sottochiave, in caratteri Unicode. Il conteggio restituito non include il carattere null di terminazione. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcValues* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di valori associati alla chiave. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcMaxValueNameLen* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni del nome più lungo del valore della chiave, in caratteri Unicode. La dimensione non include il carattere null di terminazione. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcMaxValueLen* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni del componente dati più lungo tra i valori della chiave, in byte. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni in byte del descrittore di sicurezza della chiave. Questo parametro può essere **NULL**.

</dd> <dt>

*lpftLastWriteTime* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che riceve l'ora dell'ultima scrittura. Questo parametro può essere **NULL**.

La funzione imposta i membri della struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) per indicare l'ultima modifica apportata alla chiave o a una delle relative voci di valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

Se il buffer *lpClass* è troppo piccolo per ricevere il nome della classe, la funzione restituisce l'errore di \_ altri \_ dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> </dl>

 

 
