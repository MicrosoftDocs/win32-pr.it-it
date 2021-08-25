---
description: Si verifica quando l'utente preme e rilascia un tasto mentre il controllo InkEdit ha lo stato attivo.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Evento InkEdit.KeyPress (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713100edeae3ce6b950433afb73d13f40aefb291047e98984cbd6908dde3ce2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935100"
---
# <a name="inkeditkeypress-event"></a>Evento InkEdit.KeyPress

Si verifica quando l'utente preme e rilascia un tasto mentre il [controllo InkEdit](inkedit-control-reference.md) ha lo stato attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Char* 
</dt> <dd>

Intero che restituisce un codice chiave ANSI numerico standard. Il *parametro Char* viene passato per riferimento. la modifica di invia un carattere diverso al controllo. Se si modifica *il parametro Char* su 0, l'evento viene annullato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'evento ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito **\_ nell'interfaccia IInkEditEvents.** **\_ L'interfaccia IInkEditEvents** implementa [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ di DISPID IeeKeyPress.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inked.h (richiede anche \_ i.c con input penna)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**Controllo \[ InkEdit dell'evento KeyDown\]**](inkedit-keydown.md)
</dt> <dt>

[**Controllo \[ InkEdit dell'evento KeyUp\]**](inkedit-keyup.md)
</dt> </dl>

 

