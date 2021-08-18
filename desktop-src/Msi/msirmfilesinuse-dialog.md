---
description: È possibile creare la finestra di dialogo MsiRMFilesInUse per visualizzare un elenco di processi che attualmente eseguono file che devono essere sovrascritti o eliminati dall'installazione.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Finestra di dialogo MsiRMFilesInUse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04aa3167609693135e2d3196fef0495d5244fe44f1a6e7d95d11f999efe51a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012889"
---
# <a name="msirmfilesinuse-dialog"></a>Finestra di dialogo MsiRMFilesInUse

È possibile creare la finestra di dialogo MsiRMFilesInUse per visualizzare un elenco di processi che attualmente eseguono file che devono essere sovrascritti o eliminati dall'installazione. L'utente può scegliere tra le opzioni "Chiudi automaticamente le applicazioni e riavvia le applicazioni" o "Non chiudere le applicazioni. (Sarà necessario un riavvio.)" Se l'utente seleziona l'opzione "Chiudi automaticamente le applicazioni e riavvia le applicazioni", è possibile creare un controllo [](../rstmgr/restart-manager-portal.md) pulsante di comando in questa finestra di dialogo per pubblicare l'evento di controllo RMShutdownAndRestart e Gestione riavvio può chiudere le applicazioni e riavviarle al termine dell'installazione. Ciò può eliminare o ridurre la necessità di riavviare il computer. Per altre informazioni, vedere [Riavvii del sistema.](system-reboots.md)

La **finestra di dialogo MsiRMFilesInUse** viene visualizzata durante un'installazione solo se si verificano tutte le condizioni seguenti. Quando uno di questi valori è false, Windows programma di installazione ignora la finestra di dialogo **MsiRMFilesInUse.**

-   L'installazione viene eseguita in una versione del programma di installazione di Windows non precedente alla versione 4.0 e in un sistema operativo non precedente a Windows Vista o Windows Server 2008.
-   Viene usato il livello [Interfaccia utente completa](user-interface-levels.md) dell'interfaccia utente.
-   Le interazioni con [Gestione riavvio](../rstmgr/restart-manager-portal.md) non sono state disabilitate dalla proprietà [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o dal criterio [DisableAutomaticApplicationShutdown.](disableautomaticapplicationshutdown.md)
-   La **finestra di dialogo MsiRMFilesInUse** è presente nel pacchetto di installazione.
-   Tutte le chiamate dal programma Windows di installazione a [Gestione riavvio](../rstmgr/restart-manager-portal.md) hanno esito positivo.

Questa finestra di dialogo verrà creata come richiesto [dall'azione InstallValidate](installvalidate-action.md).

 

 
