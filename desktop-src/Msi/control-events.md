---
description: Un ControlEvent specifica un'azione che deve essere eseguita dal programma di installazione o una modifica negli attributi di uno o più controlli in una finestra di dialogo. Per altre informazioni su ControlEvents, vedere Panoramica di ControlEvent.
ms.assetid: 8768acaa-884b-428f-a14e-3f39f8ea4ad5
title: Eventi di controllo (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221e8d9e6a8cea9a02b303040d06da346800912e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313818"
---
# <a name="control-events-windows-installer"></a>Eventi di controllo (Windows Installer)

Un ControlEvent specifica un'azione che deve essere eseguita dal programma di installazione o una modifica negli attributi di uno o più controlli in una finestra di dialogo. Per altre informazioni su ControlEvents, vedere [Panoramica di ControlEvent](controlevent-overview.md).

Nella tabella seguente vengono forniti i collegamenti ad altre informazioni su ControlEvents particolari.



| Evento di controllo                                                       | Breve descrizione di ControlEvent                                                                                                                                                                             |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ActionData](actiondata-controlevent.md)                           | Pubblica i dati nell'azione più recente.                                                                                                                                                                          |
| [ActionText](actiontext-controlevent.md)                           | Pubblica il nome dell'azione corrente.                                                                                                                                                                     |
| [AddLocal](addlocal-controlevent.md)                               | Notifica al programma di installazione di eseguire le funzionalità localmente.                                                                                                                                                               |
| [AddSource](addsource-controlevent.md)                             | Notifica al programma di installazione di eseguire le funzionalità dalla relativa origine.                                                                                                                                                     |
| [CheckExistingTargetPath](checkexistingtargetpath-controlevent.md) | Notifica al programma di installazione di verificare che sia possibile scrivere il percorso.                                                                                                                                                |
| [CheckTargetPath](checktargetpath-controlevent.md)                 | Notifica al programma di installazione di verificare che il percorso sia valido.                                                                                                                                                      |
| [DirectoryListNew](directorylistnew-controlevent.md)               | Notifica al controllo Directory di creare una nuova cartella.                                                                                                                                                    |
| [DirectoryListOpen](directorylistopen-controlevent.md)             | Consente di selezionare la directory nel controllo Directory.                                                                                                                                                           |
| [DirectoryListUp](directorylistup-controlevent.md)                 | Notifica al controllo Directory di selezionare l'elemento padre della directory corrente.                                                                                                                             |
| [DoAction](doaction-controlevent.md)                               | La finestra di dialogo notifica al programma di installazione di eseguire un'azione personalizzata.                                                                                                                                                 |
| [EnableRollback](enablerollback-controlevent.md)                   | Utilizzato per attivare e disattivare le funzionalità di rollback.                                                                                                                                                                |
| [EndDialog](enddialog-controlevent.md)                             | Notifica al programma di installazione di rimuovere una finestra di dialogo modale.                                                                                                                                                          |
| [IgnoreChange](ignorechange-controlevent.md)                       | Pubblicata dal controllo elenco di directory quando una cartella è evidenziata ma non aperta.                                                                                                                           |
| [MsiLaunchApp](msilaunchapp-controlevent.md)                       | Questo evento di controllo esegue un file specificato. **[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.<br/>                                                       |
| [MsiPrint](msiprint-controlevent.md)                               | Consente all'utente di stampare il contenuto del [controllo ScrollableText](scrollabletext-control.md). **[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.<br/> |
| [NewDialog](newdialog-controlevent.md)                             | Notifica al programma di installazione di modificare una finestra di dialogo modale in un'altra finestra di dialogo.                                                                                                                                  |
| [Reinstallare](reinstall-controlevent.md)                             | Avvia una reinstallazione delle funzionalità di.                                                                                                                                                                       |
| [ReinstallMode](reinstallmode-controlevent.md)                     | Specifica la modalità di convalida durante una reinstallazione.                                                                                                                                                        |
| [Rimuovi](remove-controlevent.md)                                   | Notifica al programma di installazione quando le funzionalità sono selezionate per la rimozione.                                                                                                                                                |
| [Reimpostazione](reset-controlevent.md)                                     | Reimposta tutti i valori di proprietà sui valori predefiniti utilizzati durante la creazione della finestra di dialogo.                                                                                                                    |
| [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)       | Usare [Gestione riavvio](/windows/desktop/RstMgr/restart-manager-portal) per arrestare tutte le applicazioni con file in uso e per riavviarle al termine dell'installazione.                                                              |
| [ScriptInProgress](scriptinprogress-controlevent.md)               | Visualizza una stringa durante la compilazione dello script di esecuzione.                                                                                                                                                     |
| [SelectionAction](selectionaction-controlevent.md)                 | Pubblicato da SelectionTree per descrivere un elemento.                                                                                                                                                               |
| [SelectionBrowse](selectionbrowse-controlevent.md)                 | Pubblicato da SelectionTree per generare una finestra di dialogo.                                                                                                                                                             |
| [SelectionDescription](selectiondescription-controlevent.md)       | Pubblicato da SelectionTree per fornire una stringa nel campo Description della tabella Feature.                                                                                                                 |
| [SelectionNoItems](selectionnoitems-controlevent.md)               | Usato da SelectionTree per eliminare il testo o disabilitare i pulsanti.                                                                                                                                                      |
| [SelectionPath](selectionpath-controlevent.md)                     | Pubblicato da SelectionTree per fornire il percorso di un elemento.                                                                                                                                                    |
| [SelectionPathOn](selectionpathon-controlevent.md)                 | Pubblicato da SelectionTree per indicare se è presente un percorso associato a una funzionalità.                                                                                                                     |
| [SelectionSize](selectionsize-controlevent.md)                     | Pubblicata dal controllo SelectionTree per fornire la dimensione di un elemento.                                                                                                                                            |
| [SetInstallLevel](setinstalllevel-controlevent.md)                 | Il programma di installazione modifica il livello di installazione in un valore specificato.                                                                                                                                                |
| [SetProgress](setprogress-controlevent.md)                         | Pubblicata dal programma di installazione per fornire lo stato di avanzamento dell'installazione.                                                                                                                                                  |
| [SetProperty](setproperty-controlevent.md)                         | Imposta una proprietà specificata.                                                                                                                                                                                    |
| [SetTargetPath](settargetpath-controlevent.md)                     | Notifica al programma di installazione di controllare e impostare un percorso.                                                                                                                                                               |
| [SpawnDialog](spawndialog-controlevent.md)                         | Notifica al programma di installazione di creare un elemento figlio di una casella modale.                                                                                                                                                      |
| [SpawnWaitDialog](spawnwaitdialog-controlevent.md)                 | Attiva una finestra di dialogo specificata.                                                                                                                                                                              |
| [TimeRemaining](timeremaining-controlevent.md)                     | Pubblicata dal programma di installazione per fornire il tempo rimanente nella sequenza di avanzamento.                                                                                                                            |
| [ValidateProductID](validateproductid-controlevent.md)             | Imposta ProductID sull'ID prodotto completo.                                                                                                                                                                        |



 

 

