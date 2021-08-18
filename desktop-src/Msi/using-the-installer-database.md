---
description: Il database del programma di installazione consente allo sviluppatore di un pacchetto di installazione di controllare il trasferimento di un'applicazione da un'immagine di origine a un'immagine di destinazione.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Uso del database del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec91d8982a8ddac47c96303f03a33e4c85cafa70c3ef480c660df42e72f8a84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996061"
---
# <a name="using-the-installer-database"></a>Uso del database del programma di installazione

Il [database del programma di](installer-database.md) installazione consente allo sviluppatore di un pacchetto di installazione di controllare il trasferimento di un'applicazione da un'immagine di origine a un'immagine di destinazione. Il layout delle immagini di origine e di destinazione dell'applicazione è specificato nella tabella [Directory](directory-table.md) e le azioni che installano l'applicazione sono specificate in sei tabelle di sequenza:

-   [Tabella InstallUISequence](installuisequence-table.md)
-   [Tabella InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabella AdminUISequence](adminuisequence-table.md)
-   [Tabella AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabella AdvtUISequence](advtuisequence-table.md)
-   [Tabella AdvtExecuteSequence](advtexecutesequence-table.md)

Le sezioni seguenti descrivono come usare il database [del programma di installazione](installer-database.md):

-   [Uso della tabella directory](using-the-directory-table.md)
-   [Uso di una tabella di sequenze](using-a-sequence-table.md)
-   [Recupero di un handle di database](obtaining-a-database-handle.md)
-   [Commit di database](committing-databases.md)
-   [Importazione ed esportazione](importing-and-exporting.md)
-   [Unione di database](merging-databases.md)
-   [Denominazione di tabelle, proprietà e azioni personalizzate](naming-custom-tables-properties-and-actions.md)
-   [Limitazioni OLE in Flussi](ole-limitations-on-streams.md)
-   [Utilizzo delle query](working-with-queries.md)
-   [Aggiunta di dati binari a una tabella tramite SQL](adding-binary-data-to-a-table-using-sql.md)
-   [Uso dei record](working-with-records.md)
-   [Uso dei percorsi delle cartelle](working-with-folder-locations.md)
-   [Specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md)
-   [Azioni di condizionamento da eseguire durante la rimozione](conditioning-actions-to-run-during-removal.md)
-   [Chiamata di funzioni di database da programmi](calling-database-functions-from-programs.md)
-   [Sintassi delle istruzioni condizionali](conditional-statement-syntax.md)
-   [Formato definizione colonna](column-definition-format.md)
-   [Determinare se una colonna è una chiave primaria o esterna](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



