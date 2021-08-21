---
title: Evento CdromBurnStateChange dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromBurnStateChange si verifica quando lo stato di un'operazione di masterizzazione cd cambia.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Evento CdromBurnStateChange dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28a8dfad6e5d9bc7bb603632e2eb08ceb5810f9bf02f395d825fc2d7ac64c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055039"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromBurnStateChange dell'oggetto AxWindowsMediaPlayer

L'evento CdromBurnStateChange si verifica quando lo stato di un'operazione di masterizzazione cd cambia.

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEvent**, che contiene le proprietà seguenti correlate a questo evento.



| Proprietà   | Descrizione                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| pCdromBurn | WMPLib.IWMPCdromBurnThe interfaccia che rappresenta l'operazione di masterizzazione che ha generato l'errore.<br/> |
| wmpbs      | WMPLib.WMPKindStateValore di enumerazione che indica il nuovo stato.<br/>                         |



 

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

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





