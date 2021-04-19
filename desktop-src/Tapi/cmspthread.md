---
description: La classe CMSPThread implementa il thread di lavoro MSPs.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317650"
---
# <a name="cmspthread"></a><span data-ttu-id="18bf8-103">CMSPThread</span><span class="sxs-lookup"><span data-stu-id="18bf8-103">CMSPThread</span></span>

<span data-ttu-id="18bf8-104">La classe **CMSPThread** implementa il thread di lavoro di msp.</span><span class="sxs-lookup"><span data-stu-id="18bf8-104">The **CMSPThread** class implements the MSP's worker thread.</span></span> <span data-ttu-id="18bf8-105">Le classi base usano questo thread di lavoro per diversi scopi.</span><span class="sxs-lookup"><span data-stu-id="18bf8-105">The base classes use this worker thread for a number of purposes.</span></span> <span data-ttu-id="18bf8-106">Viene fornito un meccanismo di elemento di lavoro generico e leggero che consente all'MSP derivato di utilizzare questo thread per i propri elementi di lavoro sincroni o asincroni, indipendentemente dal fatto che si verifichino.</span><span class="sxs-lookup"><span data-stu-id="18bf8-106">A generic and lightweight work item mechanism is provided to allow the derived MSP to use this thread for its own synchronous or asynchronous work items, whatever they may be.</span></span> <span data-ttu-id="18bf8-107">Il thread pompa inoltre i messaggi e supporta la gestione di APC (anche se non vengono utilizzati APC nelle classi base).</span><span class="sxs-lookup"><span data-stu-id="18bf8-107">The thread also pumps messages and supports handling of APCs (although APCs are not used in the base classes).</span></span>

<span data-ttu-id="18bf8-108">Quando sono presenti più indirizzi like, ovvero quando viene creata più volte la stessa implementazione di MSP della stessa DLL, la classe thread garantisce la scalabilità utilizzando automaticamente un singolo thread per tutti gli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="18bf8-108">When multiple like addresses are present (that is, when the same MSP implementation from the same DLL is instantiated multiple times), the thread class ensures scalability by automatically using a single thread for all the addresses.</span></span> <span data-ttu-id="18bf8-109">L'interfaccia alla classe thread è tale che l'implementazione MSP può considerare la classe thread come un thread privato e non deve preoccuparsi degli altri indirizzi che potrebbero condividerla.</span><span class="sxs-lookup"><span data-stu-id="18bf8-109">The interface to the thread class is such that the MSP implementation can think of the thread class as a private thread and need not care about the other addresses that may be sharing it.</span></span>

<span data-ttu-id="18bf8-110">Definito in MSPthrd. h.</span><span class="sxs-lookup"><span data-stu-id="18bf8-110">Defined in MSPthrd.h.</span></span>

 

 



