---
description: In un controllo di accesso, il sistema confronta le informazioni di sicurezza nel token di accesso dei thread con le informazioni di sicurezza nel descrittore di sicurezza degli oggetti.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interazione tra thread e oggetti a protezione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884453"
---
# <a name="interaction-between-threads-and-securable-objects"></a><span data-ttu-id="567c1-103">Interazione tra thread e oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="567c1-103">Interaction Between Threads and Securable Objects</span></span>

<span data-ttu-id="567c1-104">Quando un thread tenta di utilizzare un [oggetto a protezione diretta](securable-objects.md), il sistema esegue un controllo di accesso prima di consentire al thread di proseguire.</span><span class="sxs-lookup"><span data-stu-id="567c1-104">When a thread attempts to use a [securable object](securable-objects.md), the system performs an access check before allowing the thread to proceed.</span></span> <span data-ttu-id="567c1-105">In un controllo di accesso, il sistema confronta le informazioni di sicurezza nel token di [*accesso*](/windows/desktop/SecGloss/a-gly) del thread con le informazioni di sicurezza nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="567c1-105">In an access check, the system compares the security information in the thread's [*access token*](/windows/desktop/SecGloss/a-gly) against the security information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

-   <span data-ttu-id="567c1-106">Il token di accesso contiene gli [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) che identificano l'utente associato al thread.</span><span class="sxs-lookup"><span data-stu-id="567c1-106">The access token contains [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that identify the user associated with the thread.</span></span>
-   <span data-ttu-id="567c1-107">Il descrittore di sicurezza identifica il proprietario dell'oggetto e contiene un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL).</span><span class="sxs-lookup"><span data-stu-id="567c1-107">The security descriptor identifies the object's owner and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL).</span></span> <span data-ttu-id="567c1-108">Il DACL contiene le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE), ognuna delle quali specifica i diritti di accesso consentiti o negati a un utente o a un gruppo specifico.</span><span class="sxs-lookup"><span data-stu-id="567c1-108">The DACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), each of which specify the access rights allowed or denied to a specific user or group.</span></span>

<span data-ttu-id="567c1-109">Il sistema controlla l'elenco DACL dell'oggetto, cercando le voci ACE che si applicano ai SID utente e gruppo dal token di accesso del thread.</span><span class="sxs-lookup"><span data-stu-id="567c1-109">The system checks the object's DACL, looking for ACEs that apply to the user and group SIDs from the thread's access token.</span></span> <span data-ttu-id="567c1-110">Il sistema controlla ogni voce ACE fino a quando l'accesso non viene concesso o negato o fino a quando non sono presenti altre voci ACE da verificare.</span><span class="sxs-lookup"><span data-stu-id="567c1-110">The system checks each ACE until access is either granted or denied or until there are no more ACEs to check.</span></span> <span data-ttu-id="567c1-111">In teoria, un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) potrebbe avere diverse voci ACE applicabili ai SID del token.</span><span class="sxs-lookup"><span data-stu-id="567c1-111">Conceivably, an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) could have several ACEs that apply to the token's SIDs.</span></span> <span data-ttu-id="567c1-112">E, in questo caso, i diritti di accesso concessi da ogni ACE si accumulano.</span><span class="sxs-lookup"><span data-stu-id="567c1-112">And, if this occurs, the access rights granted by each ACE accumulate.</span></span> <span data-ttu-id="567c1-113">Se ad esempio una voce ACE concede l'accesso in lettura a un gruppo e un'altra voce ACE concede l'accesso in scrittura a un utente che è membro del gruppo, l'utente può disporre di accesso in lettura e scrittura all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="567c1-113">For example, if one ACE grants read access to a group and another ACE grants write access to a user who is a member of the group, the user can have both read and write access to the object.</span></span>

<span data-ttu-id="567c1-114">Nella figura seguente viene illustrata la relazione tra questi blocchi di informazioni di sicurezza:</span><span class="sxs-lookup"><span data-stu-id="567c1-114">The following illustration shows the relationship between these blocks of security information:</span></span>

![relazioni tra processi, ACE e DACL](images/cssec-02.png)

 

 
