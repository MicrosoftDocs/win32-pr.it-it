---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player negozi online, subgenre.csv
- negozi online, subgenre.csv
- Tipo 1 di negozi online, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10242e955423d75174d04899285dcd3dc20ea2ea4a761d2ab3ba53561c4d41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122941"
---
# <a name="subgenrecsv"></a>subgenre.csv

Questo file contiene una voce per ogni sottogenere rappresentato nel catalogo. Ogni voce è una riga composta dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

La colonna Formato nella tabella seguente descrive il modo in cui viene formattato ogni campo di testo Unicode. Non fa riferimento al tipo di dati del contenuto. Ad esempio, se Nella colonna Formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo             | Necessario | Formato                                                                                            | Descrizione                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SubGenreID        | Sì      | Intero non negativo.                                                                             | Identificatore di sottogenere (ID), univoco all'interno subgenre.csv. Sono consentiti fino a 1024 sottogeneri.                                                                   |
| SubGenreTitle     | Sì      | Stringa Unicode. Esempio: Intelligent Dance Musica (IDM)<br/>                                  | Nome visualizzato della sottogenere.                                                                                                                                    |
| SubGenreSubtitle  | No       | Stringa Unicode. Esempio: musica elettronica nuova e percussiva che non è una tecnica pura.<br/> | Descrivere il significato del nome visualizzato della sottogenere. Deve contenere meno di 64 caratteri.                                                                     |
| FeedAreAvailable | Sì      | Boolean.Format: \[ 0 \| 1\]<br/> Esempio: 0<br/>                                         | Indica se la riproduzione radio è possibile tramite il passaggio a un feed.                                                                                          |
| GenreID \_ collegato   | Sì      | Intero non negativo (GenreID). Esempio: 12<br/>                                             | GenreID del genere padre. È consentito un solo elemento padre.                                                                                              |
| SortOrderRank     | Sì      | Intero non negativo. Esempio: 23<br/>                                                       | Classificazione, idealmente univoca, usata per ordinare i sottogeneri nell'interfaccia utente. Se il genere padre ha 10 sottogeneri, potrebbe essere un numero intero compreso tra 1 e 10. |



 

 

 





