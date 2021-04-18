---
description: Le funzioni dei file di rete consentono di monitorare e chiudere le risorse di file, dispositivi e pipe aperte in un server. Le funzioni file sono elencate di seguito.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Funzioni NetFile (gestione delle condivisioni di rete)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df51d556647f16cc30ec51182fde5dd5551831d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317099"
---
# <a name="netfile-functions-network-share-management"></a><span data-ttu-id="0b596-104">Funzioni NetFile (gestione delle condivisioni di rete)</span><span class="sxs-lookup"><span data-stu-id="0b596-104">NetFile Functions (Network Share Management)</span></span>

<span data-ttu-id="0b596-105">Le funzioni dei file di rete consentono di monitorare e chiudere le risorse di file, dispositivi e pipe aperte in un server.</span><span class="sxs-lookup"><span data-stu-id="0b596-105">The network file functions provide a way to monitor and close the file, device, and pipe resources open on a server.</span></span> <span data-ttu-id="0b596-106">Le funzioni file sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="0b596-106">The file functions are listed following.</span></span>



| <span data-ttu-id="0b596-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="0b596-107">Function</span></span>                                 | <span data-ttu-id="0b596-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b596-108">Description</span></span>                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="0b596-109">**NetFileClose**</span><span class="sxs-lookup"><span data-stu-id="0b596-109">**NetFileClose**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | <span data-ttu-id="0b596-110">Impone la chiusura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="0b596-110">Forces a resource to close.</span></span>                                          |
| [<span data-ttu-id="0b596-111">**NetFileEnum**</span><span class="sxs-lookup"><span data-stu-id="0b596-111">**NetFileEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | <span data-ttu-id="0b596-112">Restituisce informazioni sui file aperti in un server.</span><span class="sxs-lookup"><span data-stu-id="0b596-112">Returns information about open files on a server.</span></span>                    |
| [<span data-ttu-id="0b596-113">**NetFileGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0b596-113">**NetFileGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | <span data-ttu-id="0b596-114">Restituisce informazioni su una particolare apertura di una risorsa server.</span><span class="sxs-lookup"><span data-stu-id="0b596-114">Returns information about a particular opening of a server resource.</span></span> |



 

<span data-ttu-id="0b596-115">Chiamare la funzione [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) quando il file non può essere chiuso con altri mezzi.</span><span class="sxs-lookup"><span data-stu-id="0b596-115">Call the [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) function when the file cannot be closed by any other means.</span></span> <span data-ttu-id="0b596-116">Questa funzione deve essere usata con cautela perché **NetFileClose** non scrive i dati memorizzati nella cache del sistema client nel file prima di chiudere il file.</span><span class="sxs-lookup"><span data-stu-id="0b596-116">This function should be used with caution because **NetFileClose** does not write data cached on the client system to the file before closing the file.</span></span>

<span data-ttu-id="0b596-117">La funzione [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) restituisce informazioni sulle risorse aperte in un server.</span><span class="sxs-lookup"><span data-stu-id="0b596-117">The [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) function returns information about resources open on a server.</span></span> <span data-ttu-id="0b596-118">Un file può essere aperto una o più volte da una o più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0b596-118">A file can be opened one or more times by one or more applications.</span></span> <span data-ttu-id="0b596-119">Ogni apertura di file viene identificata in modo univoco.</span><span class="sxs-lookup"><span data-stu-id="0b596-119">Each file opening is uniquely identified.</span></span> <span data-ttu-id="0b596-120">La funzione **NetFileEnum** restituisce una voce per ogni apertura del file.</span><span class="sxs-lookup"><span data-stu-id="0b596-120">The **NetFileEnum** function returns an entry for each file opening.</span></span> <span data-ttu-id="0b596-121">La funzione [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) restituisce informazioni su un'apertura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="0b596-121">The [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) function returns information about one opening of a resource.</span></span>

<span data-ttu-id="0b596-122">Le informazioni sui file sono disponibili ai livelli seguenti.</span><span class="sxs-lookup"><span data-stu-id="0b596-122">File information is available at the following levels.</span></span>

<dl>

[<span data-ttu-id="0b596-123">**Informazioni sul FILE \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0b596-123">**FILE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[<span data-ttu-id="0b596-124">**Informazioni sul FILE \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="0b596-124">**FILE\_INFO\_3**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

<span data-ttu-id="0b596-125">I livelli 0 e 1 non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="0b596-125">Levels 0 and 1 are not supported.</span></span> <span data-ttu-id="0b596-126">Il livello 2 restituisce solo il numero di identificazione assegnato alla risorsa quando è stato aperto.</span><span class="sxs-lookup"><span data-stu-id="0b596-126">Level 2 returns only the identification number assigned to the resource when it was opened.</span></span> <span data-ttu-id="0b596-127">Il livello 3 restituisce il numero di identificazione, le autorizzazioni, i blocchi di file e il nome dell'utente che ha aperto la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0b596-127">Level 3 returns the identification number, permissions, file locks, and the name of the user who opened the resource.</span></span>

<span data-ttu-id="0b596-128">Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) e [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) .</span><span class="sxs-lookup"><span data-stu-id="0b596-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) and [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) functions.</span></span> <span data-ttu-id="0b596-129">Per ulteriori informazioni, vedere [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="0b596-129">For more information, see [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
