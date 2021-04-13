---
title: Funzione FreeConnections (NapUtil. h)
description: Libera una struttura dei dati delle connessioni.
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- NAP funzione FreeConnections
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
ms.openlocfilehash: 2f840d02572af3e6382a06a1873573fc7a30420e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340393"
---
# <a name="freeconnections-function"></a>FreeConnections (funzione)

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

La funzione **FreeConnections** libera una struttura di dati [**Connections**](connections-struct.md) .

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessioni* \[ di in\]
</dt> <dd>

Puntatore alla struttura [**Connections**](connections-struct.md) da liberare.

</dd> </dl>

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

[**AllocConnections**](allocconnections-func.md)
</dt> </dl>

 

 





