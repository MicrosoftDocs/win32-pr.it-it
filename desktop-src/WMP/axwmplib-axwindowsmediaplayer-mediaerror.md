---
title: Evento MediaError dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaError si verifica quando un oggetto multimediale presenta una condizione di errore.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- Evento MediaError dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83dc6bceb188ff443bfdcab904242e91b30fba80c4bae4f03cfa388cf15642b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902611"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaError dell'oggetto AxWindowsMediaPlayer

L'evento MediaError si verifica quando un oggetto multimediale presenta una condizione di errore.

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà     | Descrizione                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| pMediaObject | System.ObjectObject con una condizione di errore. È possibile eseguire il cast a un'interfaccia IWMPMedia per accedervi.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





