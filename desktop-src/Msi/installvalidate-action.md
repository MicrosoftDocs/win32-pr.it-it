---
description: L'azione InstallValidate verifica che tutti i volumi a cui è stato attribuito il costo dispongano di spazio sufficiente per l'installazione. L'azione InstallValidate termina l'installazione con un errore irreversibile se lo spazio su disco è insufficiente in un volume.
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: Azione InstallValidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650ce136ac3b1b62e41ce34f79f5d28540d1292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233306"
---
# <a name="installvalidate-action"></a>Azione InstallValidate

L'azione InstallValidate verifica che tutti i [*volumi*](v-gly.md) a cui è stato attribuito il [*costo*](c-gly.md) dispongano di spazio sufficiente per l'installazione. L'azione InstallValidate termina l'installazione con un errore irreversibile se lo spazio su disco è insufficiente in un volume.

L'azione InstallValidate notifica inoltre all'utente se uno o più file da sovrascrivere o rimuovere sono attualmente utilizzati da un processo attivo. Per ulteriori informazioni, vedere [riavvii del sistema](system-reboots.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione [CostFinalize secondo](costfinalize-action.md) e le sequenze della finestra di dialogo dell'interfaccia utente che consentono all'utente di modificare gli Stati di selezione e/o le directory devono essere sequenziate prima dell'azione InstallValidate.

Le [azioni personalizzate](custom-actions.md) che modificano lo stato di installazione delle funzionalità o dei componenti devono essere sequenziate prima dell'azione InstallValidate.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

In genere, una sequenza precedente della finestra di dialogo dell'interfaccia utente deve eseguire la stessa verifica dell'azione InstallValidate quando l'utente tenta di avviare la copia dei file. Questa sequenza della finestra di dialogo dell'interfaccia utente dovrebbe presentare una finestra **di dialogo di spazio su disco** insufficiente se i volumi selezionati non dispongono di spazio sufficiente per l'installazione. Le finestre di dialogo dell'interfaccia utente devono essere create in modo da impedire all'utente di procedere con l'installazione se lo spazio su disco è insufficiente. Nel caso di un'installazione non interattiva, non esiste alcuna interfaccia utente e l'azione InstallValidate termina l'installazione se lo spazio su disco è insufficiente. Se la registrazione è abilitata, la provocazione della terminazione prematura viene registrata nel file di log.

Una voce viene aggiunta a una tabella filesinus interna se un file viene sovrascritto o rimosso mentre è aperto per l'esecuzione o la modifica da qualsiasi processo durante il [*costo*](c-gly.md)del file. La tabella filesinus contiene le colonne per il nome e il percorso completo del file. Quando viene eseguita l'azione InstallValidate, il programma di installazione esegue una query sulla tabella filesinus per le voci e determina il nome del processo usando il file. L'azione InstallValidate aggiunge un record alla tabella dell'interfaccia utente [ListBox](listbox-table.md) per ogni processo univoco identificato da questa query. Il record contiene i valori seguenti in ogni colonna:

**Proprietà**: FileInUseProcess

 

**Valore**: *nome del processo*

 

**Text**: *testo contenuto nella didascalia della finestra principale del processo*

L'azione InstallValidate Visualizza quindi la finestra **di dialogo file in uso** . In questa finestra di dialogo vengono visualizzati i processi che devono essere arrestati per evitare la necessità di riavviare il sistema per sostituire i file in uso.

L'azione InstallValidate esegue una query nella tabella della [finestra](dialog-table.md) di dialogo per una finestra di dialogo creata con la finestra di dialogo nome riservato [filesinus](filesinuse-dialog.md) e la Visualizza. Questa finestra di dialogo deve contenere un controllo [ListBox](listbox-control.md) associato a una proprietà denominata FileInUseProcess. Per convenzione, questa finestra di dialogo contiene un pulsante **Esci**, **Riprova** o **Ignora** , ma questo è l'autore dell'interfaccia utente. Ogni pulsante deve essere associato a un ControlEvent [EndDialog](enddialog-controlevent.md) nella tabella [ControlEvent](controlevent-table.md) . L'azione InstallValidate risponde nel modo seguente al valore restituito da [DoAction](doaction-controlevent.md) ControlEvent, come stabilito da uno di questi argomenti [EndDialog](enddialog-controlevent.md) associati al pulsante spinto dall'utente:

**Nuovo tentativo**: tutti i valori aggiunti alla tabella [ListBox](listbox-table.md) vengono cancellati e viene ripetuta l'intera procedura di [*determinazione dei costi*](c-gly.md) del file, ricontrollando i file ancora in uso. Se uno o più processi sono ancora identificati come utilizzando i file da sovrascrivere o eliminare, il processo viene ripetuto; in caso contrario, InstallValidate restituisce il controllo al programma di installazione con lo stato msiDoActionStatusSuccess.

**Exit**: l'azione InstallValidate restituisce immediatamente il controllo al programma di installazione con lo stato msiDoActionStatusUserExit. L'installazione verrà terminata.

**Qualsiasi altro valore restituito**: l'azione InstallValidate restituisce immediatamente il controllo al programma di installazione con lo stato msiDoActionStatusSuccess. In questo caso, dal momento che uno o più file sono ancora in uso, le azioni successive [InstallFiles](installfiles-action.md) e/o [InstallAdminPackage](installadminpackage-action.md) devono pianificare i file in uso da sostituire o eliminare al riavvio del sistema.

Se nel database non è presente alcuna tabella [ListBox](listbox-table.md) , InstallValidate viene chiuso automaticamente senza errori.

Il punto e virgola è il delimitatore di elenco per le trasformazioni, le origini e le patch e non deve essere utilizzato in questi nomi file o percorsi.

I file contrassegnati come di sola lettura in un percorso di sola lettura non vengono mai considerati usati dal programma di installazione.

Una finestra di dialogo di **spazio su disco** predefinita contenente i **pulsanti** **Interrompi** e ripetizioni viene visualizzata all'utente se il livello di interfaccia utente è di base.

 

 



