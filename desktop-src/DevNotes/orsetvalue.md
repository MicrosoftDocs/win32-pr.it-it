---
description: Imposta i dati per il valore di una chiave del registro di sistema specificata in un hive del registro di sistema offline.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Funzione ORSetValue (offreg. h)
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
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332594"
---
# <a name="orsetvalue-function"></a>ORSetValue (funzione)

Imposta i dati per il valore di una chiave del registro di sistema specificata in un hive del registro di sistema offline.

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

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*lpValueName* \[ in, facoltativo\]
</dt> <dd>

Nome del valore da impostare. Se un valore con questo nome non è già presente nella chiave, la funzione lo aggiunge alla chiave.

Se *lpValueName* è **null** o una stringa vuota, "", la funzione imposta il tipo e i dati per il valore predefinito o senza nome della chiave.

Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).

Le chiavi del registro di sistema non hanno valori predefiniti, ma possono avere un valore senza nome, che può essere di qualsiasi tipo.

</dd> <dt>

*dwType* \[ in\]
</dt> <dd>

Tipo di dati a cui punta il parametro *lpData* . Per un elenco dei tipi possibili, vedere [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md).

</dd> <dt>

*lpData* \[ in, facoltativo\]
</dt> <dd>

Dati da archiviare.

Per i tipi basati su stringa, ad esempio REG \_ SZ, la stringa deve essere con terminazione null. Per il \_ tipo di \_ dati reg multisz, la stringa deve terminare con due caratteri null.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Dimensioni in byte delle informazioni a cui punta il parametro *lpData* . Se i dati sono di tipo REG \_ SZ, reg \_ expand \_ sz o reg \_ \_ multisz, *cbData* deve includere la dimensione del carattere null di terminazione o caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

## <a name="remarks"></a>Commenti

Le dimensioni dei valori sono limitate dalla memoria disponibile. I valori Long (più di 2048 byte) devono essere archiviati come file con i nomi di file archiviati nel registro di sistema. Ciò consente di eseguire in modo efficiente il registro di sistema. Gli elementi dell'applicazione quali le icone, le bitmap e i file eseguibili devono essere archiviati come file e non devono essere inseriti nel registro di sistema.

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

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
