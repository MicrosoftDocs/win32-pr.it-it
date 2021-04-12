---
description: WMI controlla i diritti di accesso per le applicazioni e gli script.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Costanti di sicurezza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233669"
---
# <a name="wmi-security-constants"></a><span data-ttu-id="93568-103">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="93568-103">WMI Security Constants</span></span>

<span data-ttu-id="93568-104">WMI verifica i diritti di accesso per le applicazioni e gli script per oggetti quali gli spazi dei nomi WMI, le stampanti, i servizi, le applicazioni DCOM, i file, le condivisioni e altri oggetti a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="93568-104">WMI checks access rights for applications and scripts for objects such as WMI namespaces, printer, services, DCOM applications, files, shares, and other securable objects.</span></span> <span data-ttu-id="93568-105">L'accesso a tali oggetti a protezione diretta è controllato dalle voci di controllo di accesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="93568-105">Access to theses securable objects is controlled by access control entries (ACE).</span></span> <span data-ttu-id="93568-106">Ogni voce ACE contiene elenchi che definiscono i gruppi o gli utenti che hanno accesso.</span><span class="sxs-lookup"><span data-stu-id="93568-106">Each ACE contains lists that designate which groups or users have access.</span></span> <span data-ttu-id="93568-107">Per ulteriori informazioni sugli elenchi di controllo di accesso e sicurezza (ACL, elenchi DACL o SACL), vedere [elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="93568-107">For more information about security and access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

<span data-ttu-id="93568-108">Molti metodi del provider in WMI che interessano gli oggetti a protezione diretta richiedono che l'amministratore abiliti determinati privilegi.</span><span class="sxs-lookup"><span data-stu-id="93568-108">Many provider methods in WMI that affect securable objects require the administrator to enable certain privileges.</span></span> <span data-ttu-id="93568-109">La versione del privilegio da usare dipende dal linguaggio di programmazione, come illustrato in [**costanti Privilege**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="93568-109">Which version of the privilege you use depends on the programming language, as shown in [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="93568-110">Le costanti di sicurezza sono definite negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="93568-110">The security constants are defined in the following topics:</span></span>

-   [<span data-ttu-id="93568-111">**Costanti di sicurezza degli eventi**</span><span class="sxs-lookup"><span data-stu-id="93568-111">**Event Security Constants**</span></span>](event-security-constants.md)
-   [<span data-ttu-id="93568-112">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="93568-112">**File and Directory Access Rights Constants**</span></span>](file-and-directory-access-rights-constants.md)
-   [<span data-ttu-id="93568-113">**Costanti dei diritti di accesso allo spazio dei nomi**</span><span class="sxs-lookup"><span data-stu-id="93568-113">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
-   [<span data-ttu-id="93568-114">**Costanti del flag ACE dello spazio dei nomi**</span><span class="sxs-lookup"><span data-stu-id="93568-114">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
-   [<span data-ttu-id="93568-115">**Costanti di tipo ACE dello spazio dei nomi**</span><span class="sxs-lookup"><span data-stu-id="93568-115">**Namespace ACE Type Constants**</span></span>](namespace-ace-type-constants.md)
-   [<span data-ttu-id="93568-116">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="93568-116">**Privilege Constants**</span></span>](privilege-constants.md)

 

 
