---
title: Funzione AllocConnections (NapUtil. h)
description: Alloca memoria per un numero specificato di strutture di connessione.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- NAP funzione AllocConnections
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e29521d2fea6eec3765a3a34210b896f1baa4db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743898"
---
# <a name="allocconnections-function"></a>AllocConnections (funzione)

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

La funzione **AllocConnections** alloca memoria per un numero specificato di strutture di [**connessione**](connections-struct.md) .

## <a name="syntax"></a>Sintassi


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessioni* \[ di in uscita\]
</dt> <dd>

Puntatore a una matrice di strutture di [**connessioni**](connections-struct.md) appena allocate.

</dd> <dt>

*connectionsCount* \[ in\]
</dt> <dd>

Numero di strutture da allocare alle *connessioni*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                                   | Descrizione                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L'operazione è stata completata correttamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | È stato passato un argomento non valido.<br/>                                 |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria virtuale insufficiente nel sistema. Operazione non riuscita.<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   I parametri **in** vengono allocati e liberati dal chiamante.
-   I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.
-   I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.

Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FreeConnections**](freeconnections-func.md)
</dt> </dl>

 

 





