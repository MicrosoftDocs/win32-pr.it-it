---
title: album.csv
description: album.csv
ms.assetid: 7308e849-7227-480e-937a-8e9091bdec98
keywords:
- Windows Media Player Online Stores, album.csv
- archivi online, album.csv
- digitare 1 Store online, album.csv
- album.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f8b71dc080e6983817d4e6f146249875887ed9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298027"
---
# <a name="albumcsv"></a>album.csv

Questo file contiene una voce per ogni album incluso nel catalogo. Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

Tutti i campi nel album.csv sono obbligatori.

La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode. Non si riferisce al tipo di dati del contenuto. Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo             | Formato                                                                   | Descrizione                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlbumID           | Integer non negativo. Esempio: 789456<br/>                          | Identificatore per l'album, univoco all'interno album.csv. Deve essere minore di 2 ^ 32.                                                                                                                                                                           |
| AlbumName         | Stringa Unicode. Esempio: risultati più grandi<br/>                         | Titolo album                                                                                                                                                                                                                                          |
| AlbumArtist       | Integer non negativo. Esempio: 34331<br/>                           | ArtistID dell'artista. È consentito un solo valore. Può essere l'ID di "vari artisti" o simili.                                                                                                                                                    |
| AlbumLabel        | Stringa Unicode. Deve essere vuoto.                                         | Non utilizzato in questa versione. Deve essere vuoto.                                                                                                                                                                                                           |
| ReleaseDate       | Stringa Unicode, nel formato AAAA-MM-GG. Esempio: 2005-0-0<br/>        | Data di rilascio. Il valore 0 è consentito per il giorno o il mese.                                                                                                                                                                                               |
| AlbumPrice        | StringExample Unicode: $12,49<br/>                                 | Prezzo dell'album. È necessario includere il simbolo di valuta. La stringa vuota, 0 e-hanno un significato speciale. Una stringa vuota indica un prezzo sconosciuto. ' 0' indica che la traccia è gratuita. Un trattino ('-') indica che non è possibile acquistare l'album. |
| LinkedGenreID     | Integer non negativo. Esempio: 12<br/>                              | ID del genere principale per l'album. È consentito un solo valore.                                                                                                                                                                                        |
| LinkedSubGenreIDs | Formato: n; n; n; Esempio: 32; 44; 663;<br/>                             | Elenco di ID di sottogenere associati. Alla fine dell'elenco è consentito un punto e virgola finale.                                                                                                                                                             |
| Popolarità        | Può essere un numero intero non negativo o un valore decimale. Esempio: 1256,24<br/> | Classificazione di popolarità determinata dal servizio. Può essere la classificazione di questo album nell'elenco di album ordinati in base alla popolarità. 0 è consentito.                                                                                                              |
| IsRecentlyAdded   | Proprietà di tipo Boolean. Può essere 0 o 1.                                                  | Flag che indica che l'album è stato aggiunto di recente, come determinato dal servizio.                                                                                                                                                                    |
| Funzionalità di        | Proprietà di tipo Boolean. Può essere 0 o 1.                                                  | Flag per indicare che si tratta di un album in primo piano.                                                                                                                                                                                                      |
| EditorialGlyph    | Integer non negativo. Deve essere 0.                                       | Non usato è la versione. Deve essere 0.                                                                                                                                                                                                                    |
| FeedsAreAvailable | Proprietà di tipo Boolean. Può essere 0 o 1.                                                  | Non utilizzato in questa versione. Deve essere 0.                                                                                                                                                                                                               |



 

 

 





