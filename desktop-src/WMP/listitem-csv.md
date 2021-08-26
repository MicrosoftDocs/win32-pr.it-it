---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Windows Media Player online store,listitem.csv
- online store, listitem.csv
- digitare 1 online stores,listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6894bb30cac5dfc30ce2e98a91965de193611420291be301e3e5c06dd5509d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003373"
---
# <a name="listitemcsv"></a>listitem.csv

Questo file contiene voci per ogni elemento incluso in un elenco. Ogni voce è una riga composta dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

Tutti i campi sono obbligatori.

La colonna Formato nella tabella seguente descrive il modo in cui viene formattato ogni campo di testo Unicode. Non fa riferimento al tipo di dati del contenuto. Ad esempio, se nella colonna Formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un intero effettivo.



| Campo              | Formato                                          | Descrizione                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| ListID \_ collegato     | Intero non negativo. Esempio: 465<br/>    | ID dell'elenco di cui fa parte questo elemento.                                                                               |
| ListItem \_ collegato   | Intero non negativo. Esempio: 684793<br/> | ID dell'elemento. Può essere l'ID di una traccia, un album, un artista, un genere, un sottogenere, un feed radio o un altro elenco. |
| ItemPositionInList | Intero non negativo. Esempio: 5<br/>      | Posizione dell'elemento all'interno del relativo elenco. Il primo elemento di un elenco si trova nella posizione 0.                                   |



 

 

 





