---
title: Controllo dell'accesso agli oggetti e alle relative proprietà
description: Per controllare l'accesso agli oggetti applicazione, usare il descrittore di sicurezza dell'oggetto e, in particolare, con l'elenco di controllo di accesso discrezionale (DACL) e il relativo elenco di voci di controllo di accesso (ACE).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- oggetto AD, controllo dell'accesso a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220884"
---
# <a name="controlling-access-to-objects-and-their-properties"></a><span data-ttu-id="f8c86-104">Controllo dell'accesso agli oggetti e alle relative proprietà</span><span class="sxs-lookup"><span data-stu-id="f8c86-104">Controlling Access to Objects and Their Properties</span></span>

<span data-ttu-id="f8c86-105">Per controllare l'accesso agli oggetti applicazione, usare il descrittore di sicurezza dell'oggetto e, in particolare, con l'elenco di controllo di accesso discrezionale (DACL) e il relativo elenco di voci di controllo di accesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="f8c86-105">To control access to application objects, work with the object security descriptor, and specifically, with the discretionary access-control list (DACL) and its list of access-control entries (ACEs).</span></span>

<span data-ttu-id="f8c86-106">Quando viene creato un oggetto, viene ricevuto un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f8c86-106">When an object is created, it receives a security descriptor.</span></span> <span data-ttu-id="f8c86-107">Per ulteriori informazioni e per una descrizione delle regole utilizzate dal sistema per creare l'elenco DACL per un nuovo oggetto, vedere la pagina [relativa alla modalità di impostazione dei descrittori di sicurezza per i nuovi oggetti directory](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f8c86-107">For more information, and a description of the rules that the system uses to create the DACL for a new object, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span> <span data-ttu-id="f8c86-108">Queste regole rivelano che è possibile:</span><span class="sxs-lookup"><span data-stu-id="f8c86-108">These rules reveal that you can:</span></span>

-   <span data-ttu-id="f8c86-109">Creare un nuovo descrittore di sicurezza e collegarlo all'oggetto al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="f8c86-109">Create a new security descriptor and attach it to the object at creation time.</span></span> <span data-ttu-id="f8c86-110">Per ulteriori informazioni, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto directory](creating-a-security-descriptor-for-a-new-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="f8c86-110">For more information, see [Creating a Security Descriptor for a New Directory Object](creating-a-security-descriptor-for-a-new-directory-object.md).</span></span>
-   <span data-ttu-id="f8c86-111">Applicare una voce ACE ereditabile, in qualsiasi punto della gerarchia di directory, in modo che una voce ACE venga ereditata dagli oggetti nell'albero.</span><span class="sxs-lookup"><span data-stu-id="f8c86-111">Apply an inheritable ACE, at any point in the directory hierarchy, such that an ACE is inherited by objects down the tree.</span></span> <span data-ttu-id="f8c86-112">Un oggetto può ereditare una voce ACE dal relativo contenitore padre.</span><span class="sxs-lookup"><span data-stu-id="f8c86-112">An object can inherit an ACE from its parent container.</span></span> <span data-ttu-id="f8c86-113">Per ulteriori informazioni, vedere [ereditarietà e delega dell'amministrazione](inheritance-and-delegation-of-administration.md).</span><span class="sxs-lookup"><span data-stu-id="f8c86-113">For more information, see [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md).</span></span>
-   <span data-ttu-id="f8c86-114">Specificare una voce ACE nell'elenco DACL predefinito nello schema, se si dispone dei diritti di accesso necessari.</span><span class="sxs-lookup"><span data-stu-id="f8c86-114">Specify an ACE in the default DACL in the schema, if you have the necessary access rights.</span></span> <span data-ttu-id="f8c86-115">Ogni definizione di classe di oggetto nello schema include un descrittore di sicurezza predefinito che può avere un DACL predefinito.</span><span class="sxs-lookup"><span data-stu-id="f8c86-115">Every object class definition in the schema includes a default security descriptor that can have a default DACL.</span></span> <span data-ttu-id="f8c86-116">Per ulteriori informazioni, vedere [descrittore di sicurezza predefinito](default-security-descriptor.md).</span><span class="sxs-lookup"><span data-stu-id="f8c86-116">For more information, see [Default Security Descriptor](default-security-descriptor.md).</span></span>

<span data-ttu-id="f8c86-117">Inoltre, è possibile modificare l'elenco DACL di un oggetto esistente.</span><span class="sxs-lookup"><span data-stu-id="f8c86-117">In addition the DACL of an existing object can be modified.</span></span> <span data-ttu-id="f8c86-118">È possibile:</span><span class="sxs-lookup"><span data-stu-id="f8c86-118">You can:</span></span>

-   <span data-ttu-id="f8c86-119">Sostituire l'elenco DACL con uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="f8c86-119">Replace the DACL with a new one.</span></span>
-   <span data-ttu-id="f8c86-120">Leggere l'elenco DACL esistente, modificarlo e applicare l'elenco DACL modificato.</span><span class="sxs-lookup"><span data-stu-id="f8c86-120">Read the existing DACL, modify it, and apply the modified DACL.</span></span> <span data-ttu-id="f8c86-121">Per ulteriori informazioni, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="f8c86-121">For more information, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="f8c86-122">Nell'elenco seguente viene descritta la funzione più importante di una voce ACE in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f8c86-122">The following list describes the most important function of an ACE in Active Directory Domain Services.</span></span> <span data-ttu-id="f8c86-123">Con una voce ACE è possibile:</span><span class="sxs-lookup"><span data-stu-id="f8c86-123">With an ACE, you can:</span></span>

-   <span data-ttu-id="f8c86-124">Controllare gli utenti che possono eseguire operazioni specifiche su un oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8c86-124">Control who can perform specific operations on an object.</span></span>
-   <span data-ttu-id="f8c86-125">Controllo che ha accesso a una proprietà specifica o a un set di proprietà di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8c86-125">Control who has access to a specific property, or set of properties, of an object.</span></span>
-   <span data-ttu-id="f8c86-126">Controllare gli utenti che possono creare oggetti figlio in un contenitore, inclusi gli utenti che possono creare un tipo specifico di oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="f8c86-126">Control who can create child objects in a container, including who can create a specific type of child object.</span></span>
-   <span data-ttu-id="f8c86-127">Definire i diritti di accesso ai controlli privati per un tipo di oggetto e controllare chi può eseguire le operazioni protette da diritti privati.</span><span class="sxs-lookup"><span data-stu-id="f8c86-127">Define private control-access rights for an object type and control who can perform the operations protected by the private rights.</span></span>
-   <span data-ttu-id="f8c86-128">Applicare una voce ACE a un oggetto contenitore alla radice di un sottoalbero di directory, in modo che le protezioni possano essere ereditate automaticamente da tutti gli oggetti figlio nella struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="f8c86-128">Apply an ACE to a container object at the root of a directory subtree, such that the protections can be inherited automatically by all child objects down the tree.</span></span>
-   <span data-ttu-id="f8c86-129">Applicare una voce ACE ereditata automaticamente da un tipo specifico di oggetto figlio in un sottoalbero.</span><span class="sxs-lookup"><span data-stu-id="f8c86-129">Apply an ACE that is inherited automatically by a specific type of child object in a subtree.</span></span>
-   <span data-ttu-id="f8c86-130">Creare una voce ACE che conceda diritti a un gruppo di sicurezza, anziché a un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="f8c86-130">Create an ACE that grants rights to a security group, rather than to a single user.</span></span>
-   <span data-ttu-id="f8c86-131">Applicare una voce ACE a oggetti Criteri di gruppo per controllare gli account e i computer interessati dai criteri.</span><span class="sxs-lookup"><span data-stu-id="f8c86-131">Apply an ACE to Group Policy Objects to control the accounts and computers affected by the policy.</span></span>

 

 




