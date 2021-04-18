---
title: Evento di avviso dell'oggetto AxWindowsMediaPlayer
description: L'evento di avviso è riservato per un utilizzo futuro.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Evento di avviso dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330896"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a>Evento di avviso dell'oggetto AxWindowsMediaPlayer

L'evento di avviso è riservato per un utilizzo futuro.

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_WarningEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà    | Descrizione                                |
|-------------|--------------------------------------------|
| warningType | **System. Int32** Non supportato.<br/>  |
| param       | **System. Int32** Non supportato.<br/>  |
| description | **System. String** Non supportato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento è riservato per un utilizzo futuro.

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

 

 





