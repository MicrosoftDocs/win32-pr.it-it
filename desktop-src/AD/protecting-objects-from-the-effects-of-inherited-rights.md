---
title: Protezione di oggetti dagli effetti dei diritti ereditati
description: Come illustrato nell'argomento ereditarietà e delega dell'amministrazione, le voci ACE possono essere impostate su un oggetto contenitore, ad esempio organizationalUnit, domainDNS, container e così via, e propagate agli oggetti figlio in base ai flag ACE impostati su tali ACE.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protezione di oggetti dagli effetti di Active Directory con diritti ereditati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046497"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a><span data-ttu-id="43e45-104">Protezione di oggetti dagli effetti dei diritti ereditati</span><span class="sxs-lookup"><span data-stu-id="43e45-104">Protecting Objects from the Effects of Inherited Rights</span></span>

<span data-ttu-id="43e45-105">Come illustrato nell'argomento [ereditarietà e delega dell'amministrazione](inheritance-and-delegation-of-administration.md), le voci ACE possono essere impostate su un oggetto contenitore, ad esempio **OrganizationalUnit**, **domainDNS**, **container** e così via, e propagate agli oggetti figlio in base ai flag ACE impostati su tali ACE.</span><span class="sxs-lookup"><span data-stu-id="43e45-105">As discussed in the topic [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md), ACEs can be set on a container object, such as an **organizationalUnit**, **domainDNS**, **container**, and so on, and propagated to child objects based on the ACE flags set on those ACEs.</span></span>

<span data-ttu-id="43e45-106">Se si dispone di un oggetto protetto o di un oggetto le cui voci ACE si desidera controllare in modo esplicito, ad esempio un'unità organizzativa privata o un utente speciale, è possibile impedire la propagazione delle voci ACE all'oggetto tramite il contenitore padre o i predecessori del contenitore padre.</span><span class="sxs-lookup"><span data-stu-id="43e45-106">If you have a secure object or an object whose ACEs you want to explicitly control, such as a private OU or a special user, you can prevent ACEs from being propagated to the object by its parent container or its parent container's predecessors.</span></span>

<span data-ttu-id="43e45-107">Utilizzare la proprietà [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per controllare se i DACL e i SACL vengono ereditati dall'oggetto dal relativo contenitore padre.</span><span class="sxs-lookup"><span data-stu-id="43e45-107">Use the [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property to control whether DACLs and SACLs are inherited by the object from its parent container.</span></span>

<span data-ttu-id="43e45-108">È possibile usare la proprietà [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per proteggere un oggetto dagli effetti delle voci ACE ereditate.</span><span class="sxs-lookup"><span data-stu-id="43e45-108">The [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property can be used to protect an object from the effects of inherited ACEs.</span></span> <span data-ttu-id="43e45-109">I flag seguenti consentono di impostare in modo esplicito il controllo di accesso sull'oggetto e impedire a un utente di modificare il controllo di accesso all'oggetto impostando le voci ACE ereditabili sul contenitore padre dell'oggetto o i predecessori del relativo contenitore padre.</span><span class="sxs-lookup"><span data-stu-id="43e45-109">The following flags force access control to be set explicitly on the object and prevent a user from modifying access control to the object by setting inheritable ACEs on the object's parent container, or its parent container's predecessors.</span></span>



| <span data-ttu-id="43e45-110">Flag</span><span class="sxs-lookup"><span data-stu-id="43e45-110">Flag</span></span>                               | <span data-ttu-id="43e45-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43e45-111">Description</span></span>                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43e45-112">**\_elenco DACL se \_ protetto**</span><span class="sxs-lookup"><span data-stu-id="43e45-112">**SE\_DACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="43e45-113">Impedisce l'applicazione degli ACE impostati sull'elenco DACL del contenitore padre e di tutti gli oggetti sopra il contenitore padre nella gerarchia di directory, dall'applicazione all'oggetto DACL.</span><span class="sxs-lookup"><span data-stu-id="43e45-113">Prevents ACEs set on the DACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object DACL.</span></span><br/> |
| <span data-ttu-id="43e45-114">**SE \_ SACL è \_ protetto**</span><span class="sxs-lookup"><span data-stu-id="43e45-114">**SE\_SACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="43e45-115">Impedisce l'applicazione di Ace impostati sull'elenco SACL del contenitore padre e di tutti gli oggetti sopra il contenitore padre nella gerarchia di directory, dall'applicazione al SACL dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="43e45-115">Prevents ACEs set on the SACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object SACL.</span></span><br/> |



 

<span data-ttu-id="43e45-116">Tenere presente che il flag di **\_ \_ presenza DACL se** deve essere presente per impostare **se \_ DACL \_ protected** e **se SACL è \_ \_ presente** devono essere presenti per impostare **se \_ SACL \_ protected**.</span><span class="sxs-lookup"><span data-stu-id="43e45-116">Be aware that the **SE\_DACL\_PRESENT** flag must be present to set **SE\_DACL\_PROTECTED** and **SE\_SACL\_PRESENT** must be present to set **SE\_SACL\_PROTECTED**.</span></span>

 

