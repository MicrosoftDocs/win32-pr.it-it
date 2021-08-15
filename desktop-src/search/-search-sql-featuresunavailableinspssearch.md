---
description: Il linguaggio di query di Ricerca di Microsoft Windows è basato Structured Query Language (SQL); tuttavia non esegue la ricerca in un database relazionale con indici o tabelle definite dall'utente.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: SQL Funzionalità non disponibili in Microsoft Windows Ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66adb175aa7fae799e0ad9b69916415f12c94ee984d276b5a2238ebb19ec2f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716121"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>SQL Funzionalità non disponibili in Microsoft Windows Ricerca

Il linguaggio di query di Ricerca di Microsoft Windows è basato Structured Query Language (SQL); tuttavia non esegue la ricerca in un database relazionale con indici o tabelle definite dall'utente. Per questo problema, molte istruzioni SQL standard e funzionalità di sintassi non sono applicabili. Di seguito è riportato un elenco delle funzionalità più SQL funzionalità non supportate in Windows ricerca.


-   Istruzioni BATCH
-   Funzione COALESCE \_ TABLE
-   Funzione CONVERT (usare invece le funzioni CAST)
-   CREATE VIEW - istruzione
-   Linguaggio di definizione dei dati
-   Istruzione DATASOURCE
-   Formati di data e ora diversi dal timestamp e dalla data ISO
-   Istruzione DELETE
-   GRANT - istruzione
-   Schema delle informazioni
-   Istruzione INSERT
-   OLE DB tipi di dati
-   SQL espressioni regolari standard (usare INVECE CONTAINS o LIKE)
-   Parametri per SQL query
-   Confronto tra colonne relazionali
-   Intestazione ID revisione
-   REVOKE - istruzione
-   Alias SCOPE o numeri di revisione
-   SELECT ALL (rimuove automaticamente i duplicati)
-   Stored procedure
-   Espansione di documenti strutturati
-   UNION ALL
-   Unknown ( parola chiave)
-   Istruzione UPDATE

Windows La ricerca non supporta il thesaurus e le parole non pronunciate.

 

 



