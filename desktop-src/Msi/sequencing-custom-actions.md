---
description: Le azioni personalizzate vengono pianificate in tabelle di sequenza in modo analogo alle azioni standard.
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: Sequenziazione di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7c24fb91247a36880cb808c9b8e10437312cf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234021"
---
# <a name="sequencing-custom-actions"></a>Sequenziazione di azioni personalizzate

Le azioni personalizzate vengono pianificate in tabelle di sequenza in modo analogo alle azioni standard.

**Per pianificare un'azione personalizzata in una tabella di sequenza**

1.  Immettere il nome dell'azione personalizzata, ovvero la chiave primaria della tabella [CustomAction](customaction-table.md), nella colonna azione della tabella di [sequenza](sequence-table-detailed-example.md) .
2.  Immettere la sequenza dell'azione personalizzata relativa alle altre azioni nella tabella nella colonna sequenza della tabella di [sequenza](sequence-table-detailed-example.md) . Per ulteriori informazioni sulle tabelle di sequenza, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).
3.  Per ignorare l'azione in modo condizionale, immettere un'espressione condizionale nella colonna condizione della tabella di [sequenza](sequence-table-detailed-example.md) . Il programma di installazione ignora questa azione se l'espressione restituisce FALSE.

Come nel caso di azioni standard, le azioni personalizzate pianificate in [InstallUISequence](installuisequence-table.md) o [AdminUISequence](adminuisequence-table.md) vengono eseguite solo se l'interfaccia utente interna è impostata sul livello completo. Il livello dell'interfaccia utente viene impostato tramite la funzione [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .

Le azioni standard e personalizzate pianificate nelle tabelle [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) non apportano modifiche al sistema. Al contrario, il programma di installazione accoda i record di esecuzione in uno script per l'esecuzione successiva durante il servizio di installazione. Se non è presente alcun servizio di installazione, le azioni pianificate in queste tabelle vengono eseguite nello stesso contesto della sequenza dell'interfaccia utente.

Se il server del programma di installazione non è registrato, le azioni personalizzate vengono eseguite sul lato client. Se il server è registrato e si utilizza la modalità di interfaccia utente completa, le azioni personalizzate vengono eseguite sul lato server.

Se si usa l'interfaccia utente completa con il server, le azioni iniziali prima dell'azione [InstallValidate](installvalidate-action.md) vengono eseguite sul client per consentire l'interazione completa. L'esecuzione viene quindi cambiata nel server che ripete tali azioni ed esegue le azioni di esecuzione dello script. Questa operazione è seguita da un ritorno al client per le azioni finali.

Si noti che se un prodotto viene rimosso impostando la funzionalità principale su assente, la proprietà [**Remove**](remove.md) potrebbe non essere uguale a All fino a dopo l'azione [InstallValidate](installvalidate-action.md) . Ciò significa che qualsiasi azione personalizzata che dipende da REMOVE = ALL deve essere sequenziata dopo l'azione InstallValidate. Un'azione personalizzata può selezionare Rimuovi per determinare se un prodotto è stato impostato per la disinstallazione completa.

Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio il tipo di azione personalizzata 17 (DLL), il tipo di azione personalizzata 18 (EXE), il tipo di azione personalizzata 21 (JScript) e il tipo di azione personalizzata 22 (VBScript), devono rispettare le restrizioni di sequenziazione seguenti.

-   L'azione personalizzata deve essere sequenziata dopo l'azione [CostFinalize secondo](costfinalize-action.md) in modo che sia possibile risolvere il percorso del file a cui si fa riferimento.
-   Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (in-script) devono essere sequenziate dopo [InstallFiles](installfiles-action.md).
-   Se il file di origine non è già installato nel computer, le azioni personalizzate nondeferred devono essere sequenziate dopo l'azione [InstallInitialize](installinitialize-action.md) .

Le restrizioni di sequenziazione seguenti si applicano alle azioni personalizzate che modificano o aggiornano un pacchetto di Windows Installer.

-   Se l'azione personalizzata modifica il pacchetto, ad esempio aggiungendo righe a una tabella, l'azione deve essere sequenziata prima dell'azione [InstallInitialize](installinitialize-action.md) .
-   Se l'azione personalizzata apporta modifiche che potrebbero influire sui costi, sarà necessario sequenziarla prima dell'azione [CostInitialize](costfinalize-action.md) .
-   Se l'azione personalizzata modifica lo stato di installazione delle funzionalità o dei componenti, deve essere sequenziata prima dell'azione [InstallValidate](installvalidate-action.md) .

 

 



