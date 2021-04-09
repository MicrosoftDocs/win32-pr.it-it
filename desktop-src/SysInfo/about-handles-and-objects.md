---
description: Il sistema utilizza oggetti e handle per regolare l'accesso alle risorse di sistema per due motivi principali.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Informazioni sugli handle e sugli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967605"
---
# <a name="about-handles-and-objects"></a><span data-ttu-id="7b390-103">Informazioni sugli handle e sugli oggetti</span><span class="sxs-lookup"><span data-stu-id="7b390-103">About Handles and Objects</span></span>

<span data-ttu-id="7b390-104">Il sistema utilizza oggetti e handle per regolare l'accesso alle risorse di sistema per due motivi principali.</span><span class="sxs-lookup"><span data-stu-id="7b390-104">The system uses objects and handles to regulate access to system resources for two main reasons.</span></span> <span data-ttu-id="7b390-105">In primo luogo, l'utilizzo di oggetti garantisce che Microsoft possa aggiornare la funzionalità di sistema, purché venga mantenuta l'interfaccia dell'oggetto originale.</span><span class="sxs-lookup"><span data-stu-id="7b390-105">First, the use of objects ensures that Microsoft can update system functionality, as long as the original object interface is maintained.</span></span> <span data-ttu-id="7b390-106">Quando vengono rilasciate le versioni successive del sistema, è possibile utilizzare l'oggetto aggiornato con un numero di lavoro aggiuntivo o minimo.</span><span class="sxs-lookup"><span data-stu-id="7b390-106">When subsequent versions of the system are released, you can use the updated object with little or no additional work.</span></span>

<span data-ttu-id="7b390-107">In secondo luogo, l'utilizzo di oggetti consente di sfruttare la sicurezza di Windows.</span><span class="sxs-lookup"><span data-stu-id="7b390-107">Secondly, the use of objects enables you to take advantage of Windows security.</span></span> <span data-ttu-id="7b390-108">Ogni oggetto dispone di un proprio elenco di controllo di accesso (ACL) che specifica le azioni che possono essere eseguite da un processo sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b390-108">Each object has its own access-control list (ACL) that specifies the actions a process can perform on the object.</span></span> <span data-ttu-id="7b390-109">Il sistema esamina l'elenco di controllo di accesso di un oggetto ogni volta che un'applicazione crea un handle per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b390-109">The system examines an object's ACL each time an application creates a handle to the object.</span></span> <span data-ttu-id="7b390-110">Per altre informazioni, vedere [Controllo di accesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="7b390-110">For more information, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

-   [<span data-ttu-id="7b390-111">Gestore oggetti</span><span class="sxs-lookup"><span data-stu-id="7b390-111">Object Manager</span></span>](object-manager.md)
-   [<span data-ttu-id="7b390-112">Interfaccia oggetto</span><span class="sxs-lookup"><span data-stu-id="7b390-112">Object Interface</span></span>](object-interface.md)
-   [<span data-ttu-id="7b390-113">Spazi dei nomi degli oggetti</span><span class="sxs-lookup"><span data-stu-id="7b390-113">Object Namespaces</span></span>](/windows/desktop/Sync/object-namespaces)
-   [<span data-ttu-id="7b390-114">Limitazioni della gestione</span><span class="sxs-lookup"><span data-stu-id="7b390-114">Handle Limitations</span></span>](handle-limitations.md)
-   [<span data-ttu-id="7b390-115">Gestisci ereditarietà</span><span class="sxs-lookup"><span data-stu-id="7b390-115">Handle Inheritance</span></span>](handle-inheritance.md)

 

 
