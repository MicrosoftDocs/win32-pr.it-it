---
description: Deprecato. L'oggetto PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica quando lo stato attivo per l'input cambia prima che l'oggetto PenInputPanel fosse in grado di inserire l'input dell'utente nel controllo associato.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Evento PenInputPanel. InputFailed (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319158"
---
# <a name="peninputpanelinputfailed-event"></a>PenInputPanel. InputFailed, evento

Deprecato. L'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).

Si verifica quando lo stato attivo per l'input cambia prima che l'oggetto [**PenInputPanel**](peninputpanel-class.md) fosse in grado di inserire l'input dell'utente nel controllo associato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle della finestra del controllo che ha richiamato l'oggetto [**PenInputPanel**](peninputpanel-class.md) .

</dd> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Chiave virtuale corrispondente al tasto premuto.

</dd> <dt>

*Testo* \[ in\]
</dt> <dd>

Stringa da inserire nel controllo rappresentato dal parametro *HWND* quando è stato generato l'evento **InputFailed** .

Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzo della libreria com](using-the-com-library.md).

</dd> <dt>

*ShiftKey* \[ in\]
</dt> <dd>

Stato dei modificatori della tastiera, inclusi MAIUSC, CAPS, CTRL e ALT.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'evento ha esito positivo, viene restituito **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'evento **InputFailed** si verifica quando lo stato attivo per l'input viene modificato prima dell'inserimento dell'input utente nel controllo associato. Ad esempio, se l'utente immette input penna nel riquadro di scrittura, quindi tocca un altro controllo di modifica prima che il riconoscimento abbia avuto la possibilità di terminare, questo evento viene generato.

Usando l'handle di finestra passato in questo evento, è possibile scegliere di inserire il testo quando si verifica questo evento.

> [!Note]  
> A partire da Microsoft Windows XP Tablet PC Edition 2005, l'evento **InputFailed** non viene più applicato. Il testo viene sempre inserito prima della modifica dello stato attivo.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




