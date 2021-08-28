---
title: Oggetto multimediale
description: L'oggetto Media consente di specificare o recuperare le proprietà di un elemento multimediale, usando le proprietà e i metodi seguenti.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Oggetto multimediale Windows Media Player
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c1dbcb3dc662a431f279e03697620b80c242c99eb32e3bbcdc26d71796f7e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123311"
---
# <a name="media-object"></a>Oggetto multimediale

**L'oggetto** Media consente di specificare o recuperare le proprietà di un elemento multimediale, usando le proprietà e i metodi seguenti.

**L'oggetto** Media supporta le proprietà seguenti.



| Proprietà                                         | Descrizione                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [attributeCount](media-attributecount.md)       | Recupera il numero di attributi che possono essere sottoposti a query e/o impostati per l'elemento multimediale.              |
| [duration](media-duration.md)                   | Recupera la durata in secondi dell'elemento multimediale corrente.                                       |
| [durationString](media-durationstring.md)       | Recupera un valore **String** che indica la durata dell'elemento multimediale corrente in formato HH:MM:SS. |
| [error](media-error.md)                         | Recupera un oggetto [ErrorItem](erroritem-object.md) se l'elemento multimediale presenta una condizione di errore.    |
| [imageSourceHeight](media-imagesourceheight.md) | Recupera l'altezza dell'elemento multimediale corrente in pixel.                                          |
| [imageSourceWidth](media-imagesourcewidth.md)   | Recupera la larghezza dell'elemento multimediale corrente in pixel.                                           |
| [markerCount](media-markercount.md)             | Recupera il numero di marcatori nell'elemento multimediale.                                                 |
| [nome](media-name.md)                           | Specifica o recupera il nome dell'elemento multimediale.                                                 |
| [sourceURL](media-sourceurl.md)                 | Recupera l'URL dell'elemento multimediale.                                                               |



 

**L'oggetto** Media supporta i metodi seguenti.



| Metodo                                                       | Descrizione                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](media-getattributecountbytype.md) | Recupera il numero di attributi associati al nome e alla lingua dell'attributo specificati.            |
| [getAttributeName](media-getattributename.md)               | Recupera il nome dell'attributo corrispondente all'indice specificato.                                |
| [getItemInfo](media-getiteminfo.md)                         | Recupera il valore dell'attributo specificato per l'elemento multimediale.                                       |
| [getItemInfoByAtom](media-getiteminfobyatom.md)             | Recupera il valore dell'attributo con il numero di indice specificato.                                    |
| [getItemInfoByType](media-getiteminfobytype.md)             | Recupera il valore dell'attributo corrispondente al nome dell'attributo, alla lingua e all'indice specificati. |
| [getMarkerName](media-getmarkername.md)                     | Recupera il nome del marcatore in corrispondenza dell'indice specificato.                                                 |
| [getMarkerTime](media-getmarkertime.md)                     | Recupera l'ora del marcatore in corrispondenza dell'indice specificato.                                                 |
| [isIdentical](media-isidentical.md)                         | Recupera un valore che indica se l'oggetto fornito corrisponde a quello corrente.                 |
| [isMemberOf](media-ismemberof.md)                           | Recupera un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.     |
| [isReadOnlyItem](media-isreadonlyitem.md)                   | Recupera un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.           |
| [setItemInfo](media-setiteminfo.md)                         | Imposta il valore dell'attributo specificato per l'elemento multimediale.                                            |



 

È **possibile** accedere all'oggetto Media tramite le proprietà e i metodi seguenti.



| Oggetto                          | Proprietà o metodo                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [Controlli](controls-object.md) | [Currentitem](controls-currentitem.md)                                  |
| [Player](player-object.md)     | [currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md) |
| [Playlist](playlist-object.md) | [item](playlist-item.md)                                                |



 

Poiché è il mezzo di accesso più *comune,* player . **currentMedia** viene usato a scopo illustrativo nelle sezioni relative alla sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




