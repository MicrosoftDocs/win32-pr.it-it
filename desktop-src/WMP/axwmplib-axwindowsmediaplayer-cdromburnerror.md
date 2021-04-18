---
title: Evento CdromBurnError dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromBurnError si verifica quando si verifica un errore generico durante un'operazione di masterizzazione del CD.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Evento CdromBurnError dell'oggetto AxWindowsMediaPlayer Media Player Windows
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
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323927"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromBurnError dell'oggetto AxWindowsMediaPlayer

L'evento CdromBurnError si verifica quando si verifica un errore generico durante un'operazione di masterizzazione del CD.

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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CdromBurnErrorEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà   | Descrizione                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| hrError    | **System. Int32** Errore che ha generato l'evento.<br/>                                               |
| pCdromBurn | Interfaccia WMPLib. IWMPCdromBurnThe che rappresenta l'operazione di masterizzazione che ha generato l'errore.<br/> |



 

## <a name="remarks"></a>Commenti

Per acquisire gli errori specifici del supporto, gestire AxWMPLib. \_ \_Evento CdromBurnMediaError WMPOCXEvents.

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

[**Evento AxWindowsMediaPlayer. CdromBurnMediaError (VB e C#)**](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





