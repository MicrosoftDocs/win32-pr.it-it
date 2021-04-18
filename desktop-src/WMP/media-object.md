---
title: Oggetto multimediale
description: L'oggetto multimediale fornisce un modo per specificare o recuperare le proprietà di un elemento multimediale, usando le proprietà e i metodi seguenti.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Media Player di oggetti multimediali di Windows
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88eff6ee0a97e63df6a0c073ef18425cbb576e85
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299137"
---
# <a name="media-object"></a>Oggetto multimediale

L'oggetto **multimediale** fornisce un modo per specificare o recuperare le proprietà di un elemento multimediale, usando le proprietà e i metodi seguenti.

L'oggetto **multimediale** supporta le seguenti proprietà.



| Proprietà                                         | Descrizione                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [attributeCount](media-attributecount.md)       | Recupera il numero di attributi su cui è possibile eseguire query e/o impostare per l'elemento multimediale.              |
| [duration](media-duration.md)                   | Recupera la durata in secondi dell'elemento multimediale corrente.                                       |
| [durationString](media-durationstring.md)       | Recupera un valore **stringa** che indica la durata dell'elemento multimediale corrente nel formato HH: mm: SS. |
| [error](media-error.md)                         | Recupera un oggetto [ErrorItem](erroritem-object.md) se l'elemento multimediale presenta una condizione di errore.    |
| [imageSourceHeight](media-imagesourceheight.md) | Recupera l'altezza in pixel dell'elemento multimediale corrente.                                          |
| [imageSourceWidth](media-imagesourcewidth.md)   | Recupera la larghezza dell'elemento multimediale corrente in pixel.                                           |
| [markerCount](media-markercount.md)             | Recupera il numero di marcatori nell'elemento multimediale.                                                 |
| [nome](media-name.md)                           | Specifica o Recupera il nome dell'elemento multimediale.                                                 |
| [sourceURL](media-sourceurl.md)                 | Recupera l'URL dell'elemento multimediale.                                                               |



 

L'oggetto **multimediale** supporta i metodi seguenti.



| Metodo                                                       | Descrizione                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](media-getattributecountbytype.md) | Recupera il numero di attributi associati al nome di attributo e alla lingua specificati.            |
| [getAttributeName](media-getattributename.md)               | Recupera il nome dell'attributo corrispondente all'indice specificato.                                |
| [getItemInfo](media-getiteminfo.md)                         | Recupera il valore dell'attributo specificato per l'elemento multimediale.                                       |
| [getItemInfoByAtom](media-getiteminfobyatom.md)             | Recupera il valore dell'attributo con il numero di indice specificato.                                    |
| [getItemInfoByType](media-getiteminfobytype.md)             | Recupera il valore dell'attributo corrispondente al nome dell'attributo, alla lingua e all'indice specificati. |
| [getmarcatore](media-getmarkername.md)                     | Recupera il nome del marcatore in corrispondenza dell'indice specificato.                                                 |
| [getMarkerTime](media-getmarkertime.md)                     | Recupera l'ora del marcatore in corrispondenza dell'indice specificato.                                                 |
| [Identico](media-isidentical.md)                         | Recupera un valore che indica se l'oggetto fornito è uguale a quello corrente.                 |
| [isMemberOf](media-ismemberof.md)                           | Recupera un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.     |
| [isReadOnlyItem](media-isreadonlyitem.md)                   | Recupera un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.           |
| [setItemInfo](media-setiteminfo.md)                         | Imposta il valore dell'attributo specificato per l'elemento multimediale.                                            |



 

È possibile accedere all'oggetto **multimediale** tramite le proprietà e i metodi seguenti.



| Oggetto                          | Proprietà o metodo                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [Controlli](controls-object.md) | [currentItem](controls-currentitem.md)                                  |
| [Player](player-object.md)     | [currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md) |
| [Playlist](playlist-object.md) | [item](playlist-item.md)                                                |



 

Poiché si tratta del mezzo più comune di accesso, *Player*. **currentMedia** viene usato a scopo illustrativo nelle sezioni della sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




