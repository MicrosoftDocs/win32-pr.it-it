---
description: L'infrastruttura peer non garantisce l'ordine di ricezione ed elaborazione dei record.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Registrare le dipendenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312225"
---
# <a name="record-dependencies"></a><span data-ttu-id="9f82a-103">Registrare le dipendenze</span><span class="sxs-lookup"><span data-stu-id="9f82a-103">Record Dependencies</span></span>

<span data-ttu-id="9f82a-104">L'infrastruttura peer non garantisce l'ordine di ricezione ed elaborazione dei record.</span><span class="sxs-lookup"><span data-stu-id="9f82a-104">The Peer Infrastructure does not guarantee the order for receiving and processing records.</span></span> <span data-ttu-id="9f82a-105">Se l'applicazione ha dipendenze dei record, il che significa che l'elaborazione o la convalida di un record si basa su un altro record, l'applicazione deve essere in grado di gestire le situazioni in cui è possibile che i record vengano ricevuti in ordine arbitrario e imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="9f82a-105">If your application has record dependencies, which means that the processing or validation of one record relies on another record, then your application must be able to handle situations when records might be received in an arbitrary and unpredictable order.</span></span> <span data-ttu-id="9f82a-106">Ad esempio, un'applicazione di chat può avere due tipi di record: un record che contiene informazioni su un utente specifico e un record contenente un messaggio di chat che fa riferimento al record utente.</span><span class="sxs-lookup"><span data-stu-id="9f82a-106">For example, a chat application may have two types of records: a record that contains information about a specific user, and a record that contains a chat message that refers to the user record.</span></span>

<span data-ttu-id="9f82a-107">Un'applicazione deve essere in grado di gestire la situazione di ricezione di un record di messaggio di chat prima del record utente per il messaggio di chat.</span><span class="sxs-lookup"><span data-stu-id="9f82a-107">An application must be able to handle the situation when a chat message record is received before the user record for the chat message.</span></span> <span data-ttu-id="9f82a-108">Un modo per gestire la situazione consiste nell'attendere il record utente usando un **elenco autonomo** o una cache e un timer.</span><span class="sxs-lookup"><span data-stu-id="9f82a-108">One way to handle the situation is to wait for the user record by using a **stand-by list**, or a cache and timer.</span></span> <span data-ttu-id="9f82a-109">L'applicazione può esaminare periodicamente ogni record nell'elenco o nella cache e quindi gestire la situazione quando viene ricevuto il record utente richiesto.</span><span class="sxs-lookup"><span data-stu-id="9f82a-109">The application can periodically examine each record in the list or cache, and then handle the situation when the required user record is received.</span></span>

<span data-ttu-id="9f82a-110">Per gestire le dipendenze dei record, un'applicazione ben progettata è costituita dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f82a-110">To handle record dependencies, a well-designed application consists of the following:</span></span>

-   <span data-ttu-id="9f82a-111">Verifica sempre le dipendenze dei record prima di eseguire un'azione.</span><span class="sxs-lookup"><span data-stu-id="9f82a-111">Always checks for record dependencies before performing an action.</span></span>
-   <span data-ttu-id="9f82a-112">Anticipa le condizioni che possono verificarsi quando i record vengono ricevuti in un ordine imprevisto e quindi gestisce la situazione.</span><span class="sxs-lookup"><span data-stu-id="9f82a-112">Anticipates conditions that might occur when records are received in an unexpected order, and then handles the situation.</span></span>

 

 



