---
description: Rimuove un valore denominato dalla chiave del Registro di sistema specificata in un hive del Registro di sistema offline.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Funzione ORDeleteValue (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 717464b1ba44593a9b36ccf26e5df248cb95df9bfa40a7786896c87041e246d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045291"
---
# <a name="ordeletevalue-function"></a>Funzione ORDeleteValue

Rimuove un valore denominato dalla chiave del Registro di sistema specificata in un hive del Registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
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

Valore del Registro di sistema da rimuovere. Se questo parametro è **NULL** o una stringa vuota, il valore senza nome predefinito impostato dalla funzione [**ORSetValue**](orsetvalue.md) viene rimosso.

Per i nomi dei valori non viene fatto distinzione tra maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria del Registro di sistema offline versione 1.0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 
