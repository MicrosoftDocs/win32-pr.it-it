---
title: Evento CdromRipMediaError dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromRipMediaError si verifica quando si verifica un errore durante lo scheggiamento di una singola traccia da un CD.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Evento CdromRipMediaError dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2be1f777c4af3385e41939743bb91a20d3d7094f1a38917b3e79686b2a2863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136184"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromRipMediaError dell'oggetto AxWindowsMediaPlayer

L'evento CdromRipMediaError si verifica quando si verifica un errore durante lo scheggiamento di una singola traccia da un CD.

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEvent**, che contiene le proprietà seguenti correlate a questo evento.



| Proprietà  | Descrizione                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| pCdromRip | WMPLib.IWMPCdromRip Interface che rappresenta l'operazione di depping che ha generato l'errore.<br/>                |
| pMedia    | System.Object Elemento multimediale che ha generato l'errore. È possibile eseguire il cast a un'interfaccia IWMPMedia per accedervi.<br/> |



 

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

[**Interfaccia IWMPCdromRip (VB e C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





