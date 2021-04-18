---
title: Funzione FreeIsolationInfo (NapUtil. h)
description: Libera una struttura di dati IsolationInfo.
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- NAP funzione FreeIsolationInfo
topic_type:
- apiref
api_name:
- FreeIsolationInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ed154d35b32edab0f1a68d84f78c10cfd1cfe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302260"
---
# <a name="freeisolationinfo-function"></a>FreeIsolationInfo (funzione)

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

La funzione **FreeIsolationInfo** libera una struttura di dati [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) .

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ in\]
</dt> <dd>

Puntatore alla struttura di dati [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) da liberare.

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



 

 





