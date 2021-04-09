---
title: Contenitori e server
description: Contenitori e server
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856905"
---
# <a name="containers-and-servers"></a><span data-ttu-id="68a96-103">Contenitori e server</span><span class="sxs-lookup"><span data-stu-id="68a96-103">Containers and Servers</span></span>

<span data-ttu-id="68a96-104">Le applicazioni per documenti composti sono di due tipi di base: applicazioni contenitore e applicazioni server.</span><span class="sxs-lookup"><span data-stu-id="68a96-104">Compound document applications are of two basic types: container applications and server applications.</span></span> <span data-ttu-id="68a96-105">Le applicazioni contenitore OLE offrono agli utenti la possibilità di creare, modificare, salvare e recuperare documenti composti.</span><span class="sxs-lookup"><span data-stu-id="68a96-105">OLE container applications provide users with the ability to create, edit, save, and retrieve compound documents.</span></span> <span data-ttu-id="68a96-106">Le applicazioni server OLE forniscono agli utenti i mezzi per creare documenti e altre rappresentazioni dati che possono essere contenuti come collegamenti o incorporamenti nelle applicazioni contenitore.</span><span class="sxs-lookup"><span data-stu-id="68a96-106">OLE server applications provide users with the means to create documents and other data representations that can be contained as either links or embeddings in container applications.</span></span> <span data-ttu-id="68a96-107">Un'applicazione OLE può essere un'applicazione contenitore, un'applicazione server o entrambe.</span><span class="sxs-lookup"><span data-stu-id="68a96-107">An OLE application can be a container application, a server application, or both.</span></span>

<span data-ttu-id="68a96-108">Le applicazioni server OLE variano inoltre a seconda che siano implementate come *server in-process* o *server locali*.</span><span class="sxs-lookup"><span data-stu-id="68a96-108">OLE server applications also differ in whether they are implemented as *in-process servers* or *local servers*.</span></span> <span data-ttu-id="68a96-109">Un server in-process è una libreria a collegamento dinamico (DLL) eseguita nello spazio di processo dell'applicazione contenitore.</span><span class="sxs-lookup"><span data-stu-id="68a96-109">An in-process server is a dynamic link library (DLL) that runs in the container application's process space.</span></span> <span data-ttu-id="68a96-110">È possibile eseguire un server in-process solo dall'interno dell'applicazione contenitore.</span><span class="sxs-lookup"><span data-stu-id="68a96-110">You can run an in-process server only from within the container application.</span></span>

> [!Note]  
> <span data-ttu-id="68a96-111">Le versioni future di OLE consentiranno il collegamento e l'incorporamento tra i limiti del computer, in modo che un'applicazione contenitore in un computer sarà in grado di utilizzare un oggetto documento composto fornito da un *server remoto* in esecuzione in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="68a96-111">Future releases of OLE will enable linking and embedding across computer boundaries, so that a container application on one computer will be able to use a compound document object provided by a *remote server* running on another computer.</span></span> <span data-ttu-id="68a96-112">Dal punto di vista di un'applicazione contenitore, qualsiasi applicazione server OLE eseguita nello stesso spazio di processo, sia nello stesso computer che in un computer remoto, è un *Server processÂ*.</span><span class="sxs-lookup"><span data-stu-id="68a96-112">From a container application's point of view, any OLE server application that runs in its own process space, whether on the same computer or a remote computer, is an *out-of-processÂ server*.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="68a96-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68a96-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68a96-114">Documenti composti</span><span class="sxs-lookup"><span data-stu-id="68a96-114">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="68a96-115">Server in-process</span><span class="sxs-lookup"><span data-stu-id="68a96-115">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




