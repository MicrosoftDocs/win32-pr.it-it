---
description: Se la funzione di callback predefinita verrà chiamata durante l'impegno della coda, il contesto per la coda deve essere inizializzato usando le funzioni SetupInitDefaultQueueCallback o SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Commit della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67c19b91cc25e5107f91fbd241d96147137a38b8544568e57ea3bbbd58981a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887522"
---
# <a name="committing-the-queue"></a>Commit della coda

Se la funzione di callback predefinita verrà chiamata durante l'impegno della coda, il contesto per la coda deve essere inizializzato usando le funzioni [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) Se si usa una funzione di callback personalizzata che non chiama mai la funzione di callback predefinita, questo passaggio non è necessario.

Dopo aver compilato la coda e aver inizializzato la funzione di callback che eelaborare le notifiche della coda, è possibile chiamare [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) per eseguire il commit delle operazioni accodati.

Nell'esempio seguente viene [**utilizzato SetupCommitFileQueue per**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) eseguire il commit della coda usando la routine di callback predefinita.

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

Nell'esempio precedente MyQueue è la coda di cui eseguire il commit, OwnerWindow è la finestra proprietaria di tutte le finestre di dialogo create dalla routine di callback predefinita, SetupDefaultQueueCallback specifica che verrà usata la funzione di callback predefinita e *Context* è un puntatore alla struttura restituita dalla chiamata precedente a [**SetupInitDefaultQueueCallback.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)

 

 



