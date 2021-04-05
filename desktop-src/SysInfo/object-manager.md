---
description: Un oggetto è costituito da un'intestazione standard e da attributi specifici dell'oggetto. Poiché tutti gli oggetti hanno la stessa struttura, in Windows è disponibile un singolo gestore di oggetti che gestisce tutti gli oggetti.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Gestore oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967995"
---
# <a name="object-manager"></a><span data-ttu-id="e50c5-104">Gestore oggetti</span><span class="sxs-lookup"><span data-stu-id="e50c5-104">Object Manager</span></span>

<span data-ttu-id="e50c5-105">Un oggetto è costituito da un'intestazione standard e da attributi specifici dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e50c5-105">An object consists of a standard header and object-specific attributes.</span></span> <span data-ttu-id="e50c5-106">Poiché tutti gli oggetti hanno la stessa struttura, in Windows è disponibile un singolo gestore di oggetti che gestisce tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="e50c5-106">Because all objects have the same structure, there is a single object manager in Windows that maintains all objects.</span></span>

<span data-ttu-id="e50c5-107">L'intestazione dell'oggetto include elementi come il nome dell'oggetto, in modo che altri processi possano fare riferimento all'oggetto in base al nome e a un descrittore di sicurezza, in modo che il gestore di oggetti possa controllare i processi che accedono alla risorsa di sistema.</span><span class="sxs-lookup"><span data-stu-id="e50c5-107">The object header includes items such as the object name, so that other processes can reference the object by name, and a security descriptor, so that the object manager can control which processes access the system resource.</span></span>

<span data-ttu-id="e50c5-108">Le attività eseguite dal gestore di oggetti includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e50c5-108">The tasks that the object manager performs include the following:</span></span>

-   <span data-ttu-id="e50c5-109">Creazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="e50c5-109">Creating objects</span></span>
-   <span data-ttu-id="e50c5-110">Verifica per verificare se un processo ha il diritto di usare l'oggetto</span><span class="sxs-lookup"><span data-stu-id="e50c5-110">Verifying that a process has the right to use the object</span></span>
-   <span data-ttu-id="e50c5-111">Creazione di handle di oggetto e relativa restituzione al chiamante</span><span class="sxs-lookup"><span data-stu-id="e50c5-111">Creating object handles and returning them to the caller</span></span>
-   <span data-ttu-id="e50c5-112">Gestione delle quote delle risorse</span><span class="sxs-lookup"><span data-stu-id="e50c5-112">Maintaining resource quotas</span></span>
-   <span data-ttu-id="e50c5-113">Creazione di handle duplicati</span><span class="sxs-lookup"><span data-stu-id="e50c5-113">Creating duplicate handles</span></span>
-   <span data-ttu-id="e50c5-114">Chiusura di handle per gli oggetti</span><span class="sxs-lookup"><span data-stu-id="e50c5-114">Closing handles to objects</span></span>

 

 



