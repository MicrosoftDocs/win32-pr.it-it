---
description: Le applicazioni possono utilizzare PDH per estrarre i contatori delle prestazioni dai log SQL oppure possono estrarre i contatori formattati o non elaborati direttamente dal database tramite query SQL.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: Schema del file di log SQL
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312079"
---
# <a name="sql-log-file-schema"></a>Schema del file di log SQL

> [!IMPORTANT]
> Il supporto di PDH per i database SQL ODBC può essere modificato o non disponibile in futuro.

Le applicazioni possono utilizzare le API PDH per leggere e scrivere i dati dei contatori delle prestazioni in database SQL ODBC compatibili, quindi eseguire ulteriori elaborazioni tramite query SQL. In questa sezione viene descritto lo schema SQL utilizzato per archiviare i contatori delle prestazioni. È possibile utilizzare queste informazioni per creare visualizzazioni e report personalizzati. Lo schema è costituito dalle tre tabelle seguenti:

- [**CounterData**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> Il supporto di PDH per i database SQL ODBC funziona solo con i driver SQL ODBC che supportano le estensioni per la [copia bulk (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).
