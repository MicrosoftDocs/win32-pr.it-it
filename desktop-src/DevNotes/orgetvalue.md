---
description: Recupera il tipo e i dati per il valore del registro di sistema specificato in un hive del registro di sistema offline.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Funzione ORGetValue (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328367"
---
# <a name="orgetvalue-function"></a>ORGetValue (funzione)

Recupera il tipo e i dati per il valore del registro di sistema specificato in un hive del registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*lpSubKey* \[ in, facoltativo\]
</dt> <dd>

Nome della chiave del Registro di sistema. Questa chiave deve essere una sottochiave della chiave specificata dal parametro *handle* . Questo parametro può essere **NULL**.

Per i nomi di chiave non viene fatta distinzione tra maiuscole

</dd> <dt>

*lpValue* \[ in, facoltativo\]
</dt> <dd>

Nome del valore del registro di sistema. Se questo parametro è **null** o una stringa vuota, "", la funzione recupera il tipo e i dati per il valore predefinito o senza nome della chiave, se disponibile. Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).

Le chiavi non dispongono automaticamente di un valore senza nome o predefinito. I valori senza nome possono essere di qualsiasi tipo.

Per i nomi di valore non viene fatta distinzione tra maiuscole

</dd> <dt>

*pdwType* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve un codice che indica il tipo di dati archiviati nel valore specificato. Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md). Questo parametro può essere **null** se il tipo non è obbligatorio.

</dd> <dt>

*pvData* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve i dati del valore. Questo parametro può essere **null** se i dati non sono obbligatori.

Se i dati sono di tipo stringa, la funzione verifica la presenza di un carattere null di terminazione. Se non viene trovato, la stringa viene archiviata con un terminatore null se il buffer è sufficientemente grande da contenere il carattere aggiuntivo. In caso contrario, la funzione ha esito negativo e restituisce l'errore \_ più \_ dati.

</dd> <dt>

*pcbData* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che specifica le dimensioni in byte del buffer a cui punta il parametro *pvData* . Quando la funzione restituisce, questa variabile contiene le dimensioni dei dati copiati in *pvData*.

Il parametro *pcbData* può essere **null** solo se *pvData* è **null**.

Se i dati sono di \_ tipo reg SZ, \_ reg \_ multisz o reg \_ expand \_ SZ, questa dimensione include i caratteri null o i caratteri di terminazione. Per altre informazioni, vedere la sezione Osservazioni.

Se il buffer specificato dal parametro *pvData* non è sufficientemente grande da consentire l'archiviazione dei dati, la funzione restituisce \_ più dati di errore \_ e archivia le dimensioni del buffer richieste nella variabile a cui punta *pcbData*. In questo caso, il contenuto del buffer *pvData* non è definito.

Se *pvData* è **null** e *pcbData* è diverso da **null**, la funzione restituisce Error \_ Success e archivia le dimensioni dei dati, in byte, nella variabile a cui punta *pcbData*. Questo consente a un'applicazione di determinare il modo migliore per allocare un buffer per i dati del valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

## <a name="remarks"></a>Commenti

Un'applicazione in genere chiama la funzione [**OREnumValue**](orenumvalue.md) per determinare i nomi dei valori e quindi chiama la funzione **ORGetValue** per recuperare i dati per i nomi.

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

[**OREnumValue**](orenumvalue.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
