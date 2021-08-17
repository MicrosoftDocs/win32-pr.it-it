---
description: Prima di poter usare la routine di callback della coda predefinita, specificandola come routine di callback quando si esegue il commit di una coda di file o chiamandola da una routine di callback personalizzata, è necessario inizializzarla.
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: Inizializzazione e terminazione del contesto di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67df0707f91a17369503fa17ecbeefef3eb6827be60285b0b778b07d98eba3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965434"
---
# <a name="initializing-and-terminating-the-callback-context"></a>Inizializzazione e terminazione del contesto di callback

Prima di poter usare la routine di callback della coda predefinita, specificandola come routine di callback quando si esegue il commit di una coda di file o chiamandola da una routine di callback personalizzata, è necessario inizializzarla.

La [**funzione SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) compila la struttura del contesto usata dalla routine di callback della coda predefinita. Restituisce un puntatore void a tale struttura. Questa struttura è essenziale per l'operazione della routine di callback predefinita e deve essere passata alla routine di callback. A tale scopo, è possibile specificare il puntatore void come contesto in una chiamata a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)o specificando il puntatore void come parametro di contesto quando si chiama [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) da una routine di callback personalizzata. Questa struttura del contesto non deve essere modificata o a cui fa riferimento l'applicazione di installazione.

La [**funzione SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) inizializza anche un contesto per la routine di callback della coda predefinita, ma specifica una seconda finestra per ricevere un messaggio di stato specificato dal chiamante ogni volta che la coda invia una notifica. In questo modo è possibile usare le finestre di dialogo di richiesta e di errore predefinite del disco e incorporare anche un indicatore di stato in una seconda finestra, ad esempio in una pagina di un'installazione guidata.

Indipendentemente dal fatto che sia stato inizializzato il contesto usato dalla routine di callback della coda predefinita con [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx,**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)al termine dell'elaborazione delle operazioni in coda, chiamare [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) per rilasciare le risorse allocate nell'inizializzazione della struttura del contesto.

 

 



