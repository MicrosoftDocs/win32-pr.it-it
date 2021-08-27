---
description: Recupera il tipo e i dati per il valore del Registro di sistema specificato in un hive del Registro di sistema offline.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Funzione ORGetValue (Offreg.h)
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
ms.openlocfilehash: fc364e208e9c243754edf8731f077ec48e9133d4a95ba86b5a1f99971192b51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058651"
---
# <a name="orgetvalue-function"></a>Funzione ORGetValue

Recupera il tipo e i dati per il valore del Registro di sistema specificato in un hive del Registro di sistema offline.

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

*Handle* \[ Pollici\]
</dt> <dd>

Handle di una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.

</dd> <dt>

*lpSubKey* \[ in, facoltativo\]
</dt> <dd>

Nome della chiave del Registro di sistema. Questa chiave deve essere una sottochiave della chiave specificata dal *parametro Handle.* Questo parametro può essere **NULL**.

Per i nomi delle chiavi non viene fatto distinzione tra maiuscole e minuscole.

</dd> <dt>

*lpValue* \[ in, facoltativo\]
</dt> <dd>

Nome del valore del Registro di sistema. Se questo parametro è **NULL** o una stringa vuota, "", la funzione recupera il tipo e i dati per il valore senza nome o predefinito della chiave, se presente. Per altre informazioni, vedere [Limiti delle dimensioni degli elementi del Registro di sistema](../sysinfo/registry-element-size-limits.md).

Le chiavi non hanno automaticamente un valore senza nome o predefinito. I valori senza nome possono essere di qualsiasi tipo.

Per i nomi dei valori non viene fatto distinzione tra maiuscole e minuscole.

</dd> <dt>

*pdwType* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve un codice che indica il tipo di dati archiviati nel valore specificato. Per un elenco dei codici di tipo possibili, vedere Tipi [di valori del Registro di sistema](../sysinfo/registry-value-types.md). Questo parametro può essere **NULL** se il tipo non è obbligatorio.

</dd> <dt>

*pvData* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve i dati del valore. Questo parametro può essere **NULL** se i dati non sono necessari.

Se i dati sono una stringa, la funzione verifica la presenza di un carattere Null di terminazione. Se non ne viene trovato uno, la stringa viene archiviata con un carattere di terminazione Null se il buffer è sufficientemente grande da contenere il carattere aggiuntivo. In caso contrario, la funzione ha esito negativo e restituisce ERROR \_ MORE \_ DATA.

</dd> <dt>

*pcbData* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che specifica le dimensioni del buffer a cui punta il *parametro pvData,* in byte. Quando la funzione viene restituita, questa variabile contiene le dimensioni dei dati copiati in *pvData*.

Il *parametro pcbData* può essere **NULL solo** se *pvData* è **NULL.**

Se i dati hanno il tipo REG SZ, REG MULTI SZ o REG EXPAND SZ, questa dimensione include qualsiasi carattere o carattere \_ \_ Null di \_ \_ \_ terminazione. Per altre informazioni, vedere la sezione Osservazioni.

Se il buffer specificato dal *parametro pvData* non è sufficientemente grande per contenere i dati, la funzione restituisce ERROR MORE DATA e archivia le dimensioni del buffer richieste nella variabile a cui punta \_ \_ *pcbData*. In questo caso, il contenuto del buffer *pvData* non è definito.

Se *pvData* è **NULL** e *pcbData* è diverso da **NULL,** la funzione restituisce ERROR SUCCESS e archivia le dimensioni dei dati, in byte, nella variabile a cui punta \_ *pcbData*. Ciò consente a un'applicazione di determinare il modo migliore per allocare un buffer per i dati del valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore.

## <a name="remarks"></a>Commenti

Un'applicazione chiama in genere la [**funzione OREnumValue**](orenumvalue.md) per determinare i nomi dei valori e quindi chiama la **funzione ORGetValue** per recuperare i dati per i nomi.

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

[**OREnumValue**](orenumvalue.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
