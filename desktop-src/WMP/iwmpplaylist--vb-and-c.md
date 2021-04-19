---
title: Interfaccia IWMPPlaylist (VB e C) (Wmp.h)
description: Fornisce proprietà e metodi per organizzare, gestire e modificare gli elementi multimediali in una playlist. L'interfaccia IWMPPlaylist espone le proprietà seguenti.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- Interfaccia IWMPPlaylist (VB e C) Windows Media Player
- Interfaccia IWMPPlaylist (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52090588905e2fd79b218abe939f78c1e38fc79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329995"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>Interfaccia IWMPPlaylist (VB e C#)

Fornisce proprietà e metodi per organizzare, gestire e modificare gli elementi multimediali in una playlist.

L'interfaccia **IWMPPlaylist** espone le proprietà seguenti.

## <a name="members"></a>Membri

L'interfaccia **IWMPPlaylist (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPPlaylist (VB e C#)** presenta questi metodi.



| Metodo                                                                       | Descrizione                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**appendItem**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | Aggiunge un elemento multimediale alla fine della playlist.<br/>                |
| [**deselezionare**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | Riservato per utilizzi futuri.<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | Restituisce il valore di un attributo della playlist specificato in base al nome.<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | Inserisce un elemento multimediale in una posizione specificata in una playlist.<br/>  |
| [**moveItem**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | Modifica la posizione di un elemento multimediale nella playlist.<br/>        |
| [**removeItem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | Rimuove l'elemento multimediale specificato dalla playlist.<br/>          |
| [**setItemInfo**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | Imposta il valore di un attributo della playlist.<br/>                      |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPPlaylist (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                      | Tipo di accesso           | Descrizione                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | Sola lettura<br/>  | Ottiene il numero di attributi associati a una playlist.<br/>                                                                                |
| [**attributeName**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | Sola lettura<br/>  | Ottiene il nome di un attributo della playlist specificato da un indice. In C# si tratta del \_ metodo Get AttributeName.<br/>                               |
| [**count**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | Sola lettura<br/>  | Ottiene il numero di elementi multimediali in una playlist.<br/>                                                                                            |
| [**Identico**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | Sola lettura<br/>  | Ottiene un valore che indica se la playlist specificata è identica alla playlist corrente. In C# il metodo Get è \_ identico.<br/> |
| [**Elemento**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | Sola lettura<br/>  | Ottiene un'interfaccia per l'elemento multimediale in corrispondenza dell'indice specificato. In C# si tratta del \_ metodo Get Item.<br/>                                         |
| [**nome**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta il nome della playlist.<br/>                                                                                                   |



 

Ottenere un'interfaccia **IWMPPlaylist** usando le proprietà o i metodi seguenti a cui si accede tramite l'oggetto o l'interfaccia seguente.



| Oggetto o interfaccia                                                | Proprietà o metodo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPCdrom**](iwmpcdrom--vb-and-c.md)                           | [**Playlist**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**IWMPMediaCollection**](iwmpmediacollection--vb-and-c.md)       | [**GetAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**GetByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md)  | [**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **nuova playlist**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWMPPlaylistArray**](iwmpplaylistarray--vb-and-c.md)           | [**Elemento**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**IWMPPlaylistCollection**](iwmpplaylistcollection--vb-and-c.md) | [**Nuova playlist**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





