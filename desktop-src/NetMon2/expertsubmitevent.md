---
description: La funzione ExpertSubmitEvent indica che esiste una condizione dell'evento e fornisce una struttura di dati che descrive la condizione.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Funzione ExpertSubmitEvent (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342761"
---
# <a name="expertsubmitevent-function"></a>ExpertSubmitEvent (funzione)

La funzione **ExpertSubmitEvent** indica che esiste una condizione dell'evento e fornisce una struttura di dati che descrive la condizione.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ in\]
</dt> <dd>

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .

</dd> <dt>

*pExpertEvent* \[ in\]
</dt> <dd>

Puntatore a una struttura **NMEVENTDATA** che descrive la condizione dell'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito indica il motivo dell'errore. Se il valore restituito è NMERR \_ Expert \_ Terminate, l'esperto viene immediatamente ripulito e restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




