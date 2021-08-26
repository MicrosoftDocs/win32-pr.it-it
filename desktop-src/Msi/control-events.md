---
description: Un ControlEvent specifica un'azione che deve essere eseguita dal programma di installazione o una modifica negli attributi di uno o più controlli in una finestra di dialogo. Per altre informazioni su ControlEvents, vedere Cenni preliminari su ControlEvent.
ms.assetid: 8768acaa-884b-428f-a14e-3f39f8ea4ad5
title: Eventi di controllo (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd72e93da7ed84c845b5993b2a021119c861b682ab5eb4645c69c723b17a404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075091"
---
# <a name="control-events-windows-installer"></a>Eventi di controllo (Windows Installer)

Un ControlEvent specifica un'azione che deve essere eseguita dal programma di installazione o una modifica negli attributi di uno o più controlli in una finestra di dialogo. Per altre informazioni su ControlEvents, vedere [Cenni preliminari su ControlEvent.](controlevent-overview.md)

Nella tabella seguente vengono forniti collegamenti ad altre informazioni su controlEvents specifici.



| Evento di controllo                                                       | Breve descrizione di ControlEvent                                                                                                                                                                             |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ActionData](actiondata-controlevent.md)                           | Pubblica i dati sull'azione più recente.                                                                                                                                                                          |
| [ActionText](actiontext-controlevent.md)                           | Pubblica il nome dell'azione presente.                                                                                                                                                                     |
| [Addlocal](addlocal-controlevent.md)                               | Notifica al programma di installazione di eseguire le funzionalità in locale.                                                                                                                                                               |
| [AddSource](addsource-controlevent.md)                             | Notifica al programma di installazione di eseguire le funzionalità dalla relativa origine.                                                                                                                                                     |
| [CheckExistingTargetPath](checkexistingtargetpath-controlevent.md) | Notifica al programma di installazione di verificare che il percorso possa essere scritto.                                                                                                                                                |
| [CheckTargetPath](checktargetpath-controlevent.md)                 | Notifica al programma di installazione di verificare che il percorso sia valido.                                                                                                                                                      |
| [DirectoryListNew](directorylistnew-controlevent.md)               | Notifica al controllo DirectoryList di creare una nuova cartella.                                                                                                                                                    |
| [DirectoryListOpen](directorylistopen-controlevent.md)             | Seleziona la directory nel controllo DirectoryList.                                                                                                                                                           |
| [DirectoryListUp](directorylistup-controlevent.md)                 | Notifica al controllo DirectoryList di selezionare l'elemento padre della directory corrente.                                                                                                                             |
| [DoAction](doaction-controlevent.md)                               | La finestra di dialogo notifica al programma di installazione di eseguire un'azione personalizzata.                                                                                                                                                 |
| [EnableRollback](enablerollback-controlevent.md)                   | Consente di attivare e disattivare le funzionalità di rollback.                                                                                                                                                                |
| [EndDialog](enddialog-controlevent.md)                             | Notifica al programma di installazione di rimuovere una finestra di dialogo modale.                                                                                                                                                          |
| [IgnoreChange](ignorechange-controlevent.md)                       | Pubblicato dal controllo DirectoryList quando una cartella è evidenziata ma non aperta.                                                                                                                           |
| [MsiLaunchApp](msilaunchapp-controlevent.md)                       | Questo evento di controllo esegue un file specificato. **[Windows Installer 4.5 e versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato.<br/>                                                       |
| [MsiPrint](msiprint-controlevent.md)                               | Consente all'utente di stampare il contenuto del [controllo ScrollableText.](scrollabletext-control.md) **[Windows Installer 4.5 e versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato.<br/> |
| [NewDialog](newdialog-controlevent.md)                             | Notifica al programma di installazione di modificare una finestra di dialogo modale in un'altra finestra di dialogo.                                                                                                                                  |
| [Reinstallare](reinstall-controlevent.md)                             | Avvia una reinstallazione delle funzionalità.                                                                                                                                                                       |
| [ReinstallMode](reinstallmode-controlevent.md)                     | Specifica la modalità di convalida durante una reinstallazione.                                                                                                                                                        |
| [Rimuovi](remove-controlevent.md)                                   | Notifica al programma di installazione quando vengono selezionate funzionalità per la rimozione.                                                                                                                                                |
| [Reimpostazione](reset-controlevent.md)                                     | Reimposta tutti i valori delle proprietà ai valori predefiniti utilizzati durante la creazione della finestra di dialogo.                                                                                                                    |
| [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)       | Usare [Gestione riavvio per](/windows/desktop/RstMgr/restart-manager-portal) arrestare tutte le applicazioni che dispongono di file in uso e riavviarle al termine dell'installazione.                                                              |
| [ScriptInProgress](scriptinprogress-controlevent.md)               | Visualizza una stringa durante la compilazione dello script di esecuzione.                                                                                                                                                     |
| [SelectionAction](selectionaction-controlevent.md)                 | Pubblicato da SelectionTree per descrivere un elemento.                                                                                                                                                               |
| [SelectionBrowse](selectionbrowse-controlevent.md)                 | Pubblicato da SelectionTree per generare una finestra di dialogo.                                                                                                                                                             |
| [SelectionDescription](selectiondescription-controlevent.md)       | Pubblicato da SelectionTree per fornire una stringa nel campo Descrizione della tabella delle funzionalità.                                                                                                                 |
| [SelectionNoItems](selectionnoitems-controlevent.md)               | Usato da SelectionTree per eliminare il testo o disabilitare i pulsanti.                                                                                                                                                      |
| [SelectionPath](selectionpath-controlevent.md)                     | Pubblicato da SelectionTree per fornire il percorso di un elemento.                                                                                                                                                    |
| [SelectionPathOn](selectionpathon-controlevent.md)                 | Pubblicato da SelectionTree per indicare se è presente un percorso associato a una funzionalità.                                                                                                                     |
| [SelectionSize](selectionsize-controlevent.md)                     | Pubblicato dal controllo SelectionTree per fornire le dimensioni di un elemento.                                                                                                                                            |
| [SetInstallLevel](setinstalllevel-controlevent.md)                 | Il programma di installazione modifica il livello di installazione a un valore specificato.                                                                                                                                                |
| [SetProgress](setprogress-controlevent.md)                         | Pubblicato dal programma di installazione per fornire lo stato di avanzamento dell'installazione.                                                                                                                                                  |
| [SetProperty](setproperty-controlevent.md)                         | Imposta una proprietà specificata.                                                                                                                                                                                    |
| [SetTargetPath](settargetpath-controlevent.md)                     | Notifica al programma di installazione di controllare e impostare un percorso.                                                                                                                                                               |
| [Finestra di dialogo SpawnDialog](spawndialog-controlevent.md)                         | Notifica al programma di installazione di creare un elemento figlio di una casella modale.                                                                                                                                                      |
| [Finestra di dialogo SpawnWaitDialog](spawnwaitdialog-controlevent.md)                 | Attiva una finestra di dialogo specificata.                                                                                                                                                                              |
| [TimeRemaining](timeremaining-controlevent.md)                     | Pubblicato dal programma di installazione per fornire il tempo rimanente nella sequenza di stato.                                                                                                                            |
| [ValidateProductID](validateproductid-controlevent.md)             | Imposta ProductID sull'ID prodotto completo.                                                                                                                                                                        |



 

 

