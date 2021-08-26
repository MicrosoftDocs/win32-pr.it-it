---
title: album.csv
description: album.csv
ms.assetid: 7308e849-7227-480e-937a-8e9091bdec98
keywords:
- Windows Media Player negozi online, album.csv
- negozi online, album.csv
- Tipo 1 di negozi online, album.csv
- album.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750926a3d01f8d65d7ed11c69436049e39ea3dabf0e446ede8a8c9dcecc53bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004201"
---
# <a name="albumcsv"></a>album.csv

Questo file contiene una voce per ogni album incluso nel catalogo. Ogni voce è una riga composta dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

Tutti i campi album.csv obbligatori.

La colonna Formato nella tabella seguente descrive il modo in cui viene formattato ogni campo di testo Unicode. Non fa riferimento al tipo di dati del contenuto. Ad esempio, se Nella colonna Formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo             | Formato                                                                   | Descrizione                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlbumID           | Intero non negativo. Esempio: 789456<br/>                          | Identificatore per l'album, univoco all'interno album.csv. Deve essere minore di 2^32.                                                                                                                                                                           |
| AlbumName         | Stringa Unicode. Esempio: Greatest Hits<br/>                         | Titolo dell'album                                                                                                                                                                                                                                          |
| AlbumArtist       | Intero non negativo. Esempio: 34331<br/>                           | ArtistID dell'artista. È consentito un solo valore. Può essere l'ID di "Vari artisti" o simile.                                                                                                                                                    |
| AlbumLabel        | Stringa Unicode. Deve essere vuoto.                                         | Non usato in questa versione. Deve essere vuoto.                                                                                                                                                                                                           |
| ReleaseDate       | Stringa Unicode, nel formato AAAAA-MM-GG. Esempio: 2005-0-0<br/>        | Data di rilascio. Il valore 0 è consentito per giorno o mese.                                                                                                                                                                                               |
| AlbumPrice        | Stringa UnicodeEseple: $12.49<br/>                                 | Prezzo dell'album. Il simbolo di valuta deve essere incluso. La stringa vuota, 0 e - hanno un significato speciale. Una stringa vuota indica un prezzo sconosciuto. "0" indica che la traccia è gratuita. Un trattino ('-') indica che l'album non può essere acquistato. |
| LinkedGenreID     | Intero non negativo. Esempio: 12<br/>                              | ID del genere primario per l'album. È consentito un solo valore.                                                                                                                                                                                        |
| LinkedSubGenreIDs | Formato: n;n;n; Esempio: 32;44;663;<br/>                             | Elenco di ID sottogenere associati. Alla fine dell'elenco è consentito un punto e virgola finale.                                                                                                                                                             |
| Popolarità        | Può essere un numero intero non negativo o un valore decimale. Esempio: 1256.24<br/> | Classificazione di popolarità determinata dal servizio. Può essere la classificazione di questo album nell'elenco di album ordinati in base alla popolarità. 0 è consentito.                                                                                                              |
| IsRecentlyAdded   | Proprietà di tipo Boolean. Può essere 0 o 1.                                                  | Flag per indicare che l'album è stato aggiunto di recente, come determinato dal servizio.                                                                                                                                                                    |
| IsFeatured        | Proprietà di tipo Boolean. Può essere 0 o 1.                                                  | Flag per indicare che si tratta di un album in primo piano.                                                                                                                                                                                                      |
| EditorialGlyph    | Intero non negativo. Deve essere 0.                                       | Non usato è release. Deve essere 0.                                                                                                                                                                                                                    |
| FeedAreAvailable | Proprietà di tipo Boolean. Può essere 0 o 1.                                                  | Non usato in questa versione. Deve essere 0.                                                                                                                                                                                                               |



 

 

 





