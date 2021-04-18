---
description: Enumera i valori per la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline. La funzione recupera le informazioni per un valore sotto la chiave specificata ogni volta che viene chiamata la funzione.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Funzione OREnumValue (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328369"
---
# <a name="orenumvalue-function"></a>OREnumValue (funzione)

Enumera i valori per la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline. La funzione recupera le informazioni per un valore sotto la chiave specificata ogni volta che viene chiamata la funzione.

## <a name="syntax"></a>Sintassi


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
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

Indice del valore da recuperare. Questo parametro deve essere zero per la prima chiamata alla funzione e quindi essere incrementato per le chiamate successive.

Poiché i valori non sono ordinati, qualsiasi nuovo valore avrà un indice arbitrario. Ciò significa che la funzione può restituire valori in qualsiasi ordine.

</dd> <dt>

*lpValueName* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve il nome del valore come stringa con terminazione null. Questo buffer deve essere sufficientemente grande da includere il carattere null di terminazione.

Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcValueName* \[ in uscita\]
</dt> <dd>

Puntatore a una variabile che specifica la dimensione del buffer a cui punta il parametro *lpValueName* , in caratteri. Quando la funzione restituisce, la variabile riceve il numero di caratteri archiviati nel buffer, escluso il carattere di terminazione null.

</dd> <dt>

*lpType* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve un codice che indica il tipo di dati archiviati nel valore specificato. Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md). Il parametro *lpType* può essere **null** se il codice di tipo non è obbligatorio.

</dd> <dt>

*lpData* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve i dati per la voce del valore. Questo parametro può essere **null** se i dati non sono obbligatori.

Se *lpData* è **null** e *lpcbData* è diverso da **null**, la funzione archivia le dimensioni dei dati, in byte, nella variabile a cui punta *lpcbData*. Questo consente a un'applicazione di determinare il modo migliore per allocare un buffer per i dati.

</dd> <dt>

*lpcbData* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che specifica le dimensioni in byte del buffer a cui punta il parametro *lpData* . Quando la funzione restituisce, la variabile riceve il numero di byte archiviati nel buffer.

Questo parametro può essere **null** solo se *lpData* è **null**.

Se i dati sono di \_ tipo reg SZ, \_ reg \_ multisz o reg \_ expand \_ SZ, questa dimensione include i caratteri null o i caratteri di terminazione. Per altre informazioni, vedere la sezione Osservazioni.

Se il buffer specificato da *lpData* non è sufficientemente grande da consentire l'archiviazione dei dati, la funzione restituisce \_ più dati di errore \_ e archivia le dimensioni del buffer richieste nella variabile a cui punta *lpcbData*. In questo caso, il contenuto di *lpData* non è definito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

Se il buffer *lpData* è troppo piccolo per ricevere il valore, la funzione restituisce un errore di \_ altri \_ dati.

## <a name="remarks"></a>Commenti

Per enumerare i valori, un'applicazione deve chiamare inizialmente la funzione **OREnumValue** con il parametro *dwIndex* impostato su zero. L'applicazione deve quindi incrementare *dwIndex* e chiamare la funzione **OREnumValue** fino a quando non sono presenti altri valori (fino a quando la funzione \_ non restituisce \_ più \_ elementi).

L'applicazione può inoltre impostare *dwIndex* sull'indice dell'ultimo valore nella prima chiamata alla funzione e decrementare l'indice fino a quando non viene enumerato il valore con indice 0. Per recuperare l'indice dell'ultimo valore, utilizzare la funzione [**ORQueryInfoKey**](orqueryinfokey.md) .

Quando si usa **OREnumValue**, un'applicazione non deve chiamare funzioni del registro di sistema offline che potrebbero modificare la chiave sottoposta a query.

Se i dati sono di \_ tipo reg SZ, \_ reg \_ multisz o reg \_ expand \_ SZ, è possibile che la stringa non sia stata archiviata con i caratteri di terminazione null appropriati. Pertanto, anche se la funzione restituisce un errore di \_ esito positivo, l'applicazione deve garantire che la stringa venga terminata correttamente prima di utilizzarla; in caso contrario, potrebbe sovrascrivere un buffer. (Si noti che REG \_ Le \_ stringhe a più SZ devono avere due caratteri di terminazione null.

Per determinare la dimensione massima del nome e dei buffer dei dati, utilizzare la funzione [**ORQueryInfoKey**](orqueryinfokey.md) .

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
