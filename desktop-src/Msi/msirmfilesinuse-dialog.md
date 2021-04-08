---
description: La finestra di dialogo MsiRMFilesInUse può essere creata per visualizzare un elenco di processi che eseguono file che devono essere sovrascritti o eliminati dall'installazione.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Finestra di dialogo MsiRMFilesInUse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bba73cab51f4b3d8321b15001dbb72c638176b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968513"
---
# <a name="msirmfilesinuse-dialog"></a>Finestra di dialogo MsiRMFilesInUse

La finestra di dialogo MsiRMFilesInUse può essere creata per visualizzare un elenco di processi che eseguono file che devono essere sovrascritti o eliminati dall'installazione. L'utente può scegliere tra le opzioni "Chiudi automaticamente le applicazioni e riavviarle" oppure "non chiudere le applicazioni. (Sarà necessario riavviare il computer) ". Se l'utente seleziona l'opzione "Chiudi automaticamente le applicazioni e riavvia", è possibile creare un controllo pulsante di comando in questa finestra di dialogo per pubblicare l'evento di controllo RMShutdownAndRestart e [Gestione riavvio](../rstmgr/restart-manager-portal.md) può chiudere le applicazioni e riavviarle al termine dell'installazione. In questo modo è possibile eliminare o ridurre la necessità di riavviare il computer. Per ulteriori informazioni, vedere [riavvii del sistema](system-reboots.md).

La finestra di dialogo **MsiRMFilesInUse** viene visualizzata durante un'installazione solo se si verificano tutte le condizioni seguenti. Quando uno di questi è false, il Windows Installer ignora la finestra di dialogo **MsiRMFilesInUse** .

-   Un Windows Installer versione precedente alla versione 4,0 e un sistema operativo che non è precedente a Windows Vista o Windows Server 2008 sta eseguendo l'installazione.
-   Viene usato il [livello di interfaccia utente completo dell'interfaccia utente](user-interface-levels.md) .
-   Le interazioni con [Gestione riavvio](../rstmgr/restart-manager-portal.md) non sono state disabilitate dalla proprietà [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o dal criterio [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   La finestra di dialogo **MsiRMFilesInUse** è presente nel pacchetto di installazione.
-   Tutte le chiamate dal Windows Installer alla [Gestione riavvio](../rstmgr/restart-manager-portal.md) hanno avuto esito positivo.

Questa finestra di dialogo verrà creata come richiesto dall' [azione InstallValidate](installvalidate-action.md).

 

 
