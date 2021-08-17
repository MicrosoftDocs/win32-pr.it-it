---
title: Funzione FreeIsolationInfo (NapUtil.h)
description: Libera una struttura di dati IsolationInfo.
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- Funzione FreeIsolationInfo nap
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
ms.openlocfilehash: 031fd49bbdda7c0b36481776ba3c9dca8ea6d1c236b0010ada319b9a51f989df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940648"
---
# <a name="freeisolationinfo-function"></a>Funzione FreeIsolationInfo

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione FreeIsolationInfo** libera una [**struttura di dati IsolationInfo.**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo)

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura di dati IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) da liberare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutte le interfacce COM supportate dal sistema di Protezione accesso alla rete usano regole di gestione della memoria COM standard e allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

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



 

 





