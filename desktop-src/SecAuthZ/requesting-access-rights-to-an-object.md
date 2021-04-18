---
description: Quando si apre un handle per un oggetto, l'handle restituito dispone di una combinazione di diritti di accesso all'oggetto.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Richiesta di diritti di accesso a un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308144"
---
# <a name="requesting-access-rights-to-an-object"></a><span data-ttu-id="392ee-103">Richiesta di diritti di accesso a un oggetto</span><span class="sxs-lookup"><span data-stu-id="392ee-103">Requesting Access Rights to an Object</span></span>

<span data-ttu-id="392ee-104">Quando si apre un handle per un oggetto, l'handle restituito dispone di una combinazione di diritti di accesso all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="392ee-104">When you open a handle to an object, the returned handle has some combination of access rights to the object.</span></span> <span data-ttu-id="392ee-105">Alcune funzioni, ad esempio [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), non richiedono un set specifico di diritti di accesso richiesti.</span><span class="sxs-lookup"><span data-stu-id="392ee-105">Some functions, such as [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), do not require a specific set of requested access rights.</span></span> <span data-ttu-id="392ee-106">Queste funzioni tentano sempre di aprire l'handle per l'accesso completo.</span><span class="sxs-lookup"><span data-stu-id="392ee-106">These functions always try to open the handle for full access.</span></span> <span data-ttu-id="392ee-107">Altre funzioni, ad esempio [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), consentono di specificare il set di diritti di accesso desiderato.</span><span class="sxs-lookup"><span data-stu-id="392ee-107">Other functions, such as [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), allow you to specify the set of access rights that you want.</span></span> <span data-ttu-id="392ee-108">È necessario richiedere solo i diritti di accesso necessari, anziché aprire un handle per l'accesso completo.</span><span class="sxs-lookup"><span data-stu-id="392ee-108">You should request only the access rights that you need, rather than opening a handle for full access.</span></span> <span data-ttu-id="392ee-109">In questo modo si impedisce l'utilizzo dell'handle in modo indesiderato e aumentano le probabilità che la richiesta di accesso abbia esito positivo se l'elenco DACL dell'oggetto consente l'accesso limitato.</span><span class="sxs-lookup"><span data-stu-id="392ee-109">This prevents using the handle in an unintended way, and increases the chances that the access request will succeed if the object's DACL only allows limited access.</span></span>

<span data-ttu-id="392ee-110">Usare [i diritti di accesso generici](generic-access-rights.md) per specificare il tipo di accesso necessario quando si apre un handle a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="392ee-110">Use [generic access rights](generic-access-rights.md) to specify the type of access needed when opening a handle to an object.</span></span> <span data-ttu-id="392ee-111">Questa operazione è in genere più semplice rispetto a specificare tutti i diritti standard e specifici corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="392ee-111">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span> <span data-ttu-id="392ee-112">In alternativa, utilizzare la \_ costante massima consentita per richiedere che l'oggetto venga aperto con tutti i diritti di accesso validi per il chiamante.</span><span class="sxs-lookup"><span data-stu-id="392ee-112">Alternatively, use the MAXIMUM\_ALLOWED constant to request that the object be opened with all the access rights that are valid for the caller.</span></span>

> [!Note]  
> <span data-ttu-id="392ee-113">\_Impossibile utilizzare la costante massima consentita in una voce ACE.</span><span class="sxs-lookup"><span data-stu-id="392ee-113">The MAXIMUM\_ALLOWED constant cannot be used in an ACE.</span></span>

 

<span data-ttu-id="392ee-114">Per ottenere o impostare l'elenco SACL nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)di un oggetto, richiedere il [diritto di accesso alla \_ \_ sicurezza del sistema di accesso](sacl-access-right.md) quando si apre un handle per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="392ee-114">To get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), request the [ACCESS\_SYSTEM\_SECURITY access right](sacl-access-right.md) when opening a handle to the object.</span></span>

 

 
