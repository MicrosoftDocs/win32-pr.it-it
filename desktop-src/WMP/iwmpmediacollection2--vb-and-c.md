---
title: Interfaccia IWMPMediaCollection2 (VB e C) (WMP. h)
description: Fornisce metodi che integrano l'interfaccia IWMPMediaCollection.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- Interfaccia IWMPMediaCollection2 (VB e C) Windows Media Player
- Interfaccia IWMPMediaCollection2 (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329309"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a>Interfaccia IWMPMediaCollection2 (VB e C#)

Fornisce metodi che integrano l'interfaccia **IWMPMediaCollection** .

## <a name="members"></a>Membri

L'interfaccia **IWMPMediaCollection2 (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPMediaCollection2 (VB e C#)** presenta questi metodi.



| Metodo                                                                                                                     | Descrizione                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**createQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | Restituisce un'interfaccia **IWMPQuery** che rappresenta una nuova query.<br/>                                                                                               |
| [**getByAttributeAndMediaType**](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali con un attributo e un tipo di supporto specificati.<br/>                                     |
| [**getPlaylistByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | Restituisce un'interfaccia **IWMPPlaylist** che consente di accedere agli elementi multimediali che corrispondono alle condizioni della query.<br/>                                                    |
| [**getStringCollectionByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | Restituisce un'interfaccia **IWMPStringCollection** che fornisce l'accesso al set di tutti i valori stringa per un attributo specificato che soddisfano le condizioni della query.<br/> |



 

Ottenere un'interfaccia **IWMPMediaCollection2** eseguendo il cast del valore restituito dalla proprietà [**AxWindowsMediaPlayer. mediacollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) o dal valore restituito dalla proprietà [**IWMPLibrary. mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





