---
description: Trova l'istanza successiva della proprietà specificata dal parametro hProperty.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Funzione FindPropertyInstanceRestart (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0699cb37165e9181bf78bc3a86ad68c07dbbd589469e3e0bca6a1cd0228573f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890811"
---
# <a name="findpropertyinstancerestart-function"></a>Funzione FindPropertyInstanceRestart

La **funzione FindPropertyInstanceRestart** trova l'istanza successiva della proprietà specificata dal *parametro hProperty.*

## <a name="syntax"></a>Sintassi


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per il frame. L'handle del frame può essere recuperato da una chiamata alla [funzione GetFrame.](getframe.md)

</dd> <dt>

*hProperty* \[ Pollici\]
</dt> <dd>

Handle per la proprietà da trovare. L'handle della proprietà può essere recuperato da una chiamata alla [funzione GetProperty.](getproperty.md)

</dd> <dt>

*lpRestartKey* \[ Pollici\]
</dt> <dd>

Puntatore all'istanza della proprietà utilizzata come punto iniziale della ricerca. Se il *parametro lpRestartKey* è impostato su **NULL,** la ricerca inizia all'inizio del frame o alla fine del frame, a seconda del valore del *parametro DirForward.*

Se *lpRestartKey* punta a **NULL,** la ricerca inizia all'inizio del frame se *DirForward* è **TRUE** o alla fine del frame se il parametro è **FALSE.**

</dd> <dt>

*DirForward* \[ Pollici\]
</dt> <dd>

Indicatore della direzione di ricerca. Se il valore è **TRUE,** la ricerca viene spostata dalla posizione corrente alla fine del frame. Se il valore è **FALSE,** la ricerca viene spostata dalla posizione corrente all'inizio del frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è il successivo **LPPROPERTYINST valido.**

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser possono*](p.md) chiamare la **funzione FindPropertyInstanceRestart.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetFrame](getframe.md)
</dt> <dt>

[Getproperty](getproperty.md)
</dt> </dl>

 

 




