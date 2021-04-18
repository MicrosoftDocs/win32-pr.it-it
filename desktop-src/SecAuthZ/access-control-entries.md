---
description: Una voce di controllo di accesso (ACE) è un elemento in un elenco di controllo di accesso (ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Voci di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310955"
---
# <a name="access-control-entries"></a><span data-ttu-id="613e8-103">Voci di controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="613e8-103">Access Control Entries</span></span>

<span data-ttu-id="613e8-104">Una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) è un elemento in un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="613e8-104">An [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) is an element in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span> <span data-ttu-id="613e8-105">Un ACL può avere zero o più voci ACE.</span><span class="sxs-lookup"><span data-stu-id="613e8-105">An ACL can have zero or more ACEs.</span></span> <span data-ttu-id="613e8-106">Ogni ACE controlla o monitora l'accesso a un oggetto da un trustee specificato.</span><span class="sxs-lookup"><span data-stu-id="613e8-106">Each ACE controls or monitors access to an object by a specified trustee.</span></span> <span data-ttu-id="613e8-107">Per informazioni sull'aggiunta, la rimozione o la modifica delle voci ACE negli ACL di un oggetto, vedere [modifica degli ACL di un oggetto in C++](modifying-the-acls-of-an-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="613e8-107">For information about adding, removing, or changing the ACEs in an object's ACLs, see [Modifying the ACLs of an Object in C++](modifying-the-acls-of-an-object-in-c--.md).</span></span>

<span data-ttu-id="613e8-108">Sono disponibili sei tipi di ACE, tre dei quali sono supportati da tutti gli oggetti a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="613e8-108">There are six types of ACEs, three of which are supported by all securable objects.</span></span> <span data-ttu-id="613e8-109">Gli altri tre tipi sono [ACE specifici](object-specific-aces.md) degli oggetti supportati dagli oggetti del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="613e8-109">The other three types are [Object-specific ACEs](object-specific-aces.md) supported by directory service objects.</span></span>

<span data-ttu-id="613e8-110">Tutti i tipi di voci ACE contengono le informazioni di controllo di accesso seguenti:</span><span class="sxs-lookup"><span data-stu-id="613e8-110">All types of ACEs contain the following access control information:</span></span>

-   <span data-ttu-id="613e8-111">[ID di sicurezza](security-identifiers.md) (SID) che identifica il [trustee](trustees.md) a cui viene applicata la voce ACE.</span><span class="sxs-lookup"><span data-stu-id="613e8-111">A [security identifier](security-identifiers.md) (SID) that identifies the [trustee](trustees.md) to which the ACE applies.</span></span>
-   <span data-ttu-id="613e8-112">[*Maschera di accesso*](/windows/desktop/SecGloss/a-gly) che specifica i [diritti di accesso](access-rights-and-access-masks.md) controllati dalla voce ACE.</span><span class="sxs-lookup"><span data-stu-id="613e8-112">An [*access mask*](/windows/desktop/SecGloss/a-gly) that specifies the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span>
-   <span data-ttu-id="613e8-113">Flag che indica il tipo di voce ACE.</span><span class="sxs-lookup"><span data-stu-id="613e8-113">A flag that indicates the type of ACE.</span></span>
-   <span data-ttu-id="613e8-114">Set di flag di bit che determinano se i contenitori figlio o gli oggetti possono ereditare la voce ACE dall'oggetto primario a cui è collegato l'ACL.</span><span class="sxs-lookup"><span data-stu-id="613e8-114">A set of bit flags that determine whether child containers or objects can inherit the ACE from the primary object to which the ACL is attached.</span></span>

<span data-ttu-id="613e8-115">Nella tabella seguente sono elencati i tre tipi ACE supportati da tutti gli oggetti a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="613e8-115">The following table lists the three ACE types supported by all securable objects.</span></span>



| <span data-ttu-id="613e8-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="613e8-116">Type</span></span>               | <span data-ttu-id="613e8-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="613e8-117">Description</span></span>                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613e8-118">ACE con accesso negato</span><span class="sxs-lookup"><span data-stu-id="613e8-118">Access-denied ACE</span></span>  | <span data-ttu-id="613e8-119">Utilizzato in un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) per negare i diritti di accesso a un trustee.</span><span class="sxs-lookup"><span data-stu-id="613e8-119">Used in a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) to deny access rights to a trustee.</span></span>                                       |
| <span data-ttu-id="613e8-120">ACE consentito per l'accesso</span><span class="sxs-lookup"><span data-stu-id="613e8-120">Access-allowed ACE</span></span> | <span data-ttu-id="613e8-121">Utilizzato in un DACL per consentire diritti di accesso a un trustee.</span><span class="sxs-lookup"><span data-stu-id="613e8-121">Used in a DACL to allow access rights to a trustee.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="613e8-122">ACE di controllo del sistema</span><span class="sxs-lookup"><span data-stu-id="613e8-122">System-audit ACE</span></span>   | <span data-ttu-id="613e8-123">Utilizzato in un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) per generare un record di controllo quando il trustee tenta di esercitare i diritti di accesso specificati.</span><span class="sxs-lookup"><span data-stu-id="613e8-123">Used in a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL) to generate an audit record when the trustee attempts to exercise the specified access rights.</span></span> |



 

<span data-ttu-id="613e8-124">Per una tabella di voci ACE specifiche dell'oggetto, vedere [ACE specifici degli oggetti](object-specific-aces.md).</span><span class="sxs-lookup"><span data-stu-id="613e8-124">For a table of object-specific ACEs, see [Object-specific ACEs](object-specific-aces.md).</span></span>

> [!Note]  
> <span data-ttu-id="613e8-125">Le voci ACE degli oggetti di sistema non sono attualmente supportate.</span><span class="sxs-lookup"><span data-stu-id="613e8-125">System-alarm object ACEs are not currently supported.</span></span>

 

 

 
