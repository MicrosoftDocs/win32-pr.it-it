---
description: Prima di poter utilizzare la routine di callback della coda predefinita, specificarla come routine di callback quando si esegue il commit di una coda di file oppure chiamandola da una routine di callback personalizzata, è necessario inizializzarla.
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: Inizializzazione e terminazione del contesto di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cb4c144cb9069d395ccd688e2a172680df8a12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315322"
---
# <a name="initializing-and-terminating-the-callback-context"></a>Inizializzazione e terminazione del contesto di callback

Prima di poter utilizzare la routine di callback della coda predefinita, specificarla come routine di callback quando si esegue il commit di una coda di file oppure chiamandola da una routine di callback personalizzata, è necessario inizializzarla.

La funzione [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) compila la struttura del contesto utilizzata dalla routine di callback della coda predefinita. Restituisce un puntatore void a tale struttura. Questa struttura è essenziale per l'operazione predefinita della routine di callback e deve essere passata alla routine di callback. Questa operazione può essere eseguita specificando il puntatore void come contesto in una chiamata a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)o specificando il puntatore void come parametro di contesto quando si chiama [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) da una routine di callback personalizzata. Questa struttura del contesto non deve essere modificata o a cui fa riferimento l'applicazione di installazione.

La funzione [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) Inizializza anche un contesto per la routine di callback della coda predefinita, ma specifica una seconda finestra per ricevere un messaggio di stato specificato dal chiamante ogni volta che la coda Invia una notifica. In questo modo è possibile utilizzare le finestre di dialogo richieste disco predefinite e di errore e incorporare anche un indicatore di stato in una seconda finestra, ad esempio, in una pagina di un'installazione guidata di.

Indipendentemente dal fatto che sia stato inizializzato il contesto utilizzato dalla routine di callback della coda predefinita con [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex), al termine dell'elaborazione delle operazioni in coda, chiamare [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) per rilasciare le risorse allocate durante l'inizializzazione della struttura del contesto.

 

 



