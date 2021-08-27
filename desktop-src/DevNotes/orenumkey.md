---
description: Enumera le sottochiavi della chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline. La funzione recupera informazioni su una sottochiave ogni volta che viene chiamata.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Funzione OREnumKey (Offreg.h)
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
ms.openlocfilehash: ab72c9b0df79d464f802a1c574b749d04a8a16e89645f25959681e7f03eea5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058711"
---
# <a name="orenumkey-function"></a>FUNZIONE OREnumKey

Enumera le sottochiavi della chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline. La funzione recupera informazioni su una sottochiave ogni volta che viene chiamata.

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

*Handle* \[ Pollici\]
</dt> <dd>

Handle per una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.

</dd> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

Indice della sottochiave da recuperare. Questo parametro deve essere zero per la prima chiamata alla funzione e quindi incrementato per le chiamate successive.

Poiché le sottochiavi non vengono ordinate, qualsiasi nuova sottochiave avrà un indice arbitrario. Ciò significa che la funzione può restituire sottochiavi in qualsiasi ordine.

</dd> <dt>

*lpName* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve il nome della sottochiave, incluso il carattere Null di terminazione. La funzione copia solo il nome della sottochiave, non la gerarchia di chiavi completa, nel buffer. Se la funzione ha esito negativo, non viene copiata alcuna informazione in questo buffer.

Per altre informazioni, vedere [Limiti delle dimensioni degli elementi del Registro di sistema.](../sysinfo/registry-element-size-limits.md)

</dd> <dt>

*lpcName* \[ in, out\]
</dt> <dd>

Puntatore a una variabile che specifica le dimensioni del buffer specificato dal *parametro lpName,* in **WCHAR.** Questa dimensione deve includere il carattere null di terminazione. Se la funzione ha esito positivo, la variabile a cui punta *lpcName* contiene il numero di caratteri archiviati nel buffer, senza includere il carattere Null di terminazione.

</dd> <dt>

*lpClass* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve la stringa di classe con terminazione Null della sottochiave enumerata. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che specifica le dimensioni del buffer specificato dal *parametro lpClass,* in **WCHAR.** La dimensione deve includere il carattere Null di terminazione. Se la funzione ha esito positivo, *lpcClass* contiene il numero di caratteri archiviati nel buffer, senza includere il carattere Null di terminazione. Questo parametro può essere **NULL** solo se *lpClass* è **NULL.**

</dd> <dt>

*lpftLastWriteTime* \[ out, facoltativo\]
</dt> <dd>

Puntatore alla [struttura FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che riceve l'ora dell'ultima scrittura della sottochiave enumerata. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore. I codici di errore possibili sono i seguenti:

-   Se il buffer *lpName* è troppo piccolo per ricevere il nome della chiave, la funzione restituisce ERROR \_ MORE \_ DATA.
-   Se non sono disponibili altre sottochiavi, la funzione restituisce ERROR \_ NO \_ MORE \_ ITEMS.

## <a name="remarks"></a>Commenti

Per enumerare le sottochiavi, un'applicazione deve chiamare inizialmente la **funzione OREnumKey** con *il parametro dwIndex* impostato su zero. L'applicazione deve quindi incrementare il *parametro dwIndex* e chiamare **OREnumKey** finché non sono presenti altre sottochiavi, ovvero la funzione restituisce ERROR \_ NO MORE \_ \_ ITEMS.

L'applicazione può anche impostare *dwIndex* sull'indice dell'ultima sottochiave alla prima chiamata alla funzione e decrementare l'indice fino a quando non viene enumerata la sottochiave con l'indice 0. Per recuperare l'indice dell'ultima sottochiave, usare la [**funzione ORQueryInfoKey.**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya)

Mentre un'applicazione usa la **funzione OREnumKey,** non deve effettuare chiamate a funzioni del Registro di sistema offline che potrebbero modificare la chiave enumerata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria del Registro di sistema offline versione 1.0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
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

 

 
