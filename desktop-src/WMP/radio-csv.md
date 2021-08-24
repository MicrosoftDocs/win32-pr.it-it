---
title: radio.csv
description: radio.csv
ms.assetid: 8b0a1852-b6c9-4598-b1ab-c679362794b3
keywords:
- Windows Media Player negozi online, radio.csv
- negozi online, radio.csv
- Tipo 1 di negozi online, radio.csv
- radio.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b473bfaa960dd499fae7eb309d02ccbd693b70061d0975c58357bd72e9dcc410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002941"
---
# <a name="radiocsv"></a>radio.csv

Questo file contiene voci per ogni feed radio incluso nel catalogo. Ogni voce è una riga composta dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

La colonna Formato nella tabella seguente descrive il modo in cui viene formattato ogni campo di testo Unicode. Non fa riferimento al tipo di dati del contenuto. Ad esempio, se Nella colonna Formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



| Campo              | Necessario | Formato                                                                                                               | Descrizione                                                                                                                        |
|--------------------|----------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| RadioID            | Sì      | Intero non negativo.                                                                                                | ID per il feed radio univoco all'interno radio.csv.                                                                             |
| RadioTitle         | Sì      | Stringa Unicode. Esempio: Riscontri essenziali<br/>                                                                    | Titolo del feed di radio.                                                                                                                  |
| RadioSubtitle      | No       | Stringa Unicode. Esempio: Top 40.                                                                                     | Sottotitolo del feed radio. Spesso un nome di genere o di sottogenere.                                                                               |
| Programmatore         | Sì      | Stringa Unicode. Esempio: Terri Lee Duffy                                                                             | Nome del programmatore del feed radio. È consigliabile che questo campo non superi i 32 caratteri.                                     |
| PrimaryGenre       | Sì      | Intero non negativo.                                                                                                | ID del genere primario. È consentito un solo valore.                                                                            |
| Umore               | Sì      | Stringa Unicode. Esempio: Fun; amiable; energetico; <a0>T:System. Esuberante<br/>                                       | Una serie di aggettivi che descrivono la musica. Nessun punto e virgola finale dopo l'ultimo aggettivo.                                    |
| Category           | Sì      | Stringa Unicode                                                                                                       | Non usato in questa versione. Deve essere vuoto.                                                                                         |
| Descrizione        | No       | Stringa Unicode. Esempio: musica allestita per le parti degli artisti provati e veri che non saranno delusi.<br/> | Descrizione descrittiva per la visualizzazione nelle pagine delle proprietà. È consigliabile che questo campo non superi i 256 caratteri.                   |
| Popolarità         | Sì      | Intero non negativo o valore decimale. Esempio: 31<br/>                                                         | Classifica di popolarità tra i feed radio. Può essere 0.                                                                                    |
| StarRating         | No       | Float.Example: 3.21<br/>                                                                                       | facoltativo. Il valore, in genere compreso tra 0 e 5, viene arrotondato al più vicino 1/4 per la visualizzazione nell'interfaccia utente.                   |
| IsSubscriptionOnly | Sì      | Proprietà di tipo Boolean. Può essere 0 o 1.                                                                                              | Indica se il feed è disponibile solo per sottoscrizione.                                                                      |
| IsRecentlyAdded    | Sì      | Proprietà di tipo Boolean. Può essere 0 o 1.                                                                                              | Indica se il feed è stato aggiunto di recente.                                                                                    |
| IsFeatured         | Sì      | Proprietà di tipo Boolean. Può essere 0 o 1.                                                                                              | Indica se il feed è in primo piano.                                                                                            |
| EditorialGlyph     | Sì      | Intero non negativo. Deve essere 0.                                                                                   | Non usato in questa versione. Deve essere 0.                                                                                             |
| SortOrderRank      | Sì      | Intero non negativo.                                                                                                | Può essere usato per determinare l'ordinamento quando tutte le stazioni sono elencate nell'interfaccia utente. Deve essere 0 se questo campo non viene usato. |



 

 

 





