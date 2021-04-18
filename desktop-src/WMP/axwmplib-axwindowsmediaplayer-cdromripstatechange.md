---
title: Evento CdromRipStateChange dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromRipStateChange si verifica quando viene modificato lo stato di un'operazione di copia del CD.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Evento CdromRipStateChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323919"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromRipStateChange dell'oggetto AxWindowsMediaPlayer

L'evento CdromRipStateChange si verifica quando viene modificato lo stato di un'operazione di copia del CD.

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CdromRipStateChangeEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà  | Descrizione                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| pCdromRip | Interfaccia WMPLib. IWMPCdromRipThe che rappresenta l'operazione di strappo che ha generato l'errore.<br/> |
| wmprs     | Valore di enumerazione WMPLib. WMPRipStateThe che indica il nuovo stato.<br/>                         |



 

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

[**WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





