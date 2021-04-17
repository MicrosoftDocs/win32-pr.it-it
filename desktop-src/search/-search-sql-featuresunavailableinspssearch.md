---
description: Il linguaggio di query di Microsoft Windows Search è basato su Structured Query Language (SQL); Tuttavia, non esegue la ricerca in un database relazionale con indici o tabelle definite dall'utente.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Funzionalità SQL non disponibili in Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306131"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>Funzionalità SQL non disponibili in Microsoft Windows Search

Il linguaggio di query di Microsoft Windows Search è basato su Structured Query Language (SQL); Tuttavia, non esegue la ricerca in un database relazionale con indici o tabelle definite dall'utente. Per questo motivo, molte istruzioni SQL standard e funzionalità di sintassi non si applicano. Di seguito è riportato un elenco delle funzionalità SQL più significative che non sono supportate in Windows Search.


-   Istruzioni BATCH
-   Funzione COALESCE \_ Table
-   Funzione CONVERT (usare invece le funzioni CAST)
-   CREATE VIEW - istruzione
-   Linguaggio di definizione dei dati
-   DATASOURCE (istruzione)
-   Formati di data e ora diversi dall'indicatore di data e ora ISO
-   Istruzione DELETE
-   GRANT - istruzione
-   Schema informazioni
-   Istruzione INSERT
-   Tipi di dati OLE DB
-   Espressioni regolari SQL-standard (usare invece CONTAINs o LIKE)
-   Parametri per le query SQL
-   Confronto tra colonne relazionali
-   Intestazione ID Revisione
-   REVOKE - istruzione
-   Alias di ambito o numeri di Revisione
-   Seleziona tutto (rimuove automaticamente i duplicati)
-   Stored procedure
-   Espansione di documenti strutturati
-   UNION ALL
-   Parola chiave UNKNOWN
-   Istruzione UPDATE

Windows Search non supporta il thesaurus e le parole non significative.

 

 



