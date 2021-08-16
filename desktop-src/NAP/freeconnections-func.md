---
title: Funzione FreeConnections (NapUtil.h)
description: Libera una struttura di dati Connections.
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- Funzione FreeConnections NAP
topic_type:
- apiref
api_name:
- FreeConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258295df0b12f30d98825dd139eb51a7d1bc277417cf4d06bba9e811a00740db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940638"
---
# <a name="freeconnections-function"></a>Funzione FreeConnections

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione FreeConnections** libera una [**struttura di dati Connections.**](connections-struct.md)

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessioni* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura Connections**](connections-struct.md) da liberare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutte le interfacce COM supportate dal sistema nap usano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **In** i parametri vengono allocati e liberati dal chiamante.
-   **I** parametri out vengono allocati dal chiamato e liberati dal chiamante usando **CoTaskMem.**
-   **I parametri in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem.**

Tutte le funzioni di Protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AllocConnections**](allocconnections-func.md)
</dt> </dl>

 

 





