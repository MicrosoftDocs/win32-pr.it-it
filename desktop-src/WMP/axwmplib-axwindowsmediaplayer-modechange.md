---
title: Evento ModeChange dell'oggetto AxWindowsMediaPlayer
description: L'evento ModeChange si verifica quando viene modificata una modalità di Windows Media Player. | Evento ModeChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Evento ModeChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330012"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a>Evento ModeChange dell'oggetto AxWindowsMediaPlayer

L'evento ModeChange si verifica quando viene modificata una modalità di Windows Media Player.

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_ModeChangeEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà | Descrizione                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| modeName | System. StringIndicates la modalità modificata. Per i valori possibili, vedere la sezione Osservazioni.<br/> |
| newValue | System. BooleanIndicates il nuovo stato della modalità specificata.<br/>                        |



 

## <a name="remarks"></a>Commenti

Nella tabella seguente sono riportati i valori possibili per la proprietà modeName.



| string  | Descrizione                                         |
|---------|-----------------------------------------------------|
| shuffle | Le tracce vengono riprodotte in ordine casuale.                  |
| loop    | L'intera sequenza di tracce viene riprodotta ripetutamente. |



 

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

[**IWMPSettings. getMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. semode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





