---
description: WMI si basa su descrittori di sicurezza standard di Windows per controllare e proteggere l'accesso a oggetti a protezione diretta come gli spazi dei nomi WMI, le stampanti, i servizi e le applicazioni DCOM.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Accesso a oggetti a protezione diretta WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233476"
---
# <a name="access-to-wmi-securable-objects"></a><span data-ttu-id="bd253-103">Accesso a oggetti a protezione diretta WMI</span><span class="sxs-lookup"><span data-stu-id="bd253-103">Access to WMI Securable Objects</span></span>

<span data-ttu-id="bd253-104">WMI si basa su [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly) standard di Windows per controllare e proteggere l'accesso a oggetti a protezione diretta come gli spazi dei nomi WMI, le stampanti, i servizi e le applicazioni DCOM.</span><span class="sxs-lookup"><span data-stu-id="bd253-104">WMI relies on standard Windows [*security descriptors*](/windows/desktop/SecGloss/s-gly) to control and protect access to securable objects like WMI namespaces, printers, services, and DCOM applications.</span></span> <span data-ttu-id="bd253-105">Per ulteriori informazioni, vedere [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="bd253-105">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="bd253-106">In questa sezione vengono trattati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd253-106">The following topics are discussed in this section:</span></span>

-   [<span data-ttu-id="bd253-107">Descrittori di sicurezza e SID</span><span class="sxs-lookup"><span data-stu-id="bd253-107">Security Descriptors and SIDs</span></span>](#security-descriptors-and-sids)
-   [<span data-ttu-id="bd253-108">Controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="bd253-108">Access Control</span></span>](#access-control)
-   [<span data-ttu-id="bd253-109">Modifica della sicurezza dell'accesso</span><span class="sxs-lookup"><span data-stu-id="bd253-109">Changing Access Security</span></span>](#changing-access-security)
-   [<span data-ttu-id="bd253-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd253-110">Related topics</span></span>](#related-topics)

## <a name="security-descriptors-and-sids"></a><span data-ttu-id="bd253-111">Descrittori di sicurezza e SID</span><span class="sxs-lookup"><span data-stu-id="bd253-111">Security Descriptors and SIDs</span></span>

<span data-ttu-id="bd253-112">WMI mantiene la sicurezza dell'accesso confrontando il [*token di accesso*](/windows/desktop/SecGloss/a-gly) dell'utente che tenta di accedere a un oggetto a protezione diretta con il descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bd253-112">WMI maintains access security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user that attempts to access a securable object with the security descriptor of the object.</span></span>

<span data-ttu-id="bd253-113">Quando un utente o un gruppo viene creato in un sistema, all'account viene assegnato un [*ID di sicurezza (SID)*](/windows/desktop/SecGloss/s-gly) . il SID garantisce che un account creato con lo stesso nome di un account eliminato in precedenza non erediti le impostazioni di sicurezza precedenti.</span><span class="sxs-lookup"><span data-stu-id="bd253-113">When a user or group is created on a system, the account is given a [*security identifier (SID)*](/windows/desktop/SecGloss/s-gly) The SID ensures that an account created with the same name as a previously deleted account does not inherit the previous security settings.</span></span> <span data-ttu-id="bd253-114">Un token di accesso viene creato combinando il SID, l'elenco dei gruppi di cui l'utente è membro e l'elenco dei privilegi abilitati o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="bd253-114">An access token is created by combining the SID, the list of groups of which the user is a member, and the list of enabled or disabled privileges.</span></span> <span data-ttu-id="bd253-115">Questi token vengono assegnati a tutti i processi e i thread di proprietà dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bd253-115">These tokens are assigned to all processes and threads owned by the user.</span></span>

## <a name="access-control"></a><span data-ttu-id="bd253-116">Controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="bd253-116">Access Control</span></span>

<span data-ttu-id="bd253-117">Quando l'utente desidera utilizzare un oggetto protetto, il token di accesso viene confrontato con l' [*elenco di controllo di accesso discrezionale (DACL)*](/windows/desktop/SecGloss/d-gly) nel descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bd253-117">When the user wants to use a secured object, the access token is compared with the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) in the security descriptor on the object.</span></span> <span data-ttu-id="bd253-118">L'elenco DACL contiene autorizzazioni denominate [*ACE (Access Control Entry)*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="bd253-118">The DACL contains permissions called [*access control entries (ACE)*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="bd253-119">Gli [*elenchi di controllo di accesso di sistema (SACL)*](/windows/desktop/SecGloss/s-gly) eseguono la stessa operazione degli elenchi DACL, ma possono generare eventi di controllo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bd253-119">[*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) do the same thing as DACLs, but can generate security audit events.</span></span> <span data-ttu-id="bd253-120">A partire da Windows Vista, WMI può creare voci di controllo nel registro di sicurezza di Windows.</span><span class="sxs-lookup"><span data-stu-id="bd253-120">Starting with Windows Vista, WMI can make auditing entries in the Windows Security Log.</span></span> <span data-ttu-id="bd253-121">Per ulteriori informazioni sul controllo in WMI, vedere [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="bd253-121">For more information about auditing in WMI, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="bd253-122">Sia il DACL che il SACL sono costituiti da un elenco di voci ACE che descrivono quali utenti dispongono di diritti di accesso specifici, inclusa la scrittura nel repository WMI, l'accesso remoto e l'esecuzione e le autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="bd253-122">Both the DACL and the SACL consist of a list of ACEs that describe which users have specific access rights, including writing to the WMI repository, remote access and execution, and logon permissions.</span></span> <span data-ttu-id="bd253-123">WMI archivia questi ACL nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="bd253-123">WMI stores these ACLs in the WMI repository.</span></span>

<span data-ttu-id="bd253-124">Le voci ACE contengono tre tipi di livelli di accesso o diritti Concedi/nega: Consenti, nega per DACL e controllo di sistema (per SACL).</span><span class="sxs-lookup"><span data-stu-id="bd253-124">ACEs hold three types of access levels or grant/deny rights: allow, deny for DACL, and system audit (for SACLs).</span></span> <span data-ttu-id="bd253-125">Le voci ACE Deny precedono le voci ACE nell'elenco DACL o SACL.</span><span class="sxs-lookup"><span data-stu-id="bd253-125">Deny ACEs precede allow ACEs in the DACL or SACL.</span></span> <span data-ttu-id="bd253-126">Quando si controllano i diritti di accesso dell'utente, WMI viene eseguito consecutivamente attraverso l'elenco di controllo di accesso fino a quando non viene trovata una voce ACE Allow applicabile al token di accesso richiedente.</span><span class="sxs-lookup"><span data-stu-id="bd253-126">When checking the user access rights, WMI runs consecutively through the access control list until it finds an allow ACE that applies to the requesting access token.</span></span> <span data-ttu-id="bd253-127">Le voci ACE rimanenti non vengono controllate dopo questo punto.</span><span class="sxs-lookup"><span data-stu-id="bd253-127">The remaining ACEs are not checked after this point.</span></span> <span data-ttu-id="bd253-128">Se non viene trovata alcuna voce ACE appropriata, l'accesso viene negato.</span><span class="sxs-lookup"><span data-stu-id="bd253-128">If no appropriate allow ACE is found, then access is denied.</span></span> <span data-ttu-id="bd253-129">Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) e [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="bd253-129">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) and [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

## <a name="changing-access-security"></a><span data-ttu-id="bd253-130">Modifica della sicurezza dell'accesso</span><span class="sxs-lookup"><span data-stu-id="bd253-130">Changing Access Security</span></span>

<span data-ttu-id="bd253-131">Con le autorizzazioni appropriate, è possibile modificare la sicurezza in un oggetto a protezione diretta con uno script o un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd253-131">With appropriate permissions, you can change the security on a securable object with a script or application.</span></span> <span data-ttu-id="bd253-132">È inoltre possibile modificare le impostazioni di sicurezza negli spazi dei nomi WMI utilizzando il [*controllo WMI*](gloss-w.md) oppure aggiungendo una stringa [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) nel file di [*Managed Object Format (MOF)*](gloss-m.md) che definisce le classi per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="bd253-132">You can also change the security settings on WMI namespaces using the [*WMI Control*](gloss-w.md) or by adding a [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) string in the [*Managed Object Format (MOF)*](gloss-m.md) file that defines classes for the namespace.</span></span> <span data-ttu-id="bd253-133">Per ulteriori informazioni, vedere [accedere agli spazi dei nomi WMI](access-to-wmi-namespaces.md), [proteggere gli spazi dei nomi WMI](securing-wmi-namespaces.md)e [modificare la sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bd253-133">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md), [Securing WMI Namespaces](securing-wmi-namespaces.md), and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd253-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd253-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd253-135">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="bd253-135">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="bd253-136">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="bd253-136">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="bd253-137">Controllo dell'account utente e WMI</span><span class="sxs-lookup"><span data-stu-id="bd253-137">User Account Control and WMI</span></span>](user-account-control-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="bd253-138">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="bd253-138">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="bd253-139">Accesso agli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="bd253-139">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
