---
description: Quando un processo tenta di accedere a un oggetto a protezione diretta, il sistema scorre le voci di controllo di accesso (ACE) nell'elenco di controllo di accesso discrezionale (DACL) degli oggetti fino a quando non trova le voci ACE che consentono o negano l'accesso richiesto.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Ordine delle voci ACE in un DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314729"
---
# <a name="order-of-aces-in-a-dacl"></a><span data-ttu-id="20c79-103">Ordine delle voci ACE in un DACL</span><span class="sxs-lookup"><span data-stu-id="20c79-103">Order of ACEs in a DACL</span></span>

<span data-ttu-id="20c79-104">Quando un [*processo*](/windows/desktop/SecGloss/p-gly) tenta di accedere a un oggetto a protezione diretta, il sistema scorre le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) nell' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) dell'oggetto fino a trovare le voci ACE che consentono o negano l'accesso richiesto.</span><span class="sxs-lookup"><span data-stu-id="20c79-104">When a [*process*](/windows/desktop/SecGloss/p-gly) tries to access a securable object, the system steps through the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) until it finds ACEs that allow or deny the requested access.</span></span> <span data-ttu-id="20c79-105">I diritti di accesso consentiti a un elenco DACL possono variare a seconda dell'ordine delle voci ACE nell'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="20c79-105">The access rights that a DACL allows a user could vary depending on the order of ACEs in the DACL.</span></span> <span data-ttu-id="20c79-106">Di conseguenza, il sistema operativo Windows XP definisce un ordine preferito per le voci ACE nell'elenco DACL di un oggetto a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="20c79-106">Consequently, the Windows XP operating system defines a preferred order for ACEs in the DACL of a securable object.</span></span> <span data-ttu-id="20c79-107">L'ordine preferito fornisce un semplice Framework che garantisce che una voce ACE con accesso negato neghi effettivamente l'accesso.</span><span class="sxs-lookup"><span data-stu-id="20c79-107">The preferred order provides a simple framework that ensures that an access-denied ACE actually denies access.</span></span> <span data-ttu-id="20c79-108">Per ulteriori informazioni sull'algoritmo del sistema per il controllo dell'accesso, vedere [come gli elenchi DACL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="20c79-108">For more information about the system's algorithm for checking access, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="20c79-109">Per Windows Server 2003 e Windows XP, l'ordine corretto degli ACE è complicato dall'introduzione delle voci ACE specifiche dell'oggetto e dell'ereditarietà automatica.</span><span class="sxs-lookup"><span data-stu-id="20c79-109">For Windows Server 2003 and Windows XP, the proper order of ACEs is complicated by the introduction of object-specific ACEs and automatic inheritance.</span></span>

<span data-ttu-id="20c79-110">Nei passaggi seguenti viene descritto l'ordine preferito:</span><span class="sxs-lookup"><span data-stu-id="20c79-110">The following steps describe the preferred order:</span></span>

1.  <span data-ttu-id="20c79-111">Tutte le voci ACE esplicite vengono inserite in un gruppo prima di eventuali ACE ereditate.</span><span class="sxs-lookup"><span data-stu-id="20c79-111">All explicit ACEs are placed in a group before any inherited ACEs.</span></span>
2.  <span data-ttu-id="20c79-112">All'interno del gruppo di voci ACE esplicite, le voci ACE con accesso negato vengono inserite prima degli ACE consentiti per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="20c79-112">Within the group of explicit ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>
3.  <span data-ttu-id="20c79-113">Le voci ACE ereditate vengono inserite nell'ordine in cui vengono ereditate.</span><span class="sxs-lookup"><span data-stu-id="20c79-113">Inherited ACEs are placed in the order in which they are inherited.</span></span> <span data-ttu-id="20c79-114">Le voci ACE ereditate dall'elemento padre dell'oggetto figlio vengono prima di tutto, quindi le voci ACE ereditate dal padre e così via fino all'albero degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="20c79-114">ACEs inherited from the child object's parent come first, then ACEs inherited from the grandparent, and so on up the tree of objects.</span></span>
4.  <span data-ttu-id="20c79-115">Per ogni livello di ACE ereditate, le voci ACE con accesso negato vengono inserite prima degli ACE consentiti per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="20c79-115">For each level of inherited ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>

<span data-ttu-id="20c79-116">Naturalmente, non tutti i tipi ACE sono necessari in un ACL.</span><span class="sxs-lookup"><span data-stu-id="20c79-116">Of course, not all ACE types are required in an ACL.</span></span>

<span data-ttu-id="20c79-117">Funzioni quali [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) e [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) aggiungono una voce ACE alla fine di un ACL.</span><span class="sxs-lookup"><span data-stu-id="20c79-117">Functions such as [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) and [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) add an ACE to the end of an ACL.</span></span> <span data-ttu-id="20c79-118">È responsabilità del chiamante assicurarsi che le voci ACE vengano aggiunte nell'ordine corretto.</span><span class="sxs-lookup"><span data-stu-id="20c79-118">It is the caller's responsibility to ensure that the ACEs are added in the proper order.</span></span>

 

 
