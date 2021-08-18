---
title: Oggetto MediaCollection
description: L'oggetto MediaCollection consente di organizzare un'ampia raccolta di elementi multimediali. È possibile eseguire query per generare automaticamente le playlist.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Oggetto MediaCollection Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e529bec203b836f1f1022793a18320a7612cb242de58407ddb998c7410a47cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996251"
---
# <a name="mediacollection-object"></a>Oggetto MediaCollection

**L'oggetto MediaCollection** consente di organizzare un'ampia raccolta di elementi multimediali. È possibile eseguire query per generare automaticamente le playlist.

**L'oggetto MediaCollection** supporta i metodi seguenti.



| Metodo                                                                           | Descrizione                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [add](mediacollection-add.md)                                                   | Aggiunge un nuovo elemento multimediale o playlist alla libreria.                                                                                                              |
| [Createquery](mediacollection-createquery.md)                                   | Crea un nuovo [oggetto Query.](query-object.md)                                                                                                                |
| [getAll](mediacollection-getall.md)                                             | Recupera un oggetto [Playlist](playlist-object.md) contenente tutti gli elementi multimediali nella libreria.                                                                  |
| [getAttributeStringCollection](mediacollection-getattributestringcollection.md) | Recupera un oggetto [StringCollection](stringcollection-object.md) che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto specificato. |
| [getByAlbum](mediacollection-getbyalbum.md)                                     | Recupera un oggetto [Playlist contenente](playlist-object.md) elementi multimediali dall'album specificato.                                                            |
| [getByAttribute](mediacollection-getbyattribute.md)                             | Recupera un oggetto [Playlist](playlist-object.md) contenente elementi multimediali con l'attributo specificato con il valore specificato.                             |
| [getByAttributeAndMediaType](mediacollection-getbyattributeandmediatype.md)     | Recupera un oggetto [Playlist contenente](playlist-object.md) oggetti [Media](media-object.md) con l'attributo e il tipo di supporto specificati.                 |
| [getByAuthor](mediacollection-getbyauthor.md)                                   | Recupera un oggetto [Playlist contenente](playlist-object.md) gli elementi multimediali dell'autore specificato.                                                             |
| [getByGenre](mediacollection-getbygenre.md)                                     | Recupera un oggetto [Playlist](playlist-object.md) contenente elementi multimediali con il genere specificato.                                                            |
| [getByName](mediacollection-getbyname.md)                                       | Recupera un oggetto [Playlist](playlist-object.md) contenente elementi multimediali con il nome specificato.                                                             |
| [getMediaAtom](mediacollection-getmediaatom.md)                                 | Recupera l'indice in corrispondenza del quale risiede una proprietà specificata all'interno del set di proprietà disponibili.                                                              |
| [getPlaylistByQuery](mediacollection-getplaylistbyquery.md)                     | Recupera un oggetto [Playlist contenente](playlist-object.md) oggetti [Multimediali](media-object.md) che soddisfano le condizioni di query.                               |
| [getStringCollectionByQuery](mediacollection-getstringcollectionbyquery.md)     | Recupera un oggetto [StringCollection contenente](stringcollection-object.md) stringhe che soddisfano le condizioni di query.                                         |
| [isDeleted](mediacollection-isdeleted.md)                                       | Recupera un valore che indica se l'elemento multimediale specificato si trova nella cartella degli elementi eliminati.                                                                  |
| [remove](mediacollection-remove.md)                                             | Rimuove un elemento dalla raccolta di supporti.                                                                                                                     |
| [setDeleted](mediacollection-setdeleted.md)                                     | Sposta l'elemento multimediale specificato nella cartella degli elementi eliminati.                                                                                                    |



 

È **possibile accedere all'oggetto MediaCollection** tramite la proprietà seguente.



| Oggetto                      | Proprietà                                      |
|-----------------------------|-----------------------------------------------|
| [Player](player-object.md) | [mediaCollection](player-mediacollection.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




