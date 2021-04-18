---
title: Evento MediaCollectionAttributeStringRemoved dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaCollectionAttributeStringRemoved si verifica quando viene rimosso un valore di attributo dalla libreria. | Evento MediaCollectionAttributeStringRemoved dell'oggetto AxWindowsMediaPlayer
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Evento MediaCollectionAttributeStringRemoved dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324749"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaCollectionAttributeStringRemoved dell'oggetto AxWindowsMediaPlayer

L'evento MediaCollectionAttributeStringRemoved si verifica quando viene rimosso un valore di attributo dalla libreria.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaCollectionAttributeStringRemovedEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà           | Descrizione                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | System. StringSpecifies il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).<br/> |
| bstrAttribVal      | System. StringSpecifies il valore dell'attributo.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Commenti

Quando un elemento multimediale viene rimosso dalla libreria, i relativi metadati vengono rimossi da **mediacollection** e questo evento viene generato per ogni attributo rimosso.

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

 

 





