---
description: Il database del programma di installazione consente allo sviluppatore di un pacchetto di installazione di controllare il trasferimento di un'applicazione da un'origine a un'immagine di destinazione.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Utilizzo del database del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312312"
---
# <a name="using-the-installer-database"></a>Utilizzo del database del programma di installazione

Il [database del programma](installer-database.md) di installazione consente allo sviluppatore di un pacchetto di installazione di controllare il trasferimento di un'applicazione da un'origine a un'immagine di destinazione. Il layout delle immagini di origine e di destinazione dell'applicazione viene specificato nella tabella di [directory](directory-table.md) e le azioni che installano l'applicazione vengono specificate in sei tabelle di sequenza:

-   Tabella [InstallUISequence](installuisequence-table.md)
-   Tabella [InstallExecuteSequence](installexecutesequence-table.md)
-   Tabella [AdminUISequence](adminuisequence-table.md)
-   Tabella [AdminExecuteSequence](adminexecutesequence-table.md)
-   Tabella [AdvtUISequence](advtuisequence-table.md)
-   Tabella [AdvtExecuteSequence](advtexecutesequence-table.md)

Le sezioni seguenti descrivono come usare il [database del programma di installazione](installer-database.md):

-   [Uso della tabella di directory](using-the-directory-table.md)
-   [Utilizzo di una tabella di sequenza](using-a-sequence-table.md)
-   [Acquisizione di un handle di database](obtaining-a-database-handle.md)
-   [Commit dei database](committing-databases.md)
-   [Importazione ed esportazione](importing-and-exporting.md)
-   [Unione di database](merging-databases.md)
-   [Denominazione di tabelle, proprietà e azioni personalizzate](naming-custom-tables-properties-and-actions.md)
-   [Limitazioni OLE sui flussi](ole-limitations-on-streams.md)
-   [Utilizzo delle query](working-with-queries.md)
-   [Aggiunta di dati binari a una tabella tramite SQL](adding-binary-data-to-a-table-using-sql.md)
-   [Utilizzo dei record](working-with-records.md)
-   [Uso dei percorsi delle cartelle](working-with-folder-locations.md)
-   [Specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md)
-   [Esecuzione delle azioni di condizionamento durante la rimozione](conditioning-actions-to-run-during-removal.md)
-   [Chiamata di funzioni di database da programmi](calling-database-functions-from-programs.md)
-   [Sintassi dell'istruzione condizionale](conditional-statement-syntax.md)
-   [Formato della definizione di colonna](column-definition-format.md)
-   [Determinare se una colonna è una chiave primaria o esterna](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



