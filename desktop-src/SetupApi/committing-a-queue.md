---
description: Dopo che tutte le operazioni di file desiderate sono state accodate, è necessario eseguire il commit della coda. In questo modo verranno elaborate le operazioni dei file accodati.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Commit di una coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759791"
---
# <a name="committing-a-queue"></a>Commit di una coda

Dopo che tutte le operazioni di file desiderate sono state accodate, è necessario eseguire il commit della coda. In questo modo verranno elaborate le operazioni dei file accodati.

Non è possibile riutilizzare una coda di file dopo che è stato eseguito il commit. La procedura consigliata consiste nel raccogliere tutte le operazioni di file necessarie per la coda di file ed eseguire il commit della coda una sola volta. Se è necessaria un'elaborazione aggiuntiva della coda dopo che è stato eseguito il commit, è necessario chiudere l'handle per la coda e creare una nuova coda di file. Per eseguire il commit della coda di file, chiamare la funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , specificando una routine di callback. La routine di callback riceverà le notifiche da **SetupCommitFileQueue** durante l'elaborazione delle operazioni sui file. Se si desidera utilizzare la routine di callback della coda predefinita, è innanzitutto necessario inizializzare il contesto necessario chiamando [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex). Per ulteriori informazioni sulla routine di callback della coda predefinita, vedere [routine di callback](default-queue-callback-routine.md)della coda predefinita.

> [!Note]  
> [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) deve essere chiamato prima che la coda venga chiusa. Tutte le operazioni di cui non è stato eseguito il commit quando viene chiamato [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) non verranno eseguite.

 

 

 



