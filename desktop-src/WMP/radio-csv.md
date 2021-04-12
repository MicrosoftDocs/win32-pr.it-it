---
title: radio.csv
description: radio.csv
ms.assetid: 8b0a1852-b6c9-4598-b1ab-c679362794b3
keywords:
- Windows Media Player Online Stores, radio.csv
- archivi online, radio.csv
- digitare 1 Store online, radio.csv
- radio.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5271f3a87b32d27996f61e444723f537a09cb827
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331335"
---
# <a name="radiocsv"></a>radio.csv

Questo file contiene le voci per ogni feed di radio incluso nel catalogo. Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode. Non si riferisce al tipo di dati del contenuto. Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo              | Necessario | Formato                                                                                                               | Descrizione                                                                                                                        |
|--------------------|----------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| RadioID            | Sì      | Integer non negativo.                                                                                                | ID del feed di radio univoco all'interno radio.csv.                                                                             |
| Radiotitolo         | Sì      | Stringa Unicode. Esempio: riscontri essenziali<br/>                                                                    | Titolo del feed di radio.                                                                                                                  |
| RadioSubtitle      | No       | Stringa Unicode. Esempio: Top 40.                                                                                     | Sottotitolo del feed di radio. Spesso un nome di genere o di sottogenere.                                                                               |
| Programmatore         | Sì      | Stringa Unicode. Esempio: Terri Lee Duffy                                                                             | Nome del programmatore del feed di radio. È consigliabile che questo campo non superi 32 caratteri.                                     |
| PrimaryGenre       | Sì      | Integer non negativo.                                                                                                | ID del genere primario. È consentito un solo valore.                                                                            |
| Umore               | Sì      | Stringa Unicode. Esempio: Fun; amabile energico elegante esuberante<br/>                                       | Serie di aggettivi che descrivono la musica. Nessun punto e virgola finale dopo l'ultimo aggettivo.                                    |
| Category           | Sì      | Stringa Unicode                                                                                                       | Non utilizzato in questa versione. Deve essere vuoto.                                                                                         |
| Descrizione        | No       | Stringa Unicode. Esempio: un brano musicale descrittivo dagli artisti provati e veritieri che non sono delusi.<br/> | Descrizione descrittiva per la visualizzazione nelle pagine delle proprietà. È consigliabile che questo campo non superi 256 caratteri.                   |
| Popolarità         | Sì      | Valore integer o decimale non negativo. Esempio: 31<br/>                                                         | Classificazione della popolarità tra i feed radiofonici. Può essere 0.                                                                                    |
| StarRating         | No       | Float. esempio: 3,21<br/>                                                                                       | facoltativo. Il valore, in genere compreso tra 0 e 5, viene arrotondato al 1/4 più vicino per la visualizzazione nell'interfaccia utente.                   |
| IsSubscriptionOnly | Sì      | Proprietà di tipo Boolean. Può essere 0 o 1.                                                                                              | Indica se il feed è disponibile solo per la sottoscrizione.                                                                      |
| IsRecentlyAdded    | Sì      | Proprietà di tipo Boolean. Può essere 0 o 1.                                                                                              | Indica se il feed è stato aggiunto di recente.                                                                                    |
| Funzionalità di         | Sì      | Proprietà di tipo Boolean. Può essere 0 o 1.                                                                                              | Indica se il feed è in primo piano.                                                                                            |
| EditorialGlyph     | Sì      | Integer non negativo. Deve essere 0.                                                                                   | Non utilizzato in questa versione. Deve essere 0.                                                                                             |
| SortOrderRank      | Sì      | Integer non negativo.                                                                                                | Può essere utilizzato per determinare l'ordinamento quando tutte le stazioni sono elencate nell'interfaccia utente. Deve essere 0 se questo campo non viene utilizzato. |



 

 

 





