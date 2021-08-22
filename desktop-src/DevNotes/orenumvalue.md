---
description: Enumera i valori per la chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline. La funzione recupera le informazioni per un valore sotto la chiave specificata ogni volta che viene chiamata la funzione.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Funzione OREnumValue (Offreg.h)
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
ms.openlocfilehash: 57a65e8fd862215bd6281e487520857580cf6026b94b2ca375079f84407e4cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331802"
---
# <a name="orenumvalue-function"></a>Funzione OREnumValue

Enumera i valori per la chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline. La funzione recupera le informazioni per un valore sotto la chiave specificata ogni volta che viene chiamata la funzione.

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

*Handle* \[ Pollici\]
</dt> <dd>

Handle per una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.

</dd> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

Indice del valore da recuperare. Questo parametro deve essere zero per la prima chiamata alla funzione e quindi essere incrementato per le chiamate successive.

Poiché i valori non sono ordinati, qualsiasi nuovo valore avrà un indice arbitrario. Ciò significa che la funzione può restituire valori in qualsiasi ordine.

</dd> <dt>

*lpValueName* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve il nome del valore come stringa con terminazione Null. Questo buffer deve essere sufficientemente grande da includere il carattere Null di terminazione.

Per altre informazioni, vedere [Limiti delle dimensioni degli elementi del Registro di sistema.](../sysinfo/registry-element-size-limits.md)

</dd> <dt>

*lpcValueName* \[ in, out\]
</dt> <dd>

Puntatore a una variabile che specifica le dimensioni del buffer a cui punta il *parametro lpValueName,* in caratteri. Quando la funzione termina, la variabile riceve il numero di caratteri archiviati nel buffer, senza includere il carattere Null di terminazione.

</dd> <dt>

*lpType* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve un codice che indica il tipo di dati archiviati nel valore specificato. Per un elenco dei codici di tipo possibili, vedere Tipi [di valori del Registro di sistema.](../sysinfo/registry-value-types.md) Il *parametro lpType* può essere **NULL se** il codice del tipo non è obbligatorio.

</dd> <dt>

*lpData* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve i dati per la voce di valore. Questo parametro può essere **NULL** se i dati non sono necessari.

Se *lpData* è **NULL** e *lpcbData* è diverso da **NULL,** la funzione archivia le dimensioni dei dati, in byte, nella variabile a cui punta *lpcbData*. Ciò consente a un'applicazione di determinare il modo migliore per allocare un buffer per i dati.

</dd> <dt>

*lpcbData* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che specifica le dimensioni del buffer a cui punta il *parametro lpData,* in byte. Quando la funzione viene restituita, la variabile riceve il numero di byte archiviati nel buffer.

Questo parametro può essere **NULL** solo se *lpData* è **NULL.**

Se i dati hanno il tipo REG SZ, REG MULTI SZ o REG EXPAND SZ, questa dimensione include qualsiasi carattere o carattere \_ \_ Null di \_ \_ \_ terminazione. Per altre informazioni, vedere la sezione Osservazioni.

Se il buffer specificato da *lpData* non è sufficientemente grande da contenere i dati, la funzione restituisce ERROR MORE DATA e archivia le dimensioni del buffer richieste nella variabile a cui \_ \_ punta *lpcbData*. In questo caso, il contenuto di *lpData* non è definito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore.

Se il buffer *lpData* è troppo piccolo per ricevere il valore, la funzione restituisce ERROR \_ MORE \_ DATA.

## <a name="remarks"></a>Commenti

Per enumerare i valori, un'applicazione deve chiamare inizialmente la **funzione OREnumValue** con *il parametro dwIndex* impostato su zero. L'applicazione deve quindi *incrementare dwIndex* e chiamare la funzione **OREnumValue** finché non sono presenti altri valori (fino a quando la funzione non restituisce ERROR \_ NO MORE \_ \_ ITEMS).

L'applicazione può anche impostare *dwIndex* sull'indice dell'ultimo valore alla prima chiamata alla funzione e decrementare l'indice fino a quando non viene enumerato il valore con indice 0. Per recuperare l'indice dell'ultimo valore, usare la [**funzione ORQueryInfoKey.**](orqueryinfokey.md)

Quando si **usa OREnumValue**, un'applicazione non deve chiamare funzioni del Registro di sistema offline che potrebbero modificare la chiave su cui viene eseguita la query.

Se i dati sono di tipo REG SZ, REG MULTI SZ o REG EXPAND SZ, è possibile che la stringa non sia stata archiviata con i caratteri di \_ \_ \_ \_ \_ terminazione Null propri. Pertanto, anche se la funzione restituisce ERROR SUCCESS, l'applicazione deve assicurarsi che la stringa venga terminata correttamente prima di usarla. In caso contrario, potrebbe \_ sovrascrivere un buffer. Si noti che REG \_ Le \_ stringhe MULTI SZ devono contenere due caratteri di terminazione Null.

Per determinare la dimensione massima del nome e dei buffer di dati, usare la [**funzione ORQueryInfoKey.**](orqueryinfokey.md)

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
