---
title: Interfaccia IWMPPlaylist (VB e C) (Wmp.h)
description: Fornisce proprietà e metodi per organizzare, gestire e modificare gli elementi multimediali in una playlist. L'interfaccia IWMPPlaylist espone le proprietà seguenti.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- Interfaccia IWMPPlaylist (VB e C) Windows Media Player
- Interfaccia IWMPPlaylist (VB e C) Windows Media Player , descritta
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
ms.openlocfilehash: b3fc1d8be09596d89dd87748811846d6dee1e8af8f28bebec56fa852c42ed6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119007"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>Interfaccia IWMPPlaylist (VB e C#)

Fornisce proprietà e metodi per organizzare, gestire e modificare gli elementi multimediali in una playlist.

**L'interfaccia IWMPPlaylist** espone le proprietà seguenti.

## <a name="members"></a>Membri

**L'interfaccia IWMPPlaylist (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IWMPPlaylist (VB e C#).**



| Metodo                                                                       | Descrizione                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**appendItem**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | Aggiunge un elemento multimediale alla fine della playlist.<br/>                |
| [**Chiaro**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | Riservato per utilizzi futuri.<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | Restituisce il valore di un attributo playlist specificato in base al nome.<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | Inserisce un elemento multimediale in una posizione specificata in una playlist.<br/>  |
| [**moveItem**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | Modifica la posizione di un elemento multimediale nella playlist.<br/>        |
| [**Removeitem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | Rimuove l'elemento multimediale specificato dalla playlist.<br/>          |
| [**setItemInfo**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | Imposta il valore di un attributo playlist.<br/>                      |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili **nell'interfaccia IWMPPlaylist (VB e C#).**



| Proprietà                                                                                      | Tipo di accesso           | Descrizione                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | Sola lettura<br/>  | Ottiene il numero di attributi associati a una playlist.<br/>                                                                                |
| [**Attributename**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | Sola lettura<br/>  | Ottiene il nome di un attributo playlist specificato da un indice. In C# si tratta del metodo get \_ attributeName.<br/>                               |
| [**Conteggio**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | Sola lettura<br/>  | Ottiene il numero di elementi multimediali in una playlist.<br/>                                                                                            |
| [**isIdentical**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | Sola lettura<br/>  | Ottiene un valore che indica se la playlist specificata è identica alla playlist corrente. In C# questo è il metodo \_ get isIdentical.<br/> |
| [**Elemento**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | Sola lettura<br/>  | Ottiene un'interfaccia per l'elemento multimediale in corrispondenza dell'indice specificato. In C# questo è il metodo get \_ Item.<br/>                                         |
| [**Nome**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta il nome della playlist.<br/>                                                                                                   |



 

Ottenere **un'interfaccia IWMPPlaylist** usando le proprietà o i metodi seguenti a cui si accede tramite l'oggetto o l'interfaccia seguente.



| Oggetto o interfaccia                                                | Proprietà o metodo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPCdrom**](iwmpcdrom--vb-and-c.md)                           | [**Playlist**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**IWMPMediaCollection**](iwmpmediacollection--vb-and-c.md)       | [**getAll,**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md) [**getByAlbum,**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum) [**getByAttribute,**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md) [**getByAuthor,**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md) [**getByGenre,**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md) [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md)  | [**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWMPPlaylistArray**](iwmpplaylistarray--vb-and-c.md)           | [**Elemento**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**IWMPPlaylistCollection**](iwmpplaylistcollection--vb-and-c.md) | [**newPlaylist**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





