---
description: Modificare una qualsiasi delle altre colonne localizzabili nel database MNPFren.msi usando un editor di tabelle come Orca o SQL query.
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: Localizzazione delle colonne del database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72d4d4d82f45be66f41710dea7294a63051d69750ade49ae3b66761964b579f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629456"
---
# <a name="localizing-database-columns"></a>Localizzazione delle colonne del database

Modificare una qualsiasi delle altre colonne localizzabili nel database MNPFren.msi usando un editor di tabelle come Orca o SQL query. Per determinare quali colonne di una determinata tabella possono essere localizzate in un'altra lingua, vedere l'argomento di riferimento per tale tabella di database. Per [un elenco di tutte](database-tables.md) le tabelle di database, vedere Tabelle di database.

Ad esempio, il campo Text di alcuni record nella [tabella Control potrebbe](control-table.md) dover essere localizzato in francese. La stringa "Si è certi di voler annullare \[ l'installazione di \] ProductName?" nella finestra [di dialogo Annulla](cancel-dialog.md) può essere modificata in questa tabella per essere visualizzata in francese. Il record originale nel .msi file viene visualizzato come segue.

[Tabella di](control-table.md) controllo (parziale) del file .msi originale



| Finestra di dialogo\_  | Control | Tipo | X   | S   | Larghezza | Altezza | Attributi | Proprietà | Testo                                                          | Controllo \_ successivo | Help |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| CancelDlg | Testo    | Testo | 48  | 15  | 194   | 30     | 3          |          | Si è certi di voler annullare \[ l'installazione di \] ProductName? |               |      |



 

È possibile usare un editor di tabelle per modificare il campo Text, ad esempio l'editor di tabelle Orca fornito con l'SDK o un altro editor di tabelle, oppure usare una query SQL per modificare il campo Text del record della tabella Control. Un esempio che illustra le query di database guidate da script viene fornito in Windows Installer SDK come utilità WiRunSQL.vbs. Usare la riga di comando seguente per modificare il campo con WiRunSQL.vbs e l'host Windows script. Vedere anche [Esempi di query di database con SQL e script](examples-of-database-queries-using-sql-and-script.md).

**Cscript WiRunSQL.vbs MNPFren.msi "UPDATE Control SET Control.Text='Etes-vous sur de vouloir annuler l'installation de \[ ProductName \] ?' WHERE Control.Dialog \_ ='CancelDlg' AND Control.Control='Text'"**

[Tabella di](control-table.md) controllo (parziale) in MNPFren.msi



| Finestra di dialogo\_  | Control | Tipo | X   | S   | Larghezza | Altezza | Attributi | Proprietà | Testo                                                                | Controllo \_ successivo | Help |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| CancelDlg | Testo    | Testo | 48  | 15  | 194   | 30     | 3          |          | Êtes-vous sèr de vouloir annuler l'installation de \[ ProductName \] ? |               |      |



 

Se l'installazione di MNPFren.msi viene annullata dall'utente, viene visualizzata la finestra di dialogo Annulla con il testo " Êtes-vous sèr de vouloir annuler l'installation de MNP2000?" 

Quando si usa questo metodo per localizzare il testo dell'interfaccia utente in una lingua diversa, è necessario testare l'interfaccia utente localizzata per assicurarsi che le dimensioni dei controlli siano sufficientemente grandi da visualizzare l'intero testo localizzato. Questa operazione deve essere testata usando tutte le impostazioni delle dimensioni del carattere disponibili per la visualizzazione. Il testo localizzato può richiedere più spazio del testo originale e può essere troncato se visualizzato in un controllo troppo piccolo.

[Continua](updating-productlanguage-and-productcode-properties.md)

 

 



