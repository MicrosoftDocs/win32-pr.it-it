---
description: Notifica al programma di Windows di utilizzare Gestione riavvio per arrestare tutte le applicazioni che dispongono di file in uso e riavviarle al termine dell'installazione.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f483e485eeefc2d3a761a3d9c9ff95989a3150dcfd8fff6a36bfb6211504e95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625891"
---
# <a name="rmshutdownandrestart-controlevent"></a>RmShutdownAndRestart ControlEvent

Questo evento notifica al programma di installazione [](../rstmgr/restart-manager-portal.md) di Windows di usare Gestione riavvio per arrestare tutte le applicazioni che dispongono di file in uso e riavviarle al termine dell'installazione.

Questo ControlEvent non ha alcun effetto se si verifica una delle condizioni seguenti.

-   Il sistema operativo che esegue l'installazione non Windows Vista o Windows Server 2008.
-   Le interazioni con [Gestione riavvio](../rstmgr/restart-manager-portal.md) sono state disabilitate dalla proprietà [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o dal [criterio DisableAutomaticApplicationShutdown.](disableautomaticapplicationshutdown.md)
-   Non è attualmente disponibile alcuna sessione [di Gestione riavvio](../rstmgr/restart-manager-portal.md) aperta.
-   Qualsiasi chiamata dal programma di Windows di installazione a [Gestione riavvio](../rstmgr/restart-manager-portal.md) restituisce un errore.

## <a name="typical-use"></a>Utilizzo tipico

L'evento del controllo RMShutdownAndRestart viene pubblicato solo da un controllo [PushButton](pushbutton-control.md) nella finestra di dialogo [MsiRMFilesInUse.](msirmfilesinuse-dialog.md)

 

 
