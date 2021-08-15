---
title: Funzione AllocConnections (NapUtil.h)
description: Alloca memoria per un numero specificato di strutture Connections.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- Funzione AllocConnections nap
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
ms.openlocfilehash: cf86a44b81ef12234fdac675aa55d36c5e1a336b4316382c3fd322cf0d6ba87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800208"
---
# <a name="allocconnections-function"></a>Funzione AllocConnections

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione AllocConnections** alloca memoria per un numero specificato di [**strutture Connections.**](connections-struct.md)

## <a name="syntax"></a>Sintassi


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessioni* \[ in, out\]
</dt> <dd>

Puntatore a una matrice di strutture [**Connections**](connections-struct.md) appena allocate.

</dd> <dt>

*connectionsCount* \[ Pollici\]
</dt> <dd>

Numero di strutture da allocare alle *connessioni*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                                   | Descrizione                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | L'operazione è stata completata correttamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | È stato passato un argomento non valido.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria virtuale del sistema è insufficiente. L'operazione non è riuscita.<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le interfacce COM supportate dal sistema nap usano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **I** parametri in vengono allocati e liberati dal chiamante.
-   **I** parametri out vengono allocati dal chiamato e liberati dal chiamante usando **CoTaskMem**.
-   **I parametri in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.

Tutte le funzioni di Protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FreeConnections**](freeconnections-func.md)
</dt> </dl>

 

 





