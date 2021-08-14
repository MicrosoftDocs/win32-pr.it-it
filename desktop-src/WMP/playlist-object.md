---
title: Oggetto Playlist
description: L'oggetto Playlist consente di organizzare gli elementi multimediali in un elenco per facilitarli usando le proprietà e i metodi seguenti.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Oggetto Playlist Windows Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0709b24779d3aac90d496b38b4654596479ad7a9122660158b53b4b2e75ba622
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336719"
---
# <a name="playlist-object"></a>Oggetto Playlist

**L'oggetto Playlist** consente di organizzare gli elementi multimediali in un elenco per facilitarli usando le proprietà e i metodi seguenti.

**L'oggetto Playlist** supporta le proprietà seguenti.



| Proprietà                                      | Descrizione                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [attributeCount](playlist-attributecount.md) | Recupera il numero di attributi associati alla playlist. |
| [Attributename](playlist-attributename.md)   | Recupera il nome di un attributo specificato da un indice.        |
| [count](playlist-count.md)                   | Recupera il numero di elementi nella playlist.                   |
| [nome](playlist-name.md)                     | Specifica o recupera il nome della playlist.                 |



 

**L'oggetto Playlist** supporta i metodi seguenti.



| Metodo                                  | Descrizione                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [appendItem](playlist-appenditem.md)   | Aggiunge un elemento multimediale alla fine della playlist.                                                          |
| **deselezionare**                               | Riservato per utilizzi futuri.                                                                               |
| [getItemInfo](playlist-getiteminfo.md) | Recupera il valore di un attributo playlist.                                                           |
| [insertItem](playlist-insertitem.md)   | Inserisce un elemento multimediale nella playlist nella posizione specificata.                                      |
| [isIdentical](playlist-isidentical.md) | Recupera un valore che indica se l'oggetto **Playlist** fornito è identico a quello corrente. |
| [item](playlist-item.md)               | Recupera l'elemento multimediale in corrispondenza dell'indice specificato.                                                       |
| [moveItem](playlist-moveitem.md)       | Modifica la posizione di un elemento nella playlist.                                                       |
| [Removeitem](playlist-removeitem.md)   | Rimuove l'elemento specificato dalla playlist.                                                          |
| [setItemInfo](playlist-setiteminfo.md) | Specifica il valore di un attributo playlist.                                                           |



 

È possibile accedere all'oggetto **Playlist** tramite le proprietà e i metodi seguenti.



| Oggetto                                              | Proprietà o metodo                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cdrom](cdrom-object.md)                           | [Playlist](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [MediaCollection](mediacollection-object.md)       | [getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md) |
| [Player](player-object.md)                         | [currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)                                                                                                                                                                                               |
| [PlaylistArray](playlistarray-object.md)           | [item](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [PlaylistCollection](playlistcollection-object.md) | [newPlaylist](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

Poiché è il mezzo di accesso più *comune,* player . **currentPlaylist viene** usato a scopo illustrativo nelle sezioni relative alla sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




