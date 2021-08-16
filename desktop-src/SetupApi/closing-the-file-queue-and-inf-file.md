---
description: Al termine del commit, la coda deve essere chiusa usando la funzione SetupCloseFileQueue con l'handle creato da SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Chiusura della coda di file e del file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce5c81c75f7515acfb346b4277e416b0cb2c2a9be6e40464dcfdfc21c3b23bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887576"
---
# <a name="closing-the-file-queue-and-inf-file"></a>Chiusura della coda di file e del file INF

Al termine del commit, la coda deve essere chiusa usando la [**funzione SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) con l'handle creato da [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue). Il callback predefinito della coda deve essere eliminato e ricreato prima di poter eseguire il commit di un'altra coda.

Se un contesto predefinito è stato avviato per l'uso dalla routine di callback predefinita, deve essere terminato anche chiamando la [**funzione SetupTermDefaultQueueCallback.**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) *Context è* un puntatore alla struttura restituita dalla [**funzione SetupInitDefaultQueueCallback.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)

Quando l'accesso alle informazioni INF non è più necessario, chiamare la funzione [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) con l'handle creato da [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) per liberare le risorse di sistema.

 

 



