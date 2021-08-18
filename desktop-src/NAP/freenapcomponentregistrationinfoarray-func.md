---
title: Funzione FreeNapComponentRegistrationInfoArray (NapUtil.h)
description: Libera un numero specificato di strutture di dati NapComponentRegistrationInfo da una matrice.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- Funzione FreeNapComponentRegistrationInfoArray NAP
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d9d1aba35e7bf1ef332231836bd986b881f0e2dc995bc430075dfadf7bd482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940499"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a>Funzione FreeNapComponentRegistrationInfoArray

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione FreeNapComponentRegistrationInfoArray** libera un numero specificato di strutture di dati [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) da una matrice.

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*count* \[ Pollici\]
</dt> <dd>

Numero di [**strutture NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) nelle *informazioni* da liberare.

</dd> <dt>

*info* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di strutture di dati [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) da liberare.

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



 

 





