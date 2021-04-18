---
description: I requisiti di sicurezza a livello C2 specificano che gli amministratori di sistema devono essere in grado di controllare gli eventi correlati alla sicurezza e che l'accesso a questi dati di controllo deve essere limitato agli amministratori autorizzati.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Generazione di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318254"
---
# <a name="audit-generation"></a><span data-ttu-id="d6579-103">Generazione di controllo</span><span class="sxs-lookup"><span data-stu-id="d6579-103">Audit Generation</span></span>

<span data-ttu-id="d6579-104">I requisiti di sicurezza a livello C2 specificano che gli amministratori di sistema devono essere in grado di controllare gli eventi correlati alla sicurezza e che l'accesso a questi dati di controllo deve essere limitato agli amministratori autorizzati.</span><span class="sxs-lookup"><span data-stu-id="d6579-104">C2-level security requirements specify that system administrators must be able to audit security-related events and that access to this audit data must be limited to authorized administrators.</span></span> <span data-ttu-id="d6579-105">L'API Windows fornisce funzioni che consentono a un amministratore di monitorare gli eventi correlati alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d6579-105">The Windows API provides functions enabling an administrator to monitor security-related events.</span></span>

<span data-ttu-id="d6579-106">Il descrittore di sicurezza per un oggetto a protezione diretta può avere un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="d6579-106">The security descriptor for a securable object can have a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="d6579-107">Un SACL contiene [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) che specificano i tipi di tentativi di accesso che generano report di controllo.</span><span class="sxs-lookup"><span data-stu-id="d6579-107">A SACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) that specify the types of access attempts that generate audit reports.</span></span> <span data-ttu-id="d6579-108">Ogni voce ACE identifica un trustee, un set di diritti di accesso e un set di flag che indicano se il sistema genera messaggi di controllo per tentativi di accesso non riusciti, tentativi di accesso riusciti o entrambi.</span><span class="sxs-lookup"><span data-stu-id="d6579-108">Each ACE identifies a trustee, a set of access rights, and a set of flags that indicate whether the system generates audit messages for failed access attempts, successful access attempts, or both.</span></span>

<span data-ttu-id="d6579-109">Il sistema scrive i messaggi di controllo nel registro eventi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d6579-109">The system writes audit messages to the security event log.</span></span> <span data-ttu-id="d6579-110">Per informazioni sull'accesso ai record in un registro eventi di protezione, vedere [registrazione degli eventi](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="d6579-110">For information about accessing the records in a security event log, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

<span data-ttu-id="d6579-111">Per leggere o scrivere il SACL di un oggetto, un thread deve prima abilitare il \_ \_ privilegio se nome sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d6579-111">To read or write an object's SACL, a thread must first enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="d6579-112">Per ulteriori informazioni, vedere il [diritto di accesso SACL](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="d6579-112">For more information, see [SACL Access Right](sacl-access-right.md).</span></span>

<span data-ttu-id="d6579-113">L'API Windows fornisce inoltre supporto per le applicazioni server per generare messaggi di controllo quando un client tenta di accedere a un oggetto privato.</span><span class="sxs-lookup"><span data-stu-id="d6579-113">The Windows API also provides support for server applications to generate audit messages when a client tries to access a private object.</span></span> <span data-ttu-id="d6579-114">Per altre informazioni, vedere [controllo dell'accesso a oggetti privati](auditing-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d6579-114">For more information, see [Auditing Access To Private Objects](auditing-access-to-private-objects.md).</span></span>

 

 
