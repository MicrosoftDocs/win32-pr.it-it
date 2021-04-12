---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Windows Media Player Online Stores, genre.csv
- archivi online, genre.csv
- digitare 1 Store online, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955680"
---
# <a name="genrecsv"></a>genre.csv

Questo file contiene una voce per ogni genere rappresentato nel catalogo. Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

Tutti i campi nel genre.csv sono obbligatori.

La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode. Non si riferisce al tipo di dati del contenuto. Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo             | Formato                                                    | Descrizione                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ID genere         | Integer non negativo. Esempio: 22<br/>               | Identificatore del genere, univoco all'interno genre.csv. Deve essere minore di 2 ^ 32. È possibile ottenere un massimo di 64 generi.                                             |
| GenreTitle        | Stringa Unicode. Esempio: Rock<br/>                   | Nome visualizzato del genere.                                                                                                                                |
| FeedsAreAvailable | Boolean. Format: \[ 0 \| 1\]<br/> Esempio: 0<br/> | Indica se è possibile utilizzare il comportamento "Radio Play" passando a un feed.                                                                          |
| HasComposer       | Boolean. Format: \[ 0 \| 1\]<br/> Esempio: 1<br/> | True se questo genere deve salvare le informazioni del Composer nel catalogo. Se non è impostato, le informazioni del Composer vengono ignorate e non vengono compilate nel catalogo. |



 

 

 





