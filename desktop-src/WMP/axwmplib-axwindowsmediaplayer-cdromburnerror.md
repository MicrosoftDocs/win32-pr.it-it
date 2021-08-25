---
title: Evento CdromError dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromError si verifica quando si verifica un errore generico durante un'operazione di masterizzazione cd.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Evento CdromError dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ea2ca4c510685e8a9d23a3fdc507e055f30c8916c7bf8bbbfbb30a5c4591b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864741"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromError dell'oggetto AxWindowsMediaPlayer

L'evento CdromError si verifica quando si verifica un errore generico durante un'operazione di masterizzazione cd.

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromErrorErrorEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromErrorErrorEvent**, che contiene le proprietà seguenti correlate a questo evento.



| Proprietà   | Descrizione                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| errore hr    | **System.Int32** Errore che ha generato l'evento.<br/>                                               |
| pCdromCombo | Interfaccia WMPLib.IWMPCdromThe che rappresenta l'operazione di compressione che ha generato l'errore.<br/> |



 

## <a name="remarks"></a>Commenti

Per acquisire errori specifici del supporto, gestire AxWMPLib. \_ Evento WMPOCXEvents \_ CdromMediaError.

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

[**Evento AxWindowsMediaPlayer.CdromMediaError (VB e C#)**](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[**Interfaccia IWMPCdrom Sistema (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





