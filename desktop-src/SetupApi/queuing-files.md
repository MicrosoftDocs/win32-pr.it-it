---
description: Una volta ottenuto un handle per una coda di file chiamando la funzione SetupOpenFileQueue, è possibile aggiungere operazioni su file alla coda, file per file o Accodamento di tutti i file in una sezione INF.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Accodamento di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882065"
---
# <a name="queuing-files"></a>Accodamento di file

Una volta ottenuto un handle per una coda di file chiamando la funzione [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) , è possibile aggiungere operazioni su file alla coda, file per file o Accodamento di tutti i file in una sezione inf.

Per aggiungere un'operazione di copia per un singolo file alla coda di file, chiamare la funzione [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) . Se si desidera accodare un'operazione di copia file utilizzando il supporto di origine predefinito e le destinazioni di destinazione specificate in un file INF, è possibile chiamare la funzione [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) .

È possibile aggiungere un'operazione di eliminazione o ridenominazione dei singoli file alla coda di file aperti, chiamando la funzione [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) o [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) .

 

 



