---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player Online Stores, artist.csv
- archivi online, artist.csv
- digitare 1 Store online, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332428"
---
# <a name="artistcsv"></a>artist.csv

Questo file contiene una voce per ogni artista nel catalogo. Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

Tutti i campi nel artist.csv sono obbligatori.

La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode. Non si riferisce al tipo di dati del contenuto. Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo                  | Formato                                            | Descrizione                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ArtistID               | Integer non negativo. Esempio: 65832              | Identificatore univoco per l'artista, univoco all'interno artist.csv. Deve essere minore di 2 ^ 32.                        |
| ArtistName             | Stringa Unicode. Esempio: Don Funk<br/>       | Nome visualizzato per l'artista.                                                                               |
| LinkedGenreID          | Integer non negativo. Esempio: 313<br/>      | GenreID del genere principale dell'artista. Deve essere un genere principale e non un sottogenere. È consentito un solo valore. |
| LinkedSimilarArtistIDs | N/D                                               | Non utilizzato in questa versione. Deve essere vuoto.                                                                 |
| Popolarità             | Può essere un valore intero o decimale. Esempio: 1252,25 | Classificazione della popolarità. Può essere la posizione nell'elenco quando è ordinata in base alla popolarità.                             |
| FeedsAvailable         | Proprietà di tipo Boolean. Formato: \[ 0 \| 1 \] esempio: 0<br/>    | Non utilizzato in questa versione. Deve essere vuoto.                                                                 |



 

 

 





