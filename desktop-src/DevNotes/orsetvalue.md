---
description: Imposta i dati per il valore di una chiave del Registro di sistema specificata in un hive del Registro di sistema offline.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Funzione ORSetValue (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ae677a5dff2bcb7189b17c7d1477c95df5a5ae32b0065104b92e426e364d775d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749641"
---
# <a name="orsetvalue-function"></a>Funzione ORSetValue

Imposta i dati per il valore di una chiave del Registro di sistema specificata in un hive del Registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Handle* \[ Pollici\]
</dt> <dd>

Handle di una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.

</dd> <dt>

*lpValueName* \[ in, facoltativo\]
</dt> <dd>

Nome del valore da impostare. Se un valore con questo nome non è già presente nella chiave, la funzione lo aggiunge alla chiave.

Se *lpValueName* è **NULL** o una stringa vuota, "", la funzione imposta il tipo e i dati per il valore predefinito o senza nome della chiave.

Per altre informazioni, vedere [Limiti delle dimensioni degli elementi del Registro di sistema](../sysinfo/registry-element-size-limits.md).

Le chiavi del Registro di sistema non hanno valori predefiniti, ma possono avere un valore senza nome, che può essere di qualsiasi tipo.

</dd> <dt>

*dwType* \[ Pollici\]
</dt> <dd>

Tipo di dati a cui punta il *parametro lpData.* Per un elenco dei tipi possibili, vedere Tipi [di valori del Registro di sistema](../sysinfo/registry-value-types.md).

</dd> <dt>

*lpData* \[ in, facoltativo\]
</dt> <dd>

Dati da archiviare.

Per i tipi basati su stringa, ad esempio REG \_ SZ, la stringa deve essere con terminazione Null. Per il tipo di dati REG \_ MULTI \_ SZ, la stringa deve essere terminata con due caratteri Null.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Dimensione in byte delle informazioni a cui punta *il parametro lpData.* Se i dati sono di tipo REG \_ SZ, REG EXPAND SZ o \_ REG \_ MULTI \_ \_ SZ, *cbData* deve includere le dimensioni del carattere o dei caratteri Null di terminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore.

## <a name="remarks"></a>Commenti

Le dimensioni dei valori sono limitate dalla memoria disponibile. I valori long (più di 2048 byte) devono essere archiviati come file con i nomi di file archiviati nel Registro di sistema. Ciò consente al Registro di sistema di funzionare in modo efficiente. Gli elementi dell'applicazione, ad esempio icone, bitmap e file eseguibili, devono essere archiviati come file e non devono essere inseriti nel Registro di sistema.

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

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
