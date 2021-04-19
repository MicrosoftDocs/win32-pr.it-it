---
title: Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer
description: L'evento CurrentMediaItemAvailable si verifica quando diventa disponibile un elemento di metadati grafici nell'elemento multimediale corrente. | Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331891"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer

L'evento CurrentMediaItemAvailable si verifica quando diventa disponibile un elemento di metadati grafici nell'elemento multimediale corrente.

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CurrentMediaItemAvailableEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà     | Descrizione                                                 |
|--------------|-------------------------------------------------------------|
| bstrItemName | System. StringThe nome dell'elemento multimediale corrente.<br/> |



 

## <a name="remarks"></a>Commenti

Poiché la riproduzione può iniziare prima che un elemento multimediale venga scaricato completamente, eventuali elementi grafici dei metadati contenuti nell'elemento multimediale, ad esempio Album Cover Art, potrebbero non essere disponibili quando viene avviata la riproduzione. Questo evento avvisa l'utente al termine del download di un elemento grafico dei metadati. È quindi possibile recuperare l'interfaccia **IWMPMedia** passando il valore di **bstrItemName** a *IWMPMediaCollection*. metodo **GetByName** , dopo il quale è possibile accedere all'elemento grafico dei metadati utilizzando *IWMPMedia3*. **getItemInfoByType** e specificando **WM/Picture** per il nome dell'attributo.

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

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. getByName (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





