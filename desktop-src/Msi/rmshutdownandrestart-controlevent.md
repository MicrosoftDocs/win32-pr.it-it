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
# <a name="rmshutdownandrestart-controlevent"></a>ControlEvent RmShutdownAndRestart

Questo evento notifica al Windows Installer di utilizzare [Gestione riavvio](../rstmgr/restart-manager-portal.md) per arrestare tutte le applicazioni che hanno file in uso e per riavviarle al termine dell'installazione.

Questo ControlEvent non ha alcun effetto se si verifica una delle condizioni seguenti.

-   Il sistema operativo che esegue l'installazione non è Windows Vista o Windows Server 2008.
-   Le interazioni con [Gestione riavvio](../rstmgr/restart-manager-portal.md) sono state disabilitate dalla proprietà [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o dal criterio [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   Attualmente non è presente alcuna sessione di [Gestione riavvio](../rstmgr/restart-manager-portal.md) aperta.
-   Tutte le chiamate dal Windows Installer alla [Gestione riavvio](../rstmgr/restart-manager-portal.md) restituiscono un errore.

## <a name="typical-use"></a>Utilizzo tipico

L'evento di controllo RMShutdownAndRestart viene pubblicato solo da un controllo [pulsante](pushbutton-control.md) nella finestra di [dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) .

 

 
