---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player negozi online, artist.csv
- negozi online, artist.csv
- tipo 1 negozi online, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4192d0817740ac872d1c08989f2f57b4715d65fea6b9a6c9a199dcdabe267e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583043"
---
# <a name="artistcsv"></a>artist.csv

Questo file contiene una voce per ogni artista nel catalogo. Ogni voce è una riga composta dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

Tutti i campi artist.csv obbligatori.

La colonna Formato nella tabella seguente descrive il modo in cui viene formattato ogni campo di testo Unicode. Non fa riferimento al tipo di dati del contenuto. Ad esempio, se Nella colonna Formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo                  | Formato                                            | Descrizione                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ID artista               | Intero non negativo. Esempio: 65832              | Identificatore univoco dell'artista, univoco all'interno artist.csv. Deve essere minore di 2^32.                        |
| ArtistName             | Stringa Unicode. Esempio: Don Funk<br/>       | Nome visualizzato per l'artista.                                                                               |
| LinkedGenreID          | Intero non negativo. Esempio: 313<br/>      | GenreID del genere principale dell'artista. Deve essere un genere principale e non un sottogenere. È consentito un solo valore. |
| LinkedSimilarArtistIDs | N/A                                               | Non usato in questa versione. Deve essere vuoto.                                                                 |
| Popolarità             | Può essere un valore intero o decimale. Esempio: 1252.25 | Classifica di popolarità. Può essere la posizione nell'elenco se ordinata in base alla popolarità.                             |
| FeedAvailable         | Proprietà di tipo Boolean. Formato: \[ 0 \| 1 \] Esempio: 0<br/>    | Non usato in questa versione. Deve essere vuoto.                                                                 |



 

 

 





