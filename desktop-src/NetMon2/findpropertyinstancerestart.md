---
description: Trova l'istanza successiva della proprietà specificata dal parametro hProperty.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Funzione FindPropertyInstanceRestart (Netmon. h)
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
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305930"
---
# <a name="findpropertyinstancerestart-function"></a>FindPropertyInstanceRestart (funzione)

La funzione **FindPropertyInstanceRestart** trova l'istanza successiva della proprietà specificata dal parametro *hProperty* .

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

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame. L'handle del frame può essere recuperato da una chiamata alla funzione [GetFrame](getframe.md) .

</dd> <dt>

*hProperty* \[ in\]
</dt> <dd>

Handle per la proprietà da trovare. L'handle di proprietà può essere recuperato da una chiamata alla funzione [GetProperty](getproperty.md) .

</dd> <dt>

*lpRestartKey* \[ in\]
</dt> <dd>

Puntatore all'istanza della proprietà utilizzata come punto iniziale della ricerca. Se il parametro *lpRestartKey* è impostato su **null**, la ricerca inizia all'inizio del frame o alla fine del frame, a seconda del valore del parametro *DirForward* .

Se *lpRestartKey* punta a **null**, la ricerca inizia all'inizio del frame se *DirForward* è **true** o alla fine del frame se il parametro è **false**.

</dd> <dt>

*DirForward* \[ in\]
</dt> <dd>

Indicatore della direzione di ricerca. Se il valore è **true**, la ricerca viene spostata dalla posizione corrente alla fine del frame. Se il valore è **false**, la ricerca viene spostata dalla posizione corrente all'inizio del frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è il successivo **LPPROPERTYINST** valido.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **FindPropertyInstanceRestart** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetFrame](getframe.md)
</dt> <dt>

[GetProperty](getproperty.md)
</dt> </dl>

 

 




