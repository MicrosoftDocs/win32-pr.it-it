---
title: Evento CdromBurnMediaError dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromBurnMediaError si verifica quando si verifica un errore durante la masterizzazione di un singolo elemento multimediale in un CD.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Evento CdromBurnMediaError dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba161945edcda7409b842987ab97768c30a6e1f0ba011772cf7f3757d3f61c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765270"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromBurnMediaError dell'oggetto AxWindowsMediaPlayer

L'evento CdromBurnMediaError si verifica quando si verifica un errore durante la masterizzazione di un singolo elemento multimediale in un CD.

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEvent**, che contiene le proprietà seguenti correlate a questo evento.



| Proprietà   | Descrizione                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| pCdromBurn | WMPLib.IWMPCdromBurnThe interfaccia che rappresenta l'operazione di masterizzazione che ha generato l'errore.<br/>               |
| pMedia     | System.ObjectL'elemento multimediale che ha generato l'errore. È possibile eseguire il cast a un'interfaccia IWMPMedia per accedervi.<br/> |



 

## <a name="remarks"></a>Commenti

Per acquisire gli errori generici, gestire AxWMPLib. \_ Evento WMPOCXEvents \_ CdromBurnError.

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

[**Evento AxWindowsMediaPlayer.CdromBurnError (VB e C#)**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





