---
description: Le tabelle del gruppo tabelle di sistema tengono traccia delle tabelle e delle colonne del database di installazione.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Gruppo tabelle di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130270"
---
# <a name="system-tables-group"></a>Gruppo tabelle di sistema

Le tabelle del gruppo tabelle di sistema tengono traccia delle tabelle e delle colonne del database di installazione.

-   La [ \_ tabella](-tables-table.md) Tables tiene traccia di tutte le tabelle del database. Sono incluse le tabelle che è possibile creare per le azioni personalizzate. Eseguire una query su questa tabella per verificare se esiste una tabella.
-   La [ \_ tabella Columns](-columns-table.md) tiene traccia delle colonne del database di installazione. Attualmente le colonne temporanee non vengono rilevate da questa tabella. Eseguire una query su questa tabella per determinare se esiste una determinata colonna.
-   La [ \_ tabella Streams](-streams-table.md) elenca i flussi di dati OLE incorporati.
-   La [ \_ tabella Storages](-storages-table.md) elenca le archiviazioni di dati OLE embedded.
-   [ \_ Tabella di convalida](-validation-table.md). La \_ tabella di convalida tiene traccia dei tipi e degli intervalli consentiti di ogni colonna nel database. La \_ tabella di convalida viene utilizzata durante il processo di convalida del database per garantire che tutte le colonne siano contabilizzate e dispongano dei valori corretti. Questa tabella non è inclusa nel database del programma di installazione.

 

 



