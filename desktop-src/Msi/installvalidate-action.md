---
description: L'azione InstallValidate verifica che tutti i volumi a cui è stato attribuito il costo dispongano di spazio sufficiente per l'installazione. L'azione InstallValidate termina l'installazione con un errore irreversibile se uno spazio su disco è insufficiente.
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: Azione InstallValidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8a5e2f69df5e588c2366f7cf9fff0fb3621889e9b725605a38acc14f39457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805639"
---
# <a name="installvalidate-action"></a>Azione InstallValidate

L'azione InstallValidate verifica che [](c-gly.md) tutti i [*volumi*](v-gly.md) a cui è stato attribuito il costo dispongano di spazio sufficiente per l'installazione. L'azione InstallValidate termina l'installazione con un errore irreversibile se uno spazio su disco è insufficiente.

L'azione InstallValidate notifica inoltre all'utente se uno o più file da sovrascritti o rimuovere sono attualmente in uso da un processo attivo. Per altre informazioni, vedere [Riavvii del sistema](system-reboots.md).

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

[L'azione CostFinalize](costfinalize-action.md) e le sequenze di finestre di dialogo dell'interfaccia utente che consentono all'utente di modificare gli stati di selezione e/o le directory devono essere sequenziate prima dell'azione InstallValidate.

[Le azioni personalizzate](custom-actions.md) che modificano lo stato di installazione di funzionalità o componenti devono essere sequenziate prima dell'azione InstallValidate.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

In genere, una precedente sequenza di finestre di dialogo dell'interfaccia utente deve eseguire la stessa verifica dell'azione InstallValidate quando l'utente tenta di avviare la copia dei file. Questa sequenza di finestre  di dialogo dell'interfaccia utente dovrebbe presentare una finestra di dialogo Spazio su disco insufficiente se i volumi selezionati non hanno spazio sufficiente per l'installazione. Le finestre di dialogo dell'interfaccia utente devono essere scritte in modo da impedire all'utente di procedere con l'installazione se lo spazio su disco è insufficiente. Nel caso di un'installazione non interattiva, non è disponibile alcuna interfaccia utente e l'azione InstallValidate termina l'installazione se lo spazio su disco è insufficiente. La causa della terminazione prematura viene registrata nel file di log se la registrazione è abilitata.

Una voce viene aggiunta a una tabella FilesInUse interna se un file viene sovrascritto o rimosso mentre è aperto per l'esecuzione o la modifica da parte di qualsiasi processo durante il costo [*del*](c-gly.md)file . La tabella FilesInUse contiene colonne per il nome e il percorso completo del file. Quando viene eseguita l'azione InstallValidate, il programma di installazione esegue una query sulla tabella FilesInUse per le voci e determina il nome del processo usando il file. L'azione InstallValidate aggiunge un record alla tabella dell'interfaccia utente [di ListBox](listbox-table.md) per ogni processo univoco identificato da questa query. Il record contiene i valori seguenti in ogni colonna:

**Proprietà**: FileInUseProcess

 

**Valore:** *nome del processo*

 

**Text**: *testo contenuto nella didascalia della finestra principale del processo*

L'azione InstallValidate visualizza quindi la **finestra di dialogo** File in uso. In questa finestra di dialogo vengono visualizzati i processi che devono essere arrestati per evitare la necessità di riavviare il sistema per sostituire i file in uso.

L'azione InstallValidate esegue una query nella tabella [Dialog](dialog-table.md) per una finestra di dialogo con il nome riservato [FilesInUse](filesinuse-dialog.md) e la visualizza. Questa finestra di dialogo deve contenere un [controllo ListBox](listbox-control.md) associato a una proprietà denominata FileInUseProcess. Per convenzione, questa finestra di dialogo ha un pulsante **Esci,** **Riprova** **o** Ignora, ma questo è l'autore dell'interfaccia utente. Ogni pulsante deve essere associato a [un evento ControlEvent EndDialog](enddialog-controlevent.md) nella [tabella ControlEvent.](controlevent-table.md) L'azione InstallValidate risponde come segue al valore restituito da [DoAction](doaction-controlevent.md) ControlEvent, come indicato da uno di questi [argomenti EndDialog](enddialog-controlevent.md) associati al pulsante premuto dall'utente:

**Riprova:** tutti i valori aggiunti alla tabella [ListBox](listbox-table.md) vengono cancellati e l'intera procedura di determinazione dei costi dei [*file*](c-gly.md) viene ripetuta, verificando nuovamente i file ancora in uso. Se uno o più processi vengono ancora identificati come che usano file da sovrascritti o eliminare, il processo viene ripetuto. In caso contrario, InstallValidate restituisce il controllo al programma di installazione con stato msiDoActionStatusSuccess.

**Exit:** l'azione InstallValidate restituisce immediatamente il controllo al programma di installazione con stato msiDoActionStatusUserExit. Questa operazione termina l'installazione.

**Qualsiasi altro valore restituito:** l'azione InstallValidate restituisce immediatamente il controllo al programma di installazione con stato msiDoActionStatusSuccess. In questo caso, poiché uno o più file sono ancora in uso, le azioni [InstallFiles](installfiles-action.md) e/o [InstallAdminPackage](installadminpackage-action.md) successive devono pianificare la sostituzione o l'eliminazione dei file in uso al riavvio del sistema.

Se nel database non è presente alcuna tabella [ListBox,](listbox-table.md) InstallValidate viene chiuso automaticamente senza errori.

Il punto e virgola è il delimitatore di elenco per trasformazioni, origini e patch e non deve essere usato in questi nomi di file o percorsi.

I file contrassegnati come di sola lettura in un percorso di sola lettura non vengono mai considerati in uso dal programma di installazione.

Se il **livello dell'interfaccia** utente  è di base, viene visualizzata all'utente una finestra di dialogo Predefinita spazio su disco contenente i pulsanti Interrompi e Riprova. 

 

 



