---
description: Modificare le altre colonne localizzabili nel database MNPFren.msi usando un editor di tabelle, ad esempio Orca o query SQL.
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: Localizzazione di colonne di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed36b1adb2c496c9019b482c929e449187b1e0bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057805"
---
# <a name="localizing-database-columns"></a>Localizzazione di colonne di database

Modificare le altre colonne localizzabili nel database MNPFren.msi usando un editor di tabelle, ad esempio Orca o query SQL. Per determinare quali colonne di una determinata tabella possono essere localizzate in un'altra lingua, vedere l'argomento di riferimento relativo a tale tabella di database. Per un elenco di tutte le tabelle di database, vedere [tabelle di database](database-tables.md) .

Ad esempio, potrebbe essere necessario localizzare in francese il campo di testo di alcuni record della [tabella dei controlli](control-table.md) . La stringa "annullare l' \[ installazione di ProductName \] ?" nella [finestra di dialogo Annulla](cancel-dialog.md) può essere modificato in questa tabella per essere visualizzato in francese. Il record originale nel file con estensione msi viene visualizzato come segue.

[Tabella di controllo](control-table.md) (parziale) del file con estensione msi originale



| Finestra di dialogo\_  | Control | Tipo | X   | S   | Larghezza | Altezza | Attributi | Proprietà | Testo                                                          | Controllo \_ successivo | Help |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| CancelDlg | Testo    | Testo | 48  | 15  | 194   | 30     | 3          |          | Annullare l' \[ installazione di ProductName \] ? |               |      |



 

È possibile usare un editor tabelle per modificare il campo di testo, ad esempio l'editor di tabelle Orca fornito con SDK o un altro editor di tabelle, oppure usare una query SQL per modificare il campo di testo del record della tabella di controllo. In Windows Installer SDK viene fornito un esempio che illustra le query di database basate su script come WiRunSQL.vbs di utilità. Utilizzare la riga di comando seguente per modificare il campo con WiRunSQL.vbs e Windows script host. Vedere anche [esempi di query di database con SQL e script](examples-of-database-queries-using-sql-and-script.md).

**Cscript WiRunSQL.vbs MNPFren.msi "UPDATE Control SET Control. Text =' etes-vous sur de vouloir l'installation de \[ ProductName \] ?' DOVE Control. Dialog \_ =' CancelDlg ' e Control. Control =' text ' "**

[Tabella di controllo](control-table.md) (parziale) in MNPFren.msi



| Finestra di dialogo\_  | Control | Tipo | X   | S   | Larghezza | Altezza | Attributi | Proprietà | Testo                                                                | Controllo \_ successivo | Help |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| CancelDlg | Testo    | Testo | 48  | 15  | 194   | 30     | 3          |          | Êtes-vous sûr de vouloir l'installation de \[ ProductName \] ? |               |      |



 

Se l'installazione di MNPFren.msi viene annullata dall'utente, viene visualizzata la **finestra di dialogo Annulla** che Visualizza il testo: "êtes-vous sûr de vouloir anulare L'INSTALLATION de MNP2000?"

Quando si usa questo metodo per localizzare il testo dell'interfaccia utente in una lingua diversa, l'interfaccia utente localizzata deve essere testata per assicurarsi che le dimensioni dei controlli siano sufficientemente grandi da visualizzare l'intero testo localizzato. Questa operazione deve essere testata usando tutte le impostazioni relative alle dimensioni del carattere disponibili per la visualizzazione. Il testo localizzato può richiedere più spazio del testo originale e può essere troncato se visualizzato in un controllo troppo piccolo.

[Continua](updating-productlanguage-and-productcode-properties.md)

 

 



