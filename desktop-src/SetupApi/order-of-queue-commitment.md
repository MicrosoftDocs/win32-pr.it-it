---
description: "Quando la funzione SetupCommitFileQueue esegue il commit della coda di file, elabora le operazioni sui file nell'ordine seguente: operazioni di eliminazione di file, quindi operazioni di ridenominazione dei file e infine operazioni di copia dei file."
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Ordine di impegno della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882361"
---
# <a name="order-of-queue-commitment"></a>Ordine di impegno della coda

Quando la funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) esegue il commit della coda di file, elabora le operazioni sui file nell'ordine seguente: operazioni di eliminazione di file, quindi operazioni di ridenominazione dei file e infine operazioni di copia dei file. Nella struttura seguente viene illustrato il ciclo di vita del processo di impegno di una coda.

 

-   avvia la coda secondaria Delete
    -   avvia un'operazione di eliminazione file <--REPEAT per ogni
    -   termina un'operazione di eliminazione file <--eliminazione file in coda
-   terminare la coda secondaria Delete

<!-- -->

-   avviare la ridenominazione della coda secondaria
    -   avviare un'operazione di ridenominazione dei file <--REPEAT per ogni
    -   termina un'operazione di eliminazione file <--Rinomina file in coda
-   terminare la ridenominazione della coda secondaria

<!-- -->

-   avviare la copia subque
    -   avviare un'operazione di copia dei file <--REPEAT per ogni
    -   termina un'operazione di copia file < la copia del file in coda
    -   terminare la coda secondaria di copia
-   termina la coda

 

A ogni passaggio o, se si verifica un errore, la funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) invia una notifica alla routine di callback. La routine di callback può utilizzare le informazioni inviate dalla coda per tenere traccia dello stato di avanzamento dell'installazione e, se necessario, interagire con l'utente.

Se, ad esempio, un'operazione di copia file richiede un file di origine non disponibile nel percorso corrente, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) invierà una \_ notifica SPFILENOTIFY NEEDMEDIA alla routine di callback, insieme alle informazioni sul file e sui supporti necessari. La routine di callback può utilizzare queste informazioni per generare una finestra di dialogo in cui viene richiesto all'utente di inserire il disco successivo chiamando [ **SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)

Con l'API di installazione di è inclusa una routine di callback della coda predefinita, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka). Questa routine gestisce le notifiche della coda e genera finestre di dialogo di errore e indicatori di stato per l'installazione. È possibile utilizzare la routine di callback della coda predefinita, oppure scrivere una routine di callback del filtro per gestire un subset delle notifiche e passare le altre alla routine di callback della coda predefinita.

Se nessuna delle funzionalità della routine di callback soddisfa le proprie esigenze, è possibile scrivere una routine di callback personalizzata autonoma che non chiami la routine di callback della coda predefinita.

Per altre informazioni sulle routine di callback della coda, vedere [routine di callback della coda predefinita](default-queue-callback-routine.md)e [creazione di una routine di callback della coda personalizzata](creating-a-custom-queue-callback-routine.md).

 

 



