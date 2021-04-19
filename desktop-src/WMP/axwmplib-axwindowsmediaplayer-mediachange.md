---
title: Evento MediaChange dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaChange si verifica quando viene modificato un elemento multimediale. | Evento MediaChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 0a2380ff-df50-4092-a952-812184822719
keywords:
- Evento MediaChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175a7ed6ca57e3083d307cfe218d09233410053c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329445"
---
# <a name="mediachange-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaChange dell'oggetto AxWindowsMediaPlayer

L'evento MediaChange si verifica quando viene modificato un elemento multimediale.

``` syntax
[C#]
private void player_MediaChange(
  object sender,
  _WMPOCXEvents_MediaChangeEvent e
)

[Visual Basic]
Private Sub player_MediaChange(  
  sender As Object,  
  e As _WMPOCXEvents_MediaChangeEvent
) Handles player.MediaChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaChangeEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaChangeEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà | Descrizione                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------|
| Elemento     | Elemento multimediale System. ObjectThe modificato. È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPMedia per accedervi.<br/> |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzata un'etichetta per visualizzare il nome dell'elemento multimediale corrente. Il codice aggiorna il testo nell'etichetta a ogni occorrenza dell'evento MediaChange. L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.


```CSharp
// Add a delegate for the MediaChange event.
player.MediaChange += new AxWMPLib._WMPOCXEvents_MediaChangeEventHandler(player_MediaChange);

private void player_MediaChange(object sender, AxWMPLib._WMPOCXEvents_MediaChangeEvent e)
{
    // Get an interface to the changed media item that is returned in the event data. 
    WMPLib.IWMPMedia3 changedItem = (WMPLib.IWMPMedia3)e.item;

    // Display the name of the changed media item.
    mediaName.Text = changedItem.name;
}
```


```VB

Public Sub player_MediaChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_MediaChangeEvent) Handles player.MediaChange

    &#39; Get an interface to the changed media item that is returned in the event data.
    Dim changedItem As WMPLib.IWMPMedia3 = e.item

    &#39; Display the name of the changed media item.
    mediaName.Text = changedItem.name

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





