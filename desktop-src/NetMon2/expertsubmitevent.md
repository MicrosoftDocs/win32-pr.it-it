---
description: La funzione ExpertSubmitEvent indica che esiste una condizione di evento e fornisce una struttura di dati che descrive la condizione.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Funzione ExpertSubmitEvent (Netmon.h)
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
ms.openlocfilehash: b6ce73d378e4d8432459a23a76b30ebf4d558a5f82ec230e6841eeeb621aed13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744221"
---
# <a name="expertsubmitevent-function"></a>Funzione ExpertSubmitEvent

La **funzione ExpertSubmitEvent** indica che esiste una condizione di evento e fornisce una struttura di dati che descrive la condizione.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ Pollici\]
</dt> <dd>

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la [funzione Run.](run.md)

</dd> <dt>

*pExpertEvent* \[ Pollici\]
</dt> <dd>

Puntatore a una **struttura NMEVENTDATA** che descrive la condizione dell'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito indica il motivo dell'errore. Se il valore restituito è NMERR \_ EXPERT \_ TERMINATE, l'esperto pulisce e restituisce immediatamente un risultato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




