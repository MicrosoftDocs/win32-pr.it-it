---
description: Così come il sistema usa i descrittori di sicurezza per controllare l'accesso agli oggetti a protezione diretta, un server può usare i descrittori di sicurezza per controllare l'accesso ai relativi oggetti privati. Per altre informazioni sul modello di sicurezza di Windows, vedere modello di controllo di accesso.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Controllo degli accessi basato su ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756183"
---
# <a name="acl-based-access-control"></a><span data-ttu-id="9963f-104">Controllo degli accessi basato su ACL</span><span class="sxs-lookup"><span data-stu-id="9963f-104">ACL-based Access Control</span></span>

<span data-ttu-id="9963f-105">Così come il sistema usa i [descrittori di sicurezza](security-descriptors.md) per controllare l'accesso agli oggetti a protezione diretta, un server può usare i descrittori di sicurezza per controllare l'accesso ai relativi oggetti privati.</span><span class="sxs-lookup"><span data-stu-id="9963f-105">Just as the system uses [security descriptors](security-descriptors.md) to control access to securable objects, a server can use security descriptors to control access to its private objects.</span></span> <span data-ttu-id="9963f-106">Per altre informazioni sul modello di sicurezza di Windows, vedere [modello di controllo di accesso](access-control-model.md).</span><span class="sxs-lookup"><span data-stu-id="9963f-106">For more information about the Windows security model, see [Access Control Model](access-control-model.md).</span></span>

<span data-ttu-id="9963f-107">Un server protetto può [creare un descrittore di sicurezza](security-descriptors-for-private-objects.md) con un DACL che specifica i tipi di accesso consentiti per diversi [trustee](trustees.md).</span><span class="sxs-lookup"><span data-stu-id="9963f-107">A protected server can [create a security descriptor](security-descriptors-for-private-objects.md) with a DACL that specifies the types of access allowed for various [trustees](trustees.md).</span></span> <span data-ttu-id="9963f-108">In un caso semplice, il server potrebbe creare un singolo descrittore di sicurezza per [controllare l'accesso a tutti i dati e le funzionalità del server](checking-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9963f-108">In a simple case, the server could create a single security descriptor to [control access to all of the server's data and functionality](checking-access-to-private-objects.md).</span></span> <span data-ttu-id="9963f-109">Per una maggiore granularità della protezione, il server può creare descrittori di sicurezza per ognuno dei relativi oggetti privati o per diversi tipi di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="9963f-109">For a finer granularity of protection, the server could create security descriptors for each of its private objects, or for different types of functionality.</span></span>

<span data-ttu-id="9963f-110">Ad esempio, quando un client richiede al server di creare un nuovo oggetto in un database, il server potrebbe creare un descrittore di sicurezza per il nuovo oggetto privato.</span><span class="sxs-lookup"><span data-stu-id="9963f-110">For example, when a client asks the server to create a new object in a database, the server could create a security descriptor for the new private object.</span></span> <span data-ttu-id="9963f-111">Il server potrebbe quindi archiviare il descrittore di sicurezza con l'oggetto privato nel database.</span><span class="sxs-lookup"><span data-stu-id="9963f-111">The server could then store the security descriptor with the private object in the database.</span></span> <span data-ttu-id="9963f-112">Quando un client tenta di accedere all'oggetto, il server recupera il descrittore di sicurezza per verificare i diritti di accesso del client.</span><span class="sxs-lookup"><span data-stu-id="9963f-112">When a client tries to access the object, the server retrieves the security descriptor to check the client's access rights.</span></span> <span data-ttu-id="9963f-113">È importante notare che non c'è nulla in un descrittore di sicurezza che lo associa all'oggetto o alla funzionalità da proteggere.</span><span class="sxs-lookup"><span data-stu-id="9963f-113">It is important to note that there is nothing in a security descriptor that associates it with the object or functionality it is protecting.</span></span> <span data-ttu-id="9963f-114">Al contrario, spetta al server protetto mantenere l'associazione.</span><span class="sxs-lookup"><span data-stu-id="9963f-114">Instead, it is up to the protected server to maintain the association.</span></span>

<span data-ttu-id="9963f-115">È anche possibile controllare l'accesso all'oggetto privato.</span><span class="sxs-lookup"><span data-stu-id="9963f-115">Access to the private object can also be audited.</span></span> <span data-ttu-id="9963f-116">Per una descrizione di questo articolo, vedere [controllo dell'accesso a oggetti privati](auditing-access-to-private-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="9963f-116">Refer to [Auditing Access to Private Objects](auditing-access-to-private-objects.md) for a description of this.</span></span>

 

 



