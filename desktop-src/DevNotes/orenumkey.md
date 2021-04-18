---
description: Enumera le sottochiavi della chiave del registro di sistema aperta specificata in un hive del registro di sistema offline. La funzione recupera le informazioni su una sottochiave ogni volta che viene chiamata.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Funzione OREnumKey (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330864"
---
# <a name="orenumkey-function"></a>OREnumKey (funzione)

Enumera le sottochiavi della chiave del registro di sistema aperta specificata in un hive del registro di sistema offline. La funzione recupera le informazioni su una sottochiave ogni volta che viene chiamata.

## <a name="syntax"></a>Sintassi


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Indice della sottochiave da recuperare. Questo parametro deve essere zero per la prima chiamata alla funzione e quindi incrementato per le chiamate successive.

Poiché le sottochiavi non sono ordinate, qualsiasi nuova sottochiave avrà un indice arbitrario. Ciò significa che la funzione può restituire sottochiavi in qualsiasi ordine.

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve il nome della sottochiave, incluso il carattere null di terminazione. La funzione copia nel buffer solo il nome della sottochiave, non la gerarchia di chiavi completa. Se la funzione ha esito negativo, nessuna informazione viene copiata in questo buffer.

Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcName* \[ in uscita\]
</dt> <dd>

Puntatore a una variabile che specifica la dimensione del buffer specificato dal parametro *lpName* in **WCHAR**. Questa dimensione deve includere il carattere null di terminazione. Se la funzione ha esito positivo, la variabile a cui punta *lpcName* contiene il numero di caratteri archiviati nel buffer, escluso il carattere null di terminazione.

</dd> <dt>

*lpClass* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve la stringa di classe con terminazione null della sottochiave enumerata. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che specifica la dimensione del buffer specificato dal parametro *lpClass* in **WCHAR**. La dimensione deve includere il carattere null di terminazione. Se la funzione ha esito positivo, *lpcClass* contiene il numero di caratteri archiviati nel buffer, escluso il carattere null di terminazione. Questo parametro può essere **null** solo se *lpClass* è **null**.

</dd> <dt>

*lpftLastWriteTime* \[ out, facoltativo\]
</dt> <dd>

Puntatore alla struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che riceve l'ora dell'ultima scrittura della sottochiave enumerata. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag. I codici di errore possibili includono i seguenti:

-   Se il buffer *lpName* è troppo piccolo per ricevere il nome della chiave, la funzione restituisce l'errore di \_ altri \_ dati.
-   Se non sono disponibili altre sottochiavi, la funzione restituisce l'errore \_ non \_ più \_ elementi.

## <a name="remarks"></a>Commenti

Per enumerare le sottochiavi, un'applicazione deve chiamare inizialmente la funzione **OREnumKey** con il parametro *dwIndex* impostato su zero. L'applicazione deve quindi incrementare il parametro *dwIndex* e chiamare **OREnumKey** fino a quando non sono presenti altre sottochiavi, ovvero la funzione restituisce \_ un errore non \_ più \_ elementi.

L'applicazione può anche impostare *dwIndex* sull'indice dell'ultima sottochiave nella prima chiamata alla funzione e decrementare l'indice fino a quando non viene enumerata la sottochiave con indice 0. Per recuperare l'indice dell'ultima sottochiave, usare la funzione [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) .

Mentre un'applicazione utilizza la funzione **OREnumKey** , non deve effettuare chiamate a funzioni del registro di sistema non in linea che potrebbero modificare la chiave enumerata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
