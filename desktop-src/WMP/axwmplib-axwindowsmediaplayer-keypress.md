---
title: Evento KeyPress dell'oggetto AxWindowsMediaPlayer
description: L'evento KeyPress si verifica quando viene premuto e rilasciato un tasto. | Evento KeyPress dell'oggetto AxWindowsMediaPlayer
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Evento KeyPress dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b8022feacda910b28d68636c1abdcb2f6c1c9d3c2e799f762f25f5060b2b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618791"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a>Evento KeyPress dell'oggetto AxWindowsMediaPlayer

L'evento KeyPress si verifica quando viene premuto e rilasciato un tasto.

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent,** che contiene la proprietà seguente correlata a questo evento.



| Proprietà      | Descrizione                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **nKeyAscii** | System.Int16Specifica il codice ANSI numerico standard per il carattere.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento si verifica quando la pressione del tasto risulta in qualsiasi carattere stampabile della tastiera, il tasto CTRL combinato con un carattere dell'alfabeto standard o uno di alcuni caratteri speciali e il tasto INVIO o BACKSPACE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





