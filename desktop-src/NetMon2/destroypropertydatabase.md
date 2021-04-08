---
description: La funzione DestroyPropertyDatabase rilascia le risorse usate per creare il database delle proprietà del protocollo.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Funzione DestroyPropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968391"
---
# <a name="destroypropertydatabase-function"></a>DestroyPropertyDatabase (funzione)

La funzione **DestroyPropertyDatabase** rilascia le risorse usate per creare il [*database delle proprietà*](p.md)del protocollo.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ in\]
</dt> <dd>

Handle per il database delle proprietà da eliminare definitivamente. L'handle viene passato alla DLL del parser quando Network Monitor chiama la funzione di [annullamento della registrazione](deregister.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                              | Descrizione                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_errore interno \_ NMERR**</dt> </dl>    | An internal error occurred. <br/>    |
| <dl> <dt>**\_HPROTOCOL NMERR non valido \_**</dt> </dl> | Handle non valido in *hProtocol*. <br/> |



 

## <a name="remarks"></a>Commenti

La funzione **DestroyPropertyDatabase** deve essere chiamata solo quando si implementa la funzione di esportazione di [annullamento della registrazione](deregister.md) per il protocollo. Per le dll del parser che supportano più protocolli, viene chiamata la funzione **DestroyPropertyDatabase** per ogni implementazione di **deregister**.



| Per informazioni su                                        | Vedere                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                 |
| I punti di ingresso inclusi nella DLL del parser.        | [Architettura DLL parser](parser-dll-architecture.md) |
| Come implementare la **Deregistrazione**  è incluso un esempio.     | [Implementazione della deregistrazione](implementing-deregister.md) |



 

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

[Annullamento registrazione](deregister.md)
</dt> </dl>

 

 




