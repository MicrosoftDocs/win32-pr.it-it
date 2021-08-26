---
description: Le azioni personalizzate vengono pianificate nelle tabelle di sequenza nello stesso modo delle azioni standard.
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: Sequenziazione di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d86449b67809f782560e35d32b1b1e42434153ced776a27fd479a7b80a25a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039971"
---
# <a name="sequencing-custom-actions"></a>Sequenziazione di azioni personalizzate

Le azioni personalizzate vengono pianificate nelle tabelle di sequenza nello stesso modo delle azioni standard.

**Per pianificare un'azione personalizzata in una tabella di sequenza**

1.  Immettere il nome dell'azione personalizzata ,ovvero la chiave primaria della tabella [CustomAction,](customaction-table.md)nella colonna Azione della [tabella Sequence.](sequence-table-detailed-example.md)
2.  Immettere la sequenza dell'azione personalizzata relativa alle altre azioni nella tabella nella colonna Sequenza della [tabella Sequenza.](sequence-table-detailed-example.md) Per altre informazioni sulle tabelle di sequenza, vedere [Uso di una tabella di sequenza](using-a-sequence-table.md).
3.  Per ignorare l'azione in modo condizionale, immettere un'espressione condizionale nella colonna Condizione della [tabella Sequenza.](sequence-table-detailed-example.md) Il programma di installazione ignora questa azione se l'espressione restituisce FALSE.

Come nel caso di azioni standard, le azioni personalizzate pianificate in [InstallUISequence](installuisequence-table.md) o [AdminUISequence](adminuisequence-table.md) vengono eseguite solo se l'interfaccia utente interna è impostata sul livello completo. Il livello dell'interfaccia utente viene impostato usando la [**funzione MsiSetInternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

Le azioni standard e personalizzate pianificate nelle tabelle [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) non apportano modifiche di sistema. Il programma di installazione accoda invece i record di esecuzione in uno script per l'esecuzione successiva durante il servizio di installazione. Se non è presente alcun servizio di installazione, le azioni pianificate in queste tabelle vengono eseguite nello stesso contesto della sequenza dell'interfaccia utente.

Se il server di installazione non è registrato, le azioni personalizzate vengono eseguite sul lato client. Se il server è registrato e usa la modalità interfaccia utente completa, le azioni personalizzate vengono eseguite sul lato server.

Se si usa l'interfaccia utente completa con il server, le azioni iniziali precedenti all'azione [InstallValidate](installvalidate-action.md) vengono eseguite nel client per consentire l'interazione completa. L'esecuzione viene quindi passata al server che ripete tali azioni ed esegue le azioni di esecuzione dello script. Questa operazione è seguita da un ritorno al client per le azioni finali.

Si noti che se un prodotto viene rimosso impostando la funzionalità principale su absent, la [**proprietà REMOVE**](remove.md) potrebbe non essere uguale a ALL fino a dopo l'azione [InstallValidate.](installvalidate-action.md) Ciò significa che qualsiasi azione personalizzata che dipende da REMOVE=ALL deve essere sequenziata dopo l'azione InstallValidate. Un'azione personalizzata può controllare REMOVE per determinare se un prodotto è stato impostato per la disinstallazione completa.

Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio Custom Action Type 17 (DLL), Custom Action Type 18 (EXE), Custom Action Type 21 (JScript) e Custom Action Type 22 (VBScript), devono rispettare le restrizioni di sequenziazione seguenti.

-   L'azione personalizzata deve essere sequenziata dopo [l'azione CostFinalize](costfinalize-action.md) in modo che sia possibile risolvere il percorso del file a cui si fa riferimento.
-   Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (nello script) devono essere sequenziate dopo [InstallFiles](installfiles-action.md).
-   Se il file di origine non è già installato nel computer, le azioni personalizzate nondeferre devono essere sequenziate dopo [l'azione InstallInitialize.](installinitialize-action.md)

Le restrizioni di sequenziazione seguenti si applicano alle azioni personalizzate che modificano o aggiornano un pacchetto Windows installer.

-   Se l'azione personalizzata modifica il pacchetto, ad esempio aggiungendo righe a una tabella, l'azione deve essere sequenziata prima [dell'azione InstallInitialize.](installinitialize-action.md)
-   Se l'azione personalizzata apporta modifiche che influiscono sulla determinazione dei costi, deve essere sequenziata prima [dell'azione CostInitialize.](costfinalize-action.md)
-   Se l'azione personalizzata modifica lo stato di installazione delle funzionalità o dei componenti, deve essere sequenziata prima [dell'azione InstallValidate.](installvalidate-action.md)

 

 



