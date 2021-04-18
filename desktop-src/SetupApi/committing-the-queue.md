---
description: Se la funzione di callback predefinita verrà chiamata durante l'impegno della coda, il contesto per esso deve essere inizializzato usando le funzioni SetupInitDefaultQueueCallback o SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Commit della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ed721c60457a77a168218aa0294bf448889129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313284"
---
# <a name="committing-the-queue"></a>Commit della coda

Se la funzione di callback predefinita verrà chiamata durante l'impegno della coda, il contesto per esso deve essere inizializzato usando le funzioni [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) . Se si usa una funzione di callback personalizzata che non chiama mai la funzione di callback predefinita, questo passaggio non è necessario.

Dopo che la coda è stata compilata e la funzione di callback che elaborerà le notifiche della coda è stata inizializzata, è possibile chiamare [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) per eseguire il commit delle operazioni accodate.

Nell'esempio seguente viene usato [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) per eseguire il commit della coda usando la routine di callback predefinita.

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

Nell'esempio precedente, la coda è la coda di cui eseguire il commit, OwnerWindow è la finestra che sarà proprietaria di tutte le finestre di dialogo create dalla routine di callback predefinita, SetupDefaultQueueCallback specifica che verrà usata la funzione di callback predefinita e *context* è un puntatore alla struttura restituita dalla chiamata precedente a [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).

 

 



