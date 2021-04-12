---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Windows Media Player Online Stores, listitem.csv
- archivi online, listitem.csv
- digitare 1 Store online, listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395714"
---
# <a name="listitemcsv"></a>listitem.csv

Questo file contiene le voci per ogni elemento incluso in un elenco. Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

Tutti i campi sono obbligatori.

La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode. Non si riferisce al tipo di dati del contenuto. Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo              | Formato                                          | Descrizione                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| \_ListId collegato     | Integer non negativo. Esempio: 465<br/>    | ID dell'elenco di cui fa parte questo elemento.                                                                               |
| \_ListItem collegato   | Integer non negativo. Esempio: 684793<br/> | ID dell'elemento. Può essere l'ID di una traccia, un album, un artista, un genere, un sottogenere, un feed di radio o un altro elenco. |
| ItemPositionInList | Integer non negativo. Esempio: 5<br/>      | Posizione dell'elemento all'interno dell'elenco. Il primo elemento di un elenco è nella posizione 0.                                   |



 

 

 





