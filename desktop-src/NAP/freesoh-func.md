---
title: Funzione FreeSoH (NapUtil.h)
description: Libera una struttura di dati SoH.
ms.assetid: 587acf64-31be-46c8-9d49-b5014c1a90ba
keywords:
- Funzione FreeSoH nap
topic_type:
- apiref
api_name:
- FreeSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7e8236fcc8f0a2eaadd5b6f2ef81a393d68943d7fc5aeac5b00706ea06ec26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368683"
---
# <a name="freesoh-function"></a>Funzione FreeSoH

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione FreeSoH** libera una **struttura di dati SoH.**

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeSoH(
  _In_ SoH *soh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*soh* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura di dati SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) da liberare.

</dd> </dl>

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



 

 





