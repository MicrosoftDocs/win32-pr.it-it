---
description: Le funzioni seguenti vengono utilizzate con le code di file.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Funzioni della coda di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314655"
---
# <a name="file-queue-functions"></a>Funzioni della coda di file

Le funzioni seguenti vengono utilizzate con le code di file.



| Funzione                                                             | Descrizione                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | Termina la coda. Non viene eseguito il commit di tutte le transazioni rimanenti.                                   |
| [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | Esegui il commit di tutte le transazioni in coda.                                                                      |
| [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | Inizializza e restituisce un handle per la coda di file.                                                   |
| [**SetupPromptReboot**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | Richiede all'utente di riavviare il computer, se necessario.                                         |
| [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | Accoda una copia del file.                                                                                   |
| [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | Accoda i file in una sezione dei file di copia INF.                                                        |
| [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | Accoda i file in una sezione dei file di copia INF usando le informazioni predefinite specificate in un file INF. |
| [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | Accoda un'eliminazione di file.                                                                               |
| [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | Accoda i file in una sezione dei file di eliminazione INF.                                                      |
| [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | Accoda una ridenominazione del file.                                                                                 |
| [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | Accoda i file in una sezione dei file di ridenominazione INF.                                                      |
| [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | Esegue l'analisi della coda di file.                                                                                 |
| [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | Imposta l'override del percorso della piattaforma.                                                                      |



 

 

 



