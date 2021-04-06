---
title: Descrittore di sicurezza predefinito
description: Con Active Directory Domain Services, è anche possibile specificare la sicurezza predefinita per ogni tipo di oggetto.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Descrittore di sicurezza predefinito AD
- descrittori di sicurezza AD, valore predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046529"
---
# <a name="default-security-descriptor"></a><span data-ttu-id="cda47-105">Descrittore di sicurezza predefinito</span><span class="sxs-lookup"><span data-stu-id="cda47-105">Default Security Descriptor</span></span>

<span data-ttu-id="cda47-106">Con Active Directory Domain Services, è anche possibile specificare la sicurezza predefinita per ogni tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="cda47-106">With Active Directory Domain Services, you can also specify default security for each type of object.</span></span> <span data-ttu-id="cda47-107">Viene specificato nell'attributo [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) nella definizione dell'oggetto [**classSchema**](/windows/desktop/ADSchema/c-classschema) nello [schema Active Directory](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="cda47-107">This is specified in the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) attribute in the [**classSchema**](/windows/desktop/ADSchema/c-classschema) object definition in the [Active Directory schema](active-directory-schema.md).</span></span> <span data-ttu-id="cda47-108">Questo descrittore di sicurezza viene usato per fornire la protezione predefinita sull'oggetto se non è stato specificato alcun descrittore di sicurezza durante la creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cda47-108">This security descriptor is used to provide default protection on the object if there is no security descriptor specified during the creation of the object.</span></span>

> [!Note]  
> <span data-ttu-id="cda47-109">Le voci ACE di un descrittore di sicurezza predefinito vengono gestite come se fossero specificate come parte della creazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="cda47-109">ACEs from a default security descriptor are handled as if they were specified as part of object creation.</span></span> <span data-ttu-id="cda47-110">Pertanto, le voci ACE predefinite vengono posizionate sopra le voci ACE ereditate e vengono sostituite in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="cda47-110">Therefore, the default ACEs are placed preceding inherited ACEs and override them as appropriate.</span></span> <span data-ttu-id="cda47-111">Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="cda47-111">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="cda47-112">[**DefaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) viene specificato in un formato stringa speciale utilizzando il linguaggio SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ).</span><span class="sxs-lookup"><span data-stu-id="cda47-112">The [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) is specified in a special string format using the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="cda47-113">È possibile usare due funzioni per convertire il formato binario del descrittore di sicurezza in formato stringa e viceversa.</span><span class="sxs-lookup"><span data-stu-id="cda47-113">Two functions can be used to convert binary form of the security descriptor to string format and vice versa.</span></span> <span data-ttu-id="cda47-114">Queste funzioni sono:</span><span class="sxs-lookup"><span data-stu-id="cda47-114">These functions are:</span></span>

-   [<span data-ttu-id="cda47-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="cda47-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [<span data-ttu-id="cda47-116">ConvertStringSecurityDescriptorToSecurityDescriptor ha</span><span class="sxs-lookup"><span data-stu-id="cda47-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

<span data-ttu-id="cda47-117">Per ulteriori informazioni e per i descrittori di sicurezza predefiniti delle classi di oggetti predefinite, vedere le pagine di riferimento della classe nel riferimento allo schema Active Directory del [riferimento Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cda47-117">For more information and the default security descriptors of the predefined object classes, see the class reference pages in the Active Directory Schema Reference of the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="cda47-118">Per ulteriori informazioni e un esempio di codice per la lettura o la modifica della proprietà [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) di una classe di oggetti, vedere [lettura di defaultSecurityDescriptor per una](reading-the-defaultsecuritydescriptor-for-an-object-class.md) classe di oggetti e [modifica di defaultSecurityDescriptor per una classe di oggetti](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span><span class="sxs-lookup"><span data-stu-id="cda47-118">For more information and a code example that reads or modifies the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) property of an object class, see [Reading the defaultSecurityDescriptor for an Object Class](reading-the-defaultsecuritydescriptor-for-an-object-class.md) and [Modifying the defaultSecurityDescriptor for an Object Class](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span></span>

 

 