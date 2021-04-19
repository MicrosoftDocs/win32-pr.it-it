---
description: La funzione CreatePropertyDatabase crea un database delle proprietà in cui sono archiviate le proprietà di un protocollo.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Funzione CreatePropertyDatabase (Netmon. h)
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
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311628"
---
# <a name="createpropertydatabase-function"></a>CreatePropertyDatabase (funzione)

La funzione **CreatePropertyDatabase** crea un database delle proprietà in cui sono archiviate le proprietà di un protocollo.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ in\]
</dt> <dd>

Handle del protocollo associato al database. Quando Network Monitor chiama la funzione [Register](register-parser.md) , network monitor passa l'handle del protocollo alla DLL del parser.

</dd> <dt>

*nProperties* \[ in\]
</dt> <dd>

Numero di proprietà archiviate nel database. Impostare questo parametro sul numero di proprietà supportate dal protocollo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                             | Descrizione                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**\_errore interno \_ NMERR**</dt> </dl>   | Si è verificato un errore interno.<br/>                                     |
| <dl> <dt>**\_HPOTOCOL NMERR non valido \_**</dt> </dl> | L'handle per il protocollo specificato in *hProtocol* non è valido.<br/>     |
| <dl> <dt>**\_ \_ \_ memoria insufficiente NMERR**</dt> </dl>   | Network Monitor non dispone di memoria sufficiente per creare il database.<br/> |



 

## <a name="remarks"></a>Commenti

La funzione **CreatePropertyDatabase** deve essere chiamata solo quando si implementa la funzione [Register](register-parser.md) . Il parser USA **CreatePropertyDatabase** per creare un database di proprietà che descrive le proprietà di un protocollo. Network Monitor utilizza il database per interpretare le informazioni all'interno del protocollo.

La funzione **CreatePropertyDatabase** alloca le strutture che Network Monitor necessario per mantenere un database di proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Registra](register-parser.md)
</dt> </dl>

 

 




