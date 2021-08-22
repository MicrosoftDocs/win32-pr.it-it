---
title: Annullamento dell'operazione corrente di Gestione riavvio
description: Quando un'azione dell'utente indica al programma di installazione di eseguire un'azione diversa, è possibile usare il metodo seguente per annullare l'operazione corrente di Gestione riavvio.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c745a76ab8c72acaff0b9f1ae85ded380e1113c3687822e916b422cad9ef51f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010249"
---
# <a name="canceling-the-current-restart-manager-operation"></a>Annullamento dell'operazione corrente di Gestione riavvio

Quando un'azione dell'utente indica al programma di installazione di eseguire un'azione diversa, è possibile usare il metodo seguente per annullare l'operazione corrente di Gestione riavvio.

**Per annullare l'operazione corrente di Gestione riavvio**

-   Il programma di installazione può chiamare la [**funzione RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) da un altro thread per annullare l'operazione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) corrente. Gestione riavvio può annullare l'operazione a seconda della misura in cui l'operazione è stata completata quando viene chiamata la funzione **RMCancelCurrentTask.**

 

 




