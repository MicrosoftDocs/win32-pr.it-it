---
title: Interfaccia IWMPMediaCollection (VB e C) (WMP. h)
description: Fornisce metodi che possono essere usati per organizzare un'ampia raccolta di elementi multimediali.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- Interfaccia IWMPMediaCollection (VB e C) Windows Media Player
- Interfaccia IWMPMediaCollection (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424fd45b1fd3d02000a9774ffe75ec87e52dd9c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333750"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a>Interfaccia IWMPMediaCollection (VB e C#)

Fornisce metodi che possono essere usati per organizzare un'ampia raccolta di elementi multimediali.

## <a name="members"></a>Membri

L'interfaccia **IWMPMediaCollection (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPMediaCollection (VB e C#)** presenta questi metodi.



| Metodo                                                                                                                       | Descrizione                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**add**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | Aggiunge un nuovo elemento multimediale o una playlist alla raccolta.<br/>                                                                                  |
| [**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | Restituisce un'interfaccia **IWMPPlaylist** che corrisponde alla playlist che contiene tutti gli elementi multimediali nella libreria.<br/>               |
| [**getAttributeStringCollection**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | Restituisce un'interfaccia **IWMPStringCollection** che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto.<br/> |
| [**getByAlbum**](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali dall'album specificato.<br/>                                |
| [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | Restituisce un'interfaccia **IWMPPlaylist** che corrisponde all'attributo specificato con il valore specificato.<br/>                      |
| [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali dall'autore specificato.<br/>                             |
| [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali del genere specificato.<br/>                                  |
| [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali con il nome specificato.<br/>                                 |
| [**getMediaAtom**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | Restituisce l'indice di un attributo specificato.<br/>                                                                                        |
| **isDeleted**                                                                                                                | Non più supportata.<br/>                                                                                                               |
| [**rimuovere**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | Rimuove l'elemento multimediale specificato dall'insieme di supporti.<br/>                                                                        |
| [**Eliminata**](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | Sposta l'elemento multimediale specificato nella cartella elementi eliminati.<br/>                                                                        |



 

Ottenere un'interfaccia **IWMPMediaCollection** usando le proprietà seguenti a cui si accede tramite l'oggetto o l'interfaccia seguente.



| Oggetto o interfaccia                                               | Proprietà                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**mediacollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [**IWMPLibrary**](iwmplibrary--vb-and-c.md)                      | [**mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMediaCollection2**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





