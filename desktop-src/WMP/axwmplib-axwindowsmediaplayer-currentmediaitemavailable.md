---
title: Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer
description: L'evento CurrentMediaItemAvailable si verifica quando un elemento di metadati grafico nell'elemento multimediale corrente diventa disponibile. | Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: 6b5bbac6f27dfa7c9de1115eb3c2f5eea85096e0868ac17e0f8b11d81385f344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582350"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer

L'evento CurrentMediaItemAvailable si verifica quando un elemento di metadati grafico nell'elemento multimediale corrente diventa disponibile.

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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà     | Descrizione                                                 |
|--------------|-------------------------------------------------------------|
| bstrItemName | System.StringNo nome dell'elemento multimediale corrente.<br/> |



 

## <a name="remarks"></a>Commenti

Poiché la riproduzione può iniziare prima del download completo di un elemento multimediale, qualsiasi elemento multimediale contenuto nell'elemento multimediale (ad esempio la copertina dell'album) potrebbe non essere disponibile all'avvio della riproduzione. Questo evento avvisa l'utente al termine del download di un elemento grafico dei metadati. È quindi possibile recuperare **l'interfaccia IWMPMedia** passando il valore **di bstrItemName** a *IWMPMediaCollection*. **Metodo getByName,** dopo il quale è possibile accedere all'elemento grafico dei metadati usando *IWMPMedia3.* **getItemInfoByType e** specificando **WM/Picture** per il nome dell'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.getByName (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





