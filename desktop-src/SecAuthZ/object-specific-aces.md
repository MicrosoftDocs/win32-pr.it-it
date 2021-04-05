---
description: Le voci ACE specifiche dell'oggetto sono supportate per gli oggetti del servizio directory (DS). Una voce ACE specifica dell'oggetto contiene una coppia di GUID che consente di espandere le modalità di protezione di un oggetto da parte della voce ACE.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: ACE specifiche dell'oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40760e5cd06af97e93f74c6ff8daff89cd5962f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057879"
---
# <a name="object-specific-aces"></a><span data-ttu-id="d5e08-104">ACE specifiche dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="d5e08-104">Object-specific ACEs</span></span>

<span data-ttu-id="d5e08-105">Le [*voci ACE*](/windows/desktop/SecGloss/a-gly) specifiche dell'oggetto sono supportate per gli oggetti del servizio directory (DS).</span><span class="sxs-lookup"><span data-stu-id="d5e08-105">Object-specific [*ACEs*](/windows/desktop/SecGloss/a-gly) are supported for directory service (DS) objects.</span></span> <span data-ttu-id="d5e08-106">Una voce ACE specifica dell'oggetto contiene una coppia di GUID che consente di espandere le modalità di protezione di un oggetto da parte della voce ACE.</span><span class="sxs-lookup"><span data-stu-id="d5e08-106">An object-specific ACE contains a pair of GUIDs that expand the ways in which the ACE can protect an object.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5e08-107">GUID</span><span class="sxs-lookup"><span data-stu-id="d5e08-107">GUID</span></span></th>
<th><span data-ttu-id="d5e08-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5e08-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5e08-109"><strong>ObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="d5e08-109"><strong>ObjectType</strong></span></span></td>
<td><span data-ttu-id="d5e08-110">Identifica uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="d5e08-110">Identifies one of the following:</span></span>
<ul>
<li><span data-ttu-id="d5e08-111">Tipo di oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="d5e08-111">A type of child object.</span></span> <span data-ttu-id="d5e08-112">La voce ACE controlla il diritto di creare un tipo specificato di oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="d5e08-112">The ACE controls the right to create a specified type of child object.</span></span> <span data-ttu-id="d5e08-113">Per ulteriori informazioni, vedere <a href="controlling-child-object-creation-in-c--.md">controllo della creazione di oggetti figlio in C++</a>.</span><span class="sxs-lookup"><span data-stu-id="d5e08-113">For more information, see <a href="controlling-child-object-creation-in-c--.md">Controlling Child Object Creation in C++</a>.</span></span></li>
<li><span data-ttu-id="d5e08-114">Set di proprietà o proprietà.</span><span class="sxs-lookup"><span data-stu-id="d5e08-114">A property set or property.</span></span> <span data-ttu-id="d5e08-115">La voce ACE controlla il diritto di leggere o scrivere la proprietà o il set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d5e08-115">The ACE controls the right to read or write the property or property set.</span></span> <span data-ttu-id="d5e08-116">Per altre informazioni, vedere <a href="aces-to-control-access-to-an-object-s-properties.md">ACE per controllare l'accesso alle proprietà di un oggetto</a>.</span><span class="sxs-lookup"><span data-stu-id="d5e08-116">For more information, see <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs to Control Access to an Object's Properties</a>.</span></span></li>
<li><span data-ttu-id="d5e08-117">Un diritto esteso.</span><span class="sxs-lookup"><span data-stu-id="d5e08-117">An extended right.</span></span> <span data-ttu-id="d5e08-118">La voce ACE controlla il diritto di eseguire l'operazione associata al diritto esteso.</span><span class="sxs-lookup"><span data-stu-id="d5e08-118">The ACE controls the right to perform the operation associated with the extended right.</span></span></li>
<li><span data-ttu-id="d5e08-119">Scrittura convalidata.</span><span class="sxs-lookup"><span data-stu-id="d5e08-119">A validated write.</span></span> <span data-ttu-id="d5e08-120">La voce ACE controlla il diritto di eseguire determinate operazioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="d5e08-120">The ACE controls the right to perform certain write operations.</span></span> <span data-ttu-id="d5e08-121">Queste autorizzazioni di scrittura convalidate, definite ed esposte nell'editor ACL, forniscono le autorizzazioni per le scritture convalidate delle proprietà anziché le scritture di basso livello non controllate di qualsiasi valore in una proprietà concessa con un'autorizzazione per la &quot; Proprietà Write &quot; .</span><span class="sxs-lookup"><span data-stu-id="d5e08-121">These validated write permissions, defined and exposed in the ACL Editor, provide permissions for validated writes of properties rather than unchecked low-level writes of any value to a property that is granted with a &quot;write property&quot; permission.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5e08-122"><strong>InheritedObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="d5e08-122"><strong>InheritedObjectType</strong></span></span></td>
<td><span data-ttu-id="d5e08-123">Indica il tipo di oggetto figlio che può ereditare la voce ACE.</span><span class="sxs-lookup"><span data-stu-id="d5e08-123">Indicates the type of child object that can inherit the ACE.</span></span> <span data-ttu-id="d5e08-124">L'ereditarietà è controllata anche dai flag di ereditarietà nel <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, nonché da qualsiasi protezione contro l'ereditarietà effettuata sugli oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="d5e08-124">Inheritance is also controlled by the inheritance flags in the <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, as well as by any protection against inheritance placed on the child objects.</span></span> <span data-ttu-id="d5e08-125">Per ulteriori informazioni, vedere <a href="ace-inheritance.md">ereditarietà Ace</a>.</span><span class="sxs-lookup"><span data-stu-id="d5e08-125">For more information, see <a href="ace-inheritance.md">ACE Inheritance</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d5e08-126">Sono supportati tre tipi di voci ACE specifiche dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d5e08-126">Three types of object-specific ACEs are supported.</span></span>

> [!Note]  
> <span data-ttu-id="d5e08-127">Le voci ACE degli oggetti di sistema non sono attualmente supportate.</span><span class="sxs-lookup"><span data-stu-id="d5e08-127">System-alarm object ACEs are not currently supported.</span></span>

 



| <span data-ttu-id="d5e08-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5e08-128">Type</span></span>                      | <span data-ttu-id="d5e08-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5e08-129">Description</span></span>                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e08-130">ACE per oggetti con accesso negato</span><span class="sxs-lookup"><span data-stu-id="d5e08-130">Access-denied object ACE</span></span>  | <span data-ttu-id="d5e08-131">Utilizzato in un DACL per negare a un trustee l'accesso a una proprietà o a una proprietà impostata sull'oggetto o per limitare l'ereditarietà ACE a un tipo specificato di oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="d5e08-131">Used in a DACL to deny a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="d5e08-132">Usa la [**struttura \_ \_ \_ ACE negata all'oggetto**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="d5e08-132">Uses the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) structure.</span></span>         |
| <span data-ttu-id="d5e08-133">ACE oggetto consentito Access</span><span class="sxs-lookup"><span data-stu-id="d5e08-133">Access-allowed object ACE</span></span> | <span data-ttu-id="d5e08-134">Utilizzato in un DACL per consentire a un trustee di accedere a una proprietà o a una proprietà impostata sull'oggetto oppure per limitare l'ereditarietà ACE a un tipo specificato di oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="d5e08-134">Used in a DACL to allow a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="d5e08-135">Usa la [**struttura \_ \_ \_ ACE consentita dell'oggetto Access**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="d5e08-135">Uses the [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) structure.</span></span>      |
| <span data-ttu-id="d5e08-136">Controllo di sistema-ACE oggetto</span><span class="sxs-lookup"><span data-stu-id="d5e08-136">System-audit object ACE</span></span>   | <span data-ttu-id="d5e08-137">Utilizzato in un SACL per registrare i tentativi di accesso a una proprietà o a una proprietà impostata nell'oggetto o per limitare l'ereditarietà ACE a un tipo specificato di oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="d5e08-137">Used in a SACL to log a trustee's attempts to access a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="d5e08-138">Usa la [**struttura \_ \_ \_ ACE dell'oggetto controllo di sistema**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="d5e08-138">Uses the [**SYSTEM\_AUDIT\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) structure.</span></span> |



 

<span data-ttu-id="d5e08-139">Tutti gli ACL che contengono una voce ACE specifica dell'oggetto devono usare il servizio di revisione ACL Revisione ACL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d5e08-139">Any ACL that contains an object-specific ACE must use the revision ACL\_REVISION\_DS.</span></span>

 

 
