---
description: Crea un hive del registro di sistema offline che contiene una singola chiave radice vuota.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Funzione ORCreateHive (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331958"
---
# <a name="orcreatehive-function"></a>ORCreateHive (funzione)

Crea un hive del registro di sistema offline che contiene una singola chiave radice vuota.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phkResult* \[ out\]
</dt> <dd>

Punta a una variabile per ricevere un handle per la chiave radice dell'hive del registro di sistema offline appena creato. Se non è possibile creare l'hive, la funzione imposta questo parametro su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

Se la memoria disponibile non è sufficiente per creare l'hive del registro di sistema, la funzione restituisce un errore di \_ \_ memoria insufficiente \_ .

## <a name="remarks"></a>Commenti

La funzione **ORCreateHive** crea un hive del registro di sistema offline vuoto in memoria. Usare le funzioni [**ORCreateKey**](orcreatekey.md) e [**ORSetValue**](orsetvalue.md) per aggiungere chiavi e impostare i relativi valori.

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

[**OROpenHive**](oropenhive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 
