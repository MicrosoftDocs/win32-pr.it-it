---
title: Evento KeyPress dell'oggetto AxWindowsMediaPlayer
description: L'evento KeyPress si verifica quando un tasto viene premuto e rilasciato. | Evento KeyPress dell'oggetto AxWindowsMediaPlayer
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
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331888"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a>Evento KeyPress dell'oggetto AxWindowsMediaPlayer

L'evento KeyPress si verifica quando un tasto viene premuto e rilasciato.

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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_KeyPressEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà      | Descrizione                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **nKeyAscii** | System. Int16Specifies codice ANSI numerico standard per il carattere.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento si verifica quando la sequenza di tasti restituisce un carattere di tastiera stampabile, il tasto CTRL combinato con un carattere dell'alfabeto standard o uno dei caratteri speciali e il tasto invio o BACKSPACE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





