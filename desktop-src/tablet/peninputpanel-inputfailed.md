---
description: Deprecato. PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica quando lo stato attivo dell'input cambia prima che l'oggetto PenInputPanel sia in grado di inserire l'input dell'utente nel controllo associato.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Evento PenInputPanel.InputFailed (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc3234c73fc8ba47faa7d1f2ec89477a1bfb86b7c2abda263aff227c5961f1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934761"
---
# <a name="peninputpanelinputfailed-event"></a>Evento PenInputPanel.InputFailed

Deprecato. [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal pannello [di input di testo (TIP).](text-input-panel-reference.md)

Si verifica quando lo stato attivo dell'input cambia prima che l'oggetto [**PenInputPanel**](peninputpanel-class.md) sia in grado di inserire l'input dell'utente nel controllo associato.

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

*hWnd* \[ Pollici\]
</dt> <dd>

Handle della finestra del controllo che ha richiamato [**l'oggetto PenInputPanel.**](peninputpanel-class.md)

</dd> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Tasto virtuale corrispondente al tasto premuto.

</dd> <dt>

*Testo* \[ Pollici\]
</dt> <dd>

Stringa che deve essere inserita nel controllo rappresentato dal *parametro hWnd* quando è stato generato l'evento **InputFailed.**

Per altre informazioni sul tipo di dati BSTR, vedere [Uso della libreria COM](using-the-com-library.md).

</dd> <dt>

*MaiuscKey* \[ Pollici\]
</dt> <dd>

Stato dei modificatori della tastiera, tra cui MAIUSC, MAIUSC, CTRL e ALT.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo evento ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

**L'evento InputFailed** si verifica quando lo stato attivo dell'input cambia prima che l'input dell'utente sia stato inserito nel controllo associato. Ad esempio, se l'utente immette input penna nel blocco di scrittura, quindi tocca un altro controllo di modifica prima che il riconoscitore abbia avuto la possibilità di terminare, questo evento viene generato.

Usando l'handle di finestra passato a questo evento, è possibile scegliere di inserire il testo manualmente quando si verifica questo evento.

> [!Note]  
> A partire da Microsoft Windows XP Tablet PC Edition 2005, l'evento **InputFailed** non si applica più. Il testo viene sempre inserito prima della modifica dello stato attivo.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Peninputpanel**](peninputpanel-class.md)
</dt> </dl>

 

 




