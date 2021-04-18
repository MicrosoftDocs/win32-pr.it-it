---
description: Al termine del commit delle operazioni da parte della coda, è necessario chiuderla utilizzando la funzione SetupCloseFileQueue con l'handle creato da SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Chiusura della coda di file e del file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319335"
---
# <a name="closing-the-file-queue-and-inf-file"></a>Chiusura della coda di file e del file INF

Al termine del commit delle operazioni da parte della coda, è necessario chiuderla utilizzando la funzione [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) con l'handle creato da [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue). Il callback predefinito della coda deve essere eliminato e ricreato prima che sia possibile eseguire il commit di un'altra coda.

Se è stato avviato un contesto predefinito per l'utilizzo da parte della routine di callback predefinita, è necessario terminare anche chiamando la funzione [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) . Il *contesto* è un puntatore alla struttura restituita dalla funzione [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .

Quando l'accesso alle informazioni INF non è più necessario, chiamare la funzione [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) con l'handle creato da [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) per liberare risorse di sistema.

 

 



