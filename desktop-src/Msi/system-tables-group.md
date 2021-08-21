---
description: Le tabelle del gruppo tabelle di sistema tiene traccia delle tabelle e delle colonne del database di installazione.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Gruppo tabelle di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c05bfd06bcff049d2aea847a2bb8d0c4c3fc3d1443a615f75912ac7d4f86d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623920"
---
# <a name="system-tables-group"></a>Gruppo tabelle di sistema

Le tabelle del gruppo tabelle di sistema tiene traccia delle tabelle e delle colonne del database di installazione.

-   La [ \_ tabella Tabelle](-tables-table.md) tiene traccia di tutte le tabelle nel database. Sono incluse le tabelle che potrebbero essere state create per le proprie azioni personalizzate. Eseguire una query su questa tabella per determinare se esiste una tabella.
-   La [ \_ tabella Colonne tiene](-columns-table.md) traccia delle colonne nel database di installazione. Le colonne temporanee non vengono attualmente rilevate da questa tabella. Eseguire una query su questa tabella per determinare se esiste una determinata colonna.
-   La [ \_ Flussi tabella elenca](-streams-table.md) i flussi di dati OLE incorporati.
-   La [ \_ tabella Storages elenca](-storages-table.md) le risorse di archiviazione dei dati OLE incorporate.
-   Tabella [ \_ di convalida](-validation-table.md). La \_ tabella Validation tiene traccia dei tipi e degli intervalli consentiti di ogni colonna nel database. La tabella Validation viene usata durante il processo di convalida del database per assicurarsi che tutte le colonne \_ siano rappresentate e che i valori siano corretti. Questa tabella non viene fornita con il database del programma di installazione.

 

 



