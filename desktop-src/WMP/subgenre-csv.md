---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player Online Stores, subgenre.csv
- archivi online, subgenre.csv
- digitare 1 Store online, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298744"
---
# <a name="subgenrecsv"></a>subgenre.csv

Questo file contiene una voce per ogni sottogenere rappresentato nel catalogo. Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode. Non si riferisce al tipo di dati del contenuto. Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo             | Necessario | Formato                                                                                            | Descrizione                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SubGenreID        | Sì      | Integer non negativo.                                                                             | Identificatore (ID) del sottogenere, univoco all'interno subgenre.csv. Sono consentiti fino a 1024 sottogeneri.                                                                   |
| SubGenreTitle     | Sì      | Stringa Unicode. Esempio: Intelligent Dance Music (IDM)<br/>                                  | Nome visualizzato del sottogenere.                                                                                                                                    |
| SubGenreSubtitle  | No       | Stringa Unicode. Esempio: nuovo, musica elettronica a percussione che non è un techno puro.<br/> | Descrive il significato del nome visualizzato del sottogenere. Deve essere minore di 64 caratteri.                                                                     |
| FeedsAreAvailable | Sì      | Boolean. Format: \[ 0 \| 1\]<br/> Esempio: 0<br/>                                         | Indica se è possibile eseguire la radioriproduzione eseguendo il passaggio a un feed.                                                                                          |
| \_GenreID collegato   | Sì      | Integer non negativo (GenreID). Esempio: 12<br/>                                             | GenreID del genere padre. È consentito un solo elemento padre.                                                                                              |
| SortOrderRank     | Sì      | Integer non negativo. Esempio: 23<br/>                                                       | Classificazione, idealmente univoca, utilizzata per l'ordinamento dei sottogeneri nell'interfaccia utente. Se il genere padre ha 10 sottogeneri, potrebbe trattarsi di un numero intero compreso tra 1 e 10. |



 

 

 





