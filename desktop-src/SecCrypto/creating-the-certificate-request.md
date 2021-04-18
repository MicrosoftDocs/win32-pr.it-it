---
description: Il processo di creazione di una richiesta di certificato comporta la raccolta di determinate informazioni dal richiedente.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Creazione della richiesta di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306466"
---
# <a name="creating-the-certificate-request"></a><span data-ttu-id="5b8ca-103">Creazione della richiesta di certificato</span><span class="sxs-lookup"><span data-stu-id="5b8ca-103">Creating the Certificate Request</span></span>

<span data-ttu-id="5b8ca-104">Il processo di creazione di una richiesta di certificato comporta la raccolta di determinate informazioni dal richiedente.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-104">The process of creating a certificate request involves collecting certain information from the requester.</span></span> <span data-ttu-id="5b8ca-105">In genere, questa operazione viene eseguita tramite una sorta di interfaccia utente, sebbene le informazioni possano essere ricavate direttamente da un database senza la necessità di un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-105">Usually, this is done through some sort of user interface (UI), although the information could be taken directly from a database without the need for a UI.</span></span> <span data-ttu-id="5b8ca-106">Il livello delle informazioni richieste viene impostato in base ai criteri dell' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="5b8ca-106">The level of information required is set by the policy of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="5b8ca-107">Un esempio delle informazioni necessarie potrebbe essere il seguente:</span><span class="sxs-lookup"><span data-stu-id="5b8ca-107">An example of the required information might be as follows:</span></span>

-   <span data-ttu-id="5b8ca-108">Nome comune</span><span class="sxs-lookup"><span data-stu-id="5b8ca-108">Common Name</span></span>
-   <span data-ttu-id="5b8ca-109">Nome unità</span><span class="sxs-lookup"><span data-stu-id="5b8ca-109">Unit Name</span></span>
-   <span data-ttu-id="5b8ca-110">Nome società</span><span class="sxs-lookup"><span data-stu-id="5b8ca-110">Company Name</span></span>
-   <span data-ttu-id="5b8ca-111">City</span><span class="sxs-lookup"><span data-stu-id="5b8ca-111">City</span></span>
-   <span data-ttu-id="5b8ca-112">State</span><span class="sxs-lookup"><span data-stu-id="5b8ca-112">State</span></span>
-   <span data-ttu-id="5b8ca-113">Paese/Area geografica</span><span class="sxs-lookup"><span data-stu-id="5b8ca-113">Country/Region</span></span>

> [!Note]  
> <span data-ttu-id="5b8ca-114">L'interfaccia è progettata per eseguire una singola richiesta per ogni istanza di Xenroll.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-114">The interface is designed to make a single request for each xenroll instance.</span></span> <span data-ttu-id="5b8ca-115">Per creare ogni [*richiesta di certificato*](../secgloss/c-gly.md), è necessario creare un'istanza di Xenroll distinta.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-115">A separate xenroll instance must be created to create each [*certificate request*](../secgloss/c-gly.md).</span></span>

 

<span data-ttu-id="5b8ca-116">Per informazioni su come usare il controllo di registrazione certificati per richiedere un certificato in linguaggi di programmazione specifici, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b8ca-116">For information about how to use the Certificate Enrollment Control to request a certificate in specific programming languages, see the following topics:</span></span>

-   [<span data-ttu-id="5b8ca-117">Esempio di richiesta in C++</span><span class="sxs-lookup"><span data-stu-id="5b8ca-117">Request Sample in C++</span></span>](request-sample-in-c-.md)
-   [<span data-ttu-id="5b8ca-118">Esempio di richiesta in VBScript</span><span class="sxs-lookup"><span data-stu-id="5b8ca-118">Request Sample in VBScript</span></span>](request-sample-in-vbscript.md)

 

 
