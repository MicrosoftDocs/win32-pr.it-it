---
description: Le funzioni seguenti vengono usate con le code di file.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Funzioni di accodamento file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70087bfcc00f2c3d86c93cc62081adc9aa50705d248d79a524435c95f480562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887080"
---
# <a name="file-queue-functions"></a>Funzioni di accodamento file

Le funzioni seguenti vengono usate con le code di file.



| Funzione                                                             | Descrizione                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | Termina la coda. Non viene eseguito il commit delle transazioni rimanenti.                                   |
| [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | Esegue il commit di tutte le transazioni in coda.                                                                      |
| [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | Inizializza e restituisce un handle alla coda di file.                                                   |
| [**SetupPromptReboot**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | Richiede all'utente di riavviare il computer, se necessario.                                         |
| [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | Accoda una copia di file.                                                                                   |
| [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | Accoda i file in una sezione Di copia file INF.                                                        |
| [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | Accoda i file in una sezione InF Copy Files usando le informazioni predefinite specificate in un file INF. |
| [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | Accoda un file eliminato.                                                                               |
| [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | Accoda i file in una sezione INF Delete Files.                                                      |
| [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | Accoda un file rinominato.                                                                                 |
| [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | Accoda i file in una sezione inf rename files.                                                      |
| [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | Analizza la coda di file.                                                                                 |
| [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | Imposta l'override del percorso della piattaforma.                                                                      |



 

 

 



