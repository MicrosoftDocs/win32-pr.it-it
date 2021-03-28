---
description: Se un computer esegue Windows 2000 Server o versione successiva in una rete, gli utenti possono archiviare i profili sul server. Questi profili sono detti profili utente mobili.
title: Profili utente mobili
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979938"
---
# <a name="roaming-user-profiles"></a><span data-ttu-id="214bf-104">Profili utente mobili</span><span class="sxs-lookup"><span data-stu-id="214bf-104">Roaming User Profiles</span></span>

<span data-ttu-id="214bf-105">Se un computer esegue Windows 2000 Server o versione successiva in una rete, gli utenti possono archiviare i profili sul server.</span><span class="sxs-lookup"><span data-stu-id="214bf-105">If a computer is running Windows 2000 Server or later on a network, users can store their profiles on the server.</span></span> <span data-ttu-id="214bf-106">Questi profili sono detti *profili utente mobili*.</span><span class="sxs-lookup"><span data-stu-id="214bf-106">These profiles are called *roaming user profiles*.</span></span>

<span data-ttu-id="214bf-107">I profili utente mobili presentano i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="214bf-107">Roaming user profiles have the following advantages:</span></span>

-   <span data-ttu-id="214bf-108">Disponibilità automatica delle risorse.</span><span class="sxs-lookup"><span data-stu-id="214bf-108">Automatic resource availability.</span></span> <span data-ttu-id="214bf-109">Il profilo univoco di un utente è automaticamente disponibile quando accede a un computer in rete.</span><span class="sxs-lookup"><span data-stu-id="214bf-109">A user's unique profile is automatically available when he or she logs on to any computer on the network.</span></span> <span data-ttu-id="214bf-110">Non è necessario che gli utenti creino un profilo in ogni computer utilizzato in una rete.</span><span class="sxs-lookup"><span data-stu-id="214bf-110">Users do not need to create a profile on each computer they use on a network.</span></span>
-   <span data-ttu-id="214bf-111">Sostituzione e backup semplificati del computer.</span><span class="sxs-lookup"><span data-stu-id="214bf-111">Simplified computer replacement and backup.</span></span> <span data-ttu-id="214bf-112">Quando il computer di un utente deve essere sostituito, può essere sostituito facilmente perché tutte le informazioni sul profilo dell'utente sono gestite separatamente nella rete, indipendentemente da un singolo computer.</span><span class="sxs-lookup"><span data-stu-id="214bf-112">When a user's computer must be replaced, it can be replaced easily because all of the user's profile information is maintained separately on the network, independent of an individual computer.</span></span> <span data-ttu-id="214bf-113">Quando l'utente accede al nuovo computer per la prima volta, la copia server del profilo dell'utente viene copiata nel nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="214bf-113">When the user logs on to the new computer for the first time, the server copy of the user's profile is copied to the new computer.</span></span>

<span data-ttu-id="214bf-114">Il profilo dell'utente non viene caricato automaticamente quando l'utente è connesso tramite la funzione [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="214bf-114">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="214bf-115">Per caricare un profilo utente mobile a livello di codice, usare la funzione [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="214bf-115">To load a roaming user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="214bf-116">Per scaricare un profilo utente mobile caricato da **LoadUserProfile**, chiamare la funzione [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="214bf-116">To unload a roaming user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
