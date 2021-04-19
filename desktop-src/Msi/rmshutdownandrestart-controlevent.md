---
description: Notifica al Windows Installer di utilizzare Gestione riavvio per arrestare tutte le applicazioni con file in uso e per riavviarle al termine dell'installazione.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: ControlEvent RmShutdownAndRestart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309456"
---
# <a name="rmshutdownandrestart-controlevent"></a><span data-ttu-id="3d631-103">ControlEvent RmShutdownAndRestart</span><span class="sxs-lookup"><span data-stu-id="3d631-103">RmShutdownAndRestart ControlEvent</span></span>

<span data-ttu-id="3d631-104">Questo evento notifica al Windows Installer di utilizzare [Gestione riavvio](../rstmgr/restart-manager-portal.md) per arrestare tutte le applicazioni che hanno file in uso e per riavviarle al termine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="3d631-104">This event notifies the Windows Installer to use the [Restart Manager](../rstmgr/restart-manager-portal.md) to shutdown all applications that have files in use and to restart them at the end of the installation.</span></span>

<span data-ttu-id="3d631-105">Questo ControlEvent non ha alcun effetto se si verifica una delle condizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d631-105">This ControlEvent has no effect if any of the following are true.</span></span>

-   <span data-ttu-id="3d631-106">Il sistema operativo che esegue l'installazione non è Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3d631-106">The operating system running the installation is not Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="3d631-107">Le interazioni con [Gestione riavvio](../rstmgr/restart-manager-portal.md) sono state disabilitate dalla proprietà [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o dal criterio [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="3d631-107">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="3d631-108">Attualmente non è presente alcuna sessione di [Gestione riavvio](../rstmgr/restart-manager-portal.md) aperta.</span><span class="sxs-lookup"><span data-stu-id="3d631-108">There is currently no open [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>
-   <span data-ttu-id="3d631-109">Tutte le chiamate dal Windows Installer alla [Gestione riavvio](../rstmgr/restart-manager-portal.md) restituiscono un errore.</span><span class="sxs-lookup"><span data-stu-id="3d631-109">Any calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) returns a failure.</span></span>

## <a name="typical-use"></a><span data-ttu-id="3d631-110">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="3d631-110">Typical Use</span></span>

<span data-ttu-id="3d631-111">L'evento di controllo RMShutdownAndRestart viene pubblicato solo da un controllo [pulsante](pushbutton-control.md) nella finestra di [dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="3d631-111">The RMShutdownAndRestart control event is published only by a [PushButton](pushbutton-control.md) control on the [MsiRMFilesInUse Dialog](msirmfilesinuse-dialog.md) box.</span></span>

 

 
