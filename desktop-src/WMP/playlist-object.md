---
title: Oggetto playlist
description: L'oggetto playlist fornisce un modo per organizzare gli elementi multimediali in un elenco per semplificare la manipolazione usando le proprietà e i metodi seguenti.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Finestre oggetto playlist Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045514"
---
# <a name="playlist-object"></a>Oggetto playlist

L'oggetto **playlist** fornisce un modo per organizzare gli elementi multimediali in un elenco per semplificare la manipolazione usando le proprietà e i metodi seguenti.

L'oggetto **playlist** supporta le proprietà seguenti.



| Proprietà                                      | Descrizione                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [attributeCount](playlist-attributecount.md) | Recupera il numero di attributi associati alla playlist. |
| [attributeName](playlist-attributename.md)   | Recupera il nome di un attributo specificato da un indice.        |
| [count](playlist-count.md)                   | Recupera il numero di elementi nella playlist.                   |
| [nome](playlist-name.md)                     | Specifica o Recupera il nome della playlist.                 |



 

L'oggetto **playlist** supporta i metodi seguenti.



| Metodo                                  | Descrizione                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [appendItem](playlist-appenditem.md)   | Aggiunge un elemento multimediale alla fine della playlist.                                                          |
| **deselezionare**                               | Riservato per utilizzi futuri.                                                                               |
| [getItemInfo](playlist-getiteminfo.md) | Recupera il valore di un attributo della playlist.                                                           |
| [insertItem](playlist-insertitem.md)   | Inserisce un elemento multimediale nella playlist nella posizione specificata.                                      |
| [Identico](playlist-isidentical.md) | Recupera un valore che indica se l'oggetto **playlist** fornito è identico a quello corrente. |
| [item](playlist-item.md)               | Recupera l'elemento multimediale in corrispondenza dell'indice specificato.                                                       |
| [moveItem](playlist-moveitem.md)       | Modifica la posizione di un elemento nella playlist.                                                       |
| [removeItem](playlist-removeitem.md)   | Rimuove l'elemento specificato dalla playlist.                                                          |
| [setItemInfo](playlist-setiteminfo.md) | Specifica il valore di un attributo della playlist.                                                           |



 

È possibile accedere all'oggetto **playlist** tramite le proprietà e i metodi seguenti.



| Oggetto                                              | Proprietà o metodo                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cdrom](cdrom-object.md)                           | [playlist](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [Mediacollection](mediacollection-object.md)       | [GetAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [GetByName](mediacollection-getbyname.md) |
| [Player](player-object.md)                         | [currentPlaylist](player-currentplaylist.md), [nuova playlist](player-newplaylist.md)                                                                                                                                                                                               |
| [PlaylistArray](playlistarray-object.md)           | [item](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [PlaylistCollection](playlistcollection-object.md) | [Nuova playlist](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

Poiché si tratta del mezzo più comune di accesso, *Player*. **currentPlaylist** viene usato a scopo illustrativo nelle sezioni della sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




