---
description: La funzione CreatePropertyDatabase crea un database delle proprietà che archivia le proprietà di un protocollo.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Funzione CreatePropertyDatabase (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7c07f6f3e4569c06f0b3890e3ef3a26bca10b3272849fc005dfb3be6cbc2836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367218"
---
# <a name="createpropertydatabase-function"></a>Funzione CreatePropertyDatabase

La **funzione CreatePropertyDatabase** crea un database delle proprietà che archivia le proprietà di un protocollo.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ Pollici\]
</dt> <dd>

Handle del protocollo associato al database. Quando Network Monitor chiama la [funzione Register,](register-parser.md) Network Monitor passa l'handle di protocollo alla DLL del parser.

</dd> <dt>

*nProprietà* \[ Pollici\]
</dt> <dd>

Numero di proprietà archiviate nel database. Impostare questo parametro sul numero di proprietà supportate dal protocollo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                             | Descrizione                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE INTERNO DI \_ \_ NMERR**</dt> </dl>   | Si è verificato un errore interno.<br/>                                     |
| <dl> <dt>**\_HPOTOCOL NON VALIDO DI NMERR \_**</dt> </dl> | L'handle per il protocollo specificato in *hProtocol* non è valido.<br/>     |
| <dl> <dt>**MEMORIA INSUFFICIENTE \_ DI NMERR \_ \_**</dt> </dl>   | Network Monitor non dispone di memoria sufficiente per creare il database.<br/> |



 

## <a name="remarks"></a>Commenti

La **funzione CreatePropertyDatabase** deve essere chiamata solo quando si implementa la [funzione Register.](register-parser.md) Il parser usa **CreatePropertyDatabase per** creare un database delle proprietà che descrive le proprietà di un protocollo. Network Monitor usa il database per interpretare le informazioni all'interno del protocollo.

La **funzione CreatePropertyDatabase** alloca le strutture necessarie Network Monitor gestire un database delle proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Registra](register-parser.md)
</dt> </dl>

 

 




