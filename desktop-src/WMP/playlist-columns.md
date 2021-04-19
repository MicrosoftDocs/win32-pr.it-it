---
title: PLAYLIST. Columns
description: L'attributo Columns definisce le colonne visualizzate nell'elemento PLAYLIST.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- PLAYLIST. Columns Media Player Windows
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325998"
---
# <a name="playlistcolumns"></a>PLAYLIST. Columns

L'attributo **Columns** definisce le colonne visualizzate nell'elemento **playlist** .

``` syntax
        elementID.columns
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura nel formato seguente:

\_nome database = nome DEscrittivo \_ ; \_ nome database = nome descrittivo \_ ;

Nome descrittivo \_ è il valore visualizzato nell'intestazione di colonna dell'elemento playlist e il \_ nome del database è un valore della tabella seguente. Si noti che un elemento della playlist può essere un elemento multimediale dalla libreria o da un CD oppure può essere un'altra **playlist** creata dall'utente o ricavata da un CD. Alcune colonne sono valide solo con determinati elementi della playlist come indicato nella colonna Descrizione.



| Valore             | Descrizione                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| Album             | Nome dell'album. Utilizzato solo con elementi multimediali.                                                                      |
| Artista            | Nome dell'artista. Non usato con le playlist create dall'utente.                                                           |
| Autore            | Nome dell'artista.                                                                                                 |
| Bitrate           | Velocità in bit del contenuto. Utilizzato solo con gli elementi multimediali della libreria.                                               |
| CDTrackEnabled    | Indica se la traccia del CD è abilitata. Utilizzato solo con gli elementi multimediali CD.                                               |
| Selezionata           | Riservato per utilizzi futuri.                                                                                                |
| Copyright         | Copyright della playlist. Non usato con playlist CD o elementi multimediali.                                               |
| CreationDate      | Data e ora di creazione della voce nella libreria. Utilizzato solo con gli elementi della libreria.                     |
| DigitallySecure   | Indica se l'elemento è protetto con Windows Media Rights Manager. Utilizzato solo con gli elementi multimediali della libreria. |
| Duration          | Durata dell'elemento multimediale.                                                                                         |
| FileType          | Riservato per utilizzi futuri.                                                                                                |
| Genre             | Genere della playlist. Non usato con playlist da CDs.                                                            |
| MediaAttribute    | Riservato per utilizzi futuri.                                                                                                |
| MediaType         | Tipo di elemento multimediale (audio o video).                                                                            |
| Metadatasource    | Origine dei metadati per questa traccia CD (AMG, WindowsMedia.com e così via). Utilizzato solo con gli elementi multimediali CD.         |
| ModifiedBy        | Riservato per utilizzi futuri.                                                                                                |
| Nome              | Nome della playlist.                                                                                               |
| OriginalIndex     | Se applicabile, l'identificatore di traccia CD corrispondente. Utilizzato solo con gli elementi multimediali CD.                                    |
| PlayCount         | Il numero di volte in cui il contenuto è stato riprodotto fino alla fine. Utilizzato solo con gli elementi multimediali della libreria.        |
| PlaylistAttribute | Riservato per utilizzi futuri.                                                                                                |
| Classificazione            | Riservato per utilizzi futuri.                                                                                                |
| SourceURL         | Percorso o URL del contenuto. Utilizzato solo con gli elementi multimediali della libreria.                                            |
| Stato            | Stato di copia di una traccia CD da copiare. Utilizzato solo con gli elementi multimediali CD.                                           |
| Stile             | Riservato per utilizzi futuri.                                                                                                |
| Sommario               | Se applicabile, l'identificatore della tabella di contenuti CD corrispondente. Non usato con le playlist create dall'utente.                 |



 

## <a name="remarks"></a>Commenti

Se una delle colonne non esiste nella libreria, viene lasciata vuota.

È possibile specificare un massimo di 31 colonne.

Se si specifica una colonna duplicata, i dati nella prima colonna verranno allineati a sinistra, ma tutte le altre colonne duplicate verranno allineate a destra. Se, ad esempio, sono presenti due colonne Duration, i dati verranno allineati a sinistra nel primo e allineati a destra nel secondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. columnsVisible**](playlist-columnsvisible.md)
</dt> </dl>

 

 





