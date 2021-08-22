---
title: Evento LibraryDisconnect dell'oggetto AxWindowsMediaPlayer
description: L'evento LibraryDisconnect si verifica quando una libreria non è più disponibile.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Evento LibraryDisconnect dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a032dc95a68430768b0f2aa109a56dae80cdaecb14b67eb5dbf6b2657cdd5107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136004"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a>Evento LibraryDisconnect dell'oggetto AxWindowsMediaPlayer

L'evento LibraryDisconnect si verifica quando una libreria non è più disponibile.

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ Libreria \_ WMPOCXEventsDisconnectEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ Libreria WMPOCXEventsDisconnectEvent \_**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà | Descrizione                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib.IWMPLibrary** Interfaccia che rappresenta la libreria disconnessa.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento non si verifica per la libreria locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                                         |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





