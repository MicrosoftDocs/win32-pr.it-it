---
title: Annullamento dell'operazione corrente di gestione riavvio
description: Quando un'azione utente indirizza il programma di installazione per eseguire un'azione diversa, è possibile usare il metodo seguente per annullare l'operazione corrente di gestione riavvio.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714659"
---
# <a name="canceling-the-current-restart-manager-operation"></a>Annullamento dell'operazione corrente di gestione riavvio

Quando un'azione utente indirizza il programma di installazione per eseguire un'azione diversa, è possibile usare il metodo seguente per annullare l'operazione corrente di gestione riavvio.

**Per annullare l'operazione corrente di gestione riavvio**

-   Il programma di installazione può chiamare la funzione [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) da un altro thread per annullare l'operazione corrente di [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) . È possibile che la gestione riavvio annulli l'operazione a seconda della misura in cui l'operazione è stata completata quando viene chiamata la funzione **RMCancelCurrentTask** .

 

 




