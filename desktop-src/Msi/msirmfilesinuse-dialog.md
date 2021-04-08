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
# <a name="msirmfilesinuse-dialog"></a><span data-ttu-id="e8a8a-103">Finestra di dialogo MsiRMFilesInUse</span><span class="sxs-lookup"><span data-stu-id="e8a8a-103">MsiRMFilesInUse Dialog</span></span>

<span data-ttu-id="e8a8a-104">La finestra di dialogo MsiRMFilesInUse può essere creata per visualizzare un elenco di processi che eseguono file che devono essere sovrascritti o eliminati dall'installazione.</span><span class="sxs-lookup"><span data-stu-id="e8a8a-104">The MsiRMFilesInUse Dialog box can be authored to display a list of processes that are currently running files that need to be overwritten or deleted by the installation.</span></span> <span data-ttu-id="e8a8a-105">L'utente può scegliere tra le opzioni "Chiudi automaticamente le applicazioni e riavviarle" oppure "non chiudere le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e8a8a-105">The user can select between options to "Automatically close applications and restart them" or "Do not close applications.</span></span> <span data-ttu-id="e8a8a-106">(Sarà necessario riavviare il computer) ". Se l'utente seleziona l'opzione "Chiudi automaticamente le applicazioni e riavvia", è possibile creare un controllo pulsante di comando in questa finestra di dialogo per pubblicare l'evento di controllo RMShutdownAndRestart e [Gestione riavvio](../rstmgr/restart-manager-portal.md) può chiudere le applicazioni e riavviarle al termine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="e8a8a-106">(A reboot will be required.)" If the user selects the "Automatically close applications and restart them" option, a push button control on this dialog box can be authored to publish the RMShutdownAndRestart control event and the [Restart Manager](../rstmgr/restart-manager-portal.md) can close the applications and restart them at the end of the installation.</span></span> <span data-ttu-id="e8a8a-107">In questo modo è possibile eliminare o ridurre la necessità di riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="e8a8a-107">This can eliminate or reduce the need to restart the computer.</span></span> <span data-ttu-id="e8a8a-108">Per ulteriori informazioni, vedere [riavvii del sistema](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="e8a8a-108">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="e8a8a-109">La finestra di dialogo **MsiRMFilesInUse** viene visualizzata durante un'installazione solo se si verificano tutte le condizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8a8a-109">The **MsiRMFilesInUse** dialog box is displayed during an installation only if all the following are true.</span></span> <span data-ttu-id="e8a8a-110">Quando uno di questi è false, il Windows Installer ignora la finestra di dialogo **MsiRMFilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="e8a8a-110">When any of these are false, the Windows Installer ignores the **MsiRMFilesInUse** dialog box.</span></span>

-   <span data-ttu-id="e8a8a-111">Un Windows Installer versione precedente alla versione 4,0 e un sistema operativo che non è precedente a Windows Vista o Windows Server 2008 sta eseguendo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e8a8a-111">A Windows Installer version that is not earlier than version 4.0 and an operating system that is not earlier than Windows Vista or Windows Server 2008 is running the installation.</span></span>
-   <span data-ttu-id="e8a8a-112">Viene usato il [livello di interfaccia utente completo dell'interfaccia utente](user-interface-levels.md) .</span><span class="sxs-lookup"><span data-stu-id="e8a8a-112">The Full UI [user interface level](user-interface-levels.md) is used.</span></span>
-   <span data-ttu-id="e8a8a-113">Le interazioni con [Gestione riavvio](../rstmgr/restart-manager-portal.md) non sono state disabilitate dalla proprietà [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o dal criterio [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="e8a8a-113">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have not been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="e8a8a-114">La finestra di dialogo **MsiRMFilesInUse** è presente nel pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="e8a8a-114">The **MsiRMFilesInUse** dialog box is present in the installation package.</span></span>
-   <span data-ttu-id="e8a8a-115">Tutte le chiamate dal Windows Installer alla [Gestione riavvio](../rstmgr/restart-manager-portal.md) hanno avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e8a8a-115">All calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) are successful.</span></span>

<span data-ttu-id="e8a8a-116">Questa finestra di dialogo verrà creata come richiesto dall' [azione InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="e8a8a-116">This dialog box will be created as required by the [InstallValidate action](installvalidate-action.md).</span></span>

 

 
