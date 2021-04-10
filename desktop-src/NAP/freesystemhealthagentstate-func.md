---
title: Funzione FreeSystemHealthAgentState (NapUtil. h)
description: Libera una struttura di dati SystemHealthAgentState.
ms.assetid: e9bfa8ee-c335-416e-94cf-28646709d419
keywords:
- NAP funzione FreeSystemHealthAgentState
topic_type:
- apiref
api_name:
- FreeSystemHealthAgentState
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce59135de1c8f47d84a07f01dbb5f2bbe697f9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119407"
---
# <a name="freesystemhealthagentstate-function"></a>FreeSystemHealthAgentState (funzione)

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

La funzione **FreeSystemHealthAgentState** libera una struttura di dati [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) .

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeSystemHealthAgentState(
  _In_ SystemHealthAgentState *state
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*stato* \[ di in\]
</dt> <dd>

Puntatore alla struttura di dati [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) da liberare.

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



 

 





