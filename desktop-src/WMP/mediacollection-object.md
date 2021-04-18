---
title: Mediacollection (oggetto)
description: L'oggetto Mediacollection consente di organizzare un'ampia raccolta di elementi multimediali. È possibile eseguire query su di essa per generare automaticamente playlist.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Media Player finestre oggetti mediacollection
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299209"
---
# <a name="mediacollection-object"></a>Mediacollection (oggetto)

L'oggetto **mediacollection** consente di organizzare un'ampia raccolta di elementi multimediali. È possibile eseguire query su di essa per generare automaticamente playlist.

L'oggetto **mediacollection** supporta i metodi seguenti.



| Metodo                                                                           | Descrizione                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [add](mediacollection-add.md)                                                   | Aggiunge un nuovo elemento multimediale o una playlist alla raccolta.                                                                                                              |
| [createQuery](mediacollection-createquery.md)                                   | Crea un nuovo oggetto [query](query-object.md) .                                                                                                                |
| [getAll](mediacollection-getall.md)                                             | Recupera un oggetto [playlist](playlist-object.md) contenente tutti gli elementi multimediali nella libreria.                                                                  |
| [getAttributeStringCollection](mediacollection-getattributestringcollection.md) | Recupera un oggetto [StringCollection](stringcollection-object.md) che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto specificato. |
| [getByAlbum](mediacollection-getbyalbum.md)                                     | Recupera un oggetto [playlist](playlist-object.md) contenente elementi multimediali dall'album specificato.                                                            |
| [getByAttribute](mediacollection-getbyattribute.md)                             | Recupera un oggetto [playlist](playlist-object.md) contenente gli elementi multimediali con l'attributo specificato con il valore specificato.                             |
| [getByAttributeAndMediaType](mediacollection-getbyattributeandmediatype.md)     | Recupera un oggetto [playlist](playlist-object.md) contenente oggetti [multimediali](media-object.md) con l'attributo e il tipo di supporto specificati.                 |
| [getByAuthor](mediacollection-getbyauthor.md)                                   | Recupera un oggetto [playlist](playlist-object.md) contenente elementi multimediali dall'autore specificato.                                                             |
| [getByGenre](mediacollection-getbygenre.md)                                     | Recupera un oggetto [playlist](playlist-object.md) contenente elementi multimediali con il genere specificato.                                                            |
| [getByName](mediacollection-getbyname.md)                                       | Recupera un oggetto [playlist](playlist-object.md) contenente elementi multimediali con il nome specificato.                                                             |
| [getMediaAtom](mediacollection-getmediaatom.md)                                 | Recupera l'indice in corrispondenza del quale si trova una proprietà specificata nel set di proprietà disponibili.                                                              |
| [getPlaylistByQuery](mediacollection-getplaylistbyquery.md)                     | Recupera un oggetto [playlist](playlist-object.md) contenente oggetti [multimediali](media-object.md) che corrispondono alle condizioni della query.                               |
| [getStringCollectionByQuery](mediacollection-getstringcollectionbyquery.md)     | Recupera un oggetto [StringCollection](stringcollection-object.md) contenente stringhe corrispondenti alle condizioni della query.                                         |
| [isDeleted](mediacollection-isdeleted.md)                                       | Recupera un valore che indica se l'elemento multimediale specificato si trova nella cartella elementi eliminati.                                                                  |
| [remove](mediacollection-remove.md)                                             | Rimuove un elemento dall'insieme di supporti.                                                                                                                     |
| [Eliminata](mediacollection-setdeleted.md)                                     | Sposta l'elemento multimediale specificato nella cartella elementi eliminati.                                                                                                    |



 

È possibile accedere all'oggetto **mediacollection** tramite la proprietà seguente.



| Oggetto                      | Proprietà                                      |
|-----------------------------|-----------------------------------------------|
| [Player](player-object.md) | [mediacollection](player-mediacollection.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




