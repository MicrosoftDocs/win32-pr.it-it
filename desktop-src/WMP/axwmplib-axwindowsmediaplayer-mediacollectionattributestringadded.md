---
title: Evento MediaCollectionAttributeStringAdded dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaCollectionAttributeStringAdded si verifica quando un valore di attributo viene aggiunto alla libreria. | Evento MediaCollectionAttributeStringAdded dell'oggetto AxWindowsMediaPlayer
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- Evento MediaCollectionAttributeStringAdded dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325003"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaCollectionAttributeStringAdded dell'oggetto AxWindowsMediaPlayer

L'evento MediaCollectionAttributeStringAdded si verifica quando un valore di attributo viene aggiunto alla libreria.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaCollectionAttributeStringAddedEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà           | Descrizione                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | System. StringSpecifies il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).<br/> |
| bstrAttribVal      | System. StringSpecifies il valore dell'attributo.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Commenti

Quando un elemento multimediale viene aggiunto alla libreria, i relativi metadati vengono aggiunti alla raccolta di supporti e questo evento viene generato per ogni attributo aggiunto.

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

[**AxWindowsMediaPlayer. mediacollection (VB e C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





