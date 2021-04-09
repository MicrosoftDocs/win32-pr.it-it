---
title: Funzione FreeNapComponentRegistrationInfoArray (NapUtil. h)
description: Libera un numero specificato di strutture di dati NapComponentRegistrationInfo da una matrice.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- NAP funzione FreeNapComponentRegistrationInfoArray
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
ms.openlocfilehash: df823ad8086c57a6ee193bd0d58678786cfe325b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120930"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a>FreeNapComponentRegistrationInfoArray (funzione)

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

La funzione **FreeNapComponentRegistrationInfoArray** libera un numero specificato di strutture di dati [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) da una matrice.

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numero* \[ di in\]
</dt> <dd>

Numero di strutture [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) in *info* da liberare.

</dd> <dt>

*informazioni* \[ su in\]
</dt> <dd>

Puntatore a una matrice di strutture di dati [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) da liberare.

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



 

 





