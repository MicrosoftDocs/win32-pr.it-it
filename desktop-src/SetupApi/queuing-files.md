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
# <a name="queuing-files"></a><span data-ttu-id="f0047-103">Accodamento di file</span><span class="sxs-lookup"><span data-stu-id="f0047-103">Queuing Files</span></span>

<span data-ttu-id="f0047-104">Una volta ottenuto un handle per una coda di file chiamando la funzione [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) , è possibile aggiungere operazioni su file alla coda, file per file o Accodamento di tutti i file in una sezione inf.</span><span class="sxs-lookup"><span data-stu-id="f0047-104">After you have obtained a handle to a file queue by calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function, you can add file operations to the queue, either file-by-file, or by queuing all the files in an INF section.</span></span>

<span data-ttu-id="f0047-105">Per aggiungere un'operazione di copia per un singolo file alla coda di file, chiamare la funzione [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) .</span><span class="sxs-lookup"><span data-stu-id="f0047-105">To add a copy operation for an individual file to the file queue, call the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) function.</span></span> <span data-ttu-id="f0047-106">Se si desidera accodare un'operazione di copia file utilizzando il supporto di origine predefinito e le destinazioni di destinazione specificate in un file INF, è possibile chiamare la funzione [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) .</span><span class="sxs-lookup"><span data-stu-id="f0047-106">If you want to queue a file copy operation using the default source media and target destinations specified in an INF file, you can call the [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) function.</span></span>

<span data-ttu-id="f0047-107">È possibile aggiungere un'operazione di eliminazione o ridenominazione dei singoli file alla coda di file aperti, chiamando la funzione [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) o [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) .</span><span class="sxs-lookup"><span data-stu-id="f0047-107">You can add an individual file delete or rename operation to the open file queue, by calling the [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) or [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) function.</span></span>

 

 



