---
description: Le applicazioni possono usare PDH per estrarre i contatori delle prestazioni dai log SQL oppure possono estrarre contatori formattati o non elaborati direttamente dal database tramite SQL query.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL Log File Schema
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: a95026c478094d8e71a44c2c57e65c2fa7044b00e982ea43187244838beed2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143814"
---
# <a name="sql-log-file-schema"></a>SQL Log File Schema

> [!IMPORTANT]
> Il supporto PDH per i SQL ODBC potrebbe essere modificato o non disponibile in futuro.

Le applicazioni possono usare le API PDH per leggere e scrivere i dati dei contatori delle prestazioni in database SQL ODBC compatibili e quindi eseguire ulteriori elaborazioni tramite SQL query. In questa sezione viene descritto SQL schema utilizzato per archiviare i contatori delle prestazioni. È possibile usare queste informazioni per creare visualizzazioni e report personalizzati. Lo schema è costituito dalle tre tabelle seguenti:

- [**Counterdata**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> Il supporto PDH per i SQL ODBC funziona solo con i driver odbc SQL che supportano le estensioni [bcp (Bulk Copy).](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)
