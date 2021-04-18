---
title: Evento FolderScanStateChange dell'oggetto AxWindowsMediaPlayer
description: L'evento FolderScanStateChange si verifica quando viene modificato lo stato di un'operazione di monitoraggio della cartella.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Evento FolderScanStateChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324386"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento FolderScanStateChange dell'oggetto AxWindowsMediaPlayer

L'evento FolderScanStateChange si verifica quando viene modificato lo stato di un'operazione di monitoraggio della cartella.

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_FolderScanStateChangeEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà | Descrizione                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| wmpfss   | Valore di enumerazione WMPLib. WMPFolderScanStateThe che indica il nuovo stato.<br/> |



 

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

[**WMPFolderScanState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





