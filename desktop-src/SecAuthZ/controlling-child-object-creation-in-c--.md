---
description: È possibile utilizzare l'elenco DACL di un oggetto contenitore per controllare gli utenti autorizzati a creare oggetti figlio all'interno del contenitore.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Controllo della creazione di oggetti figlio in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598b2fd9a9889fbb77d2b3a4ecd004efcd823b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527637"
---
# <a name="controlling-child-object-creation-in-c"></a><span data-ttu-id="38d4a-103">Controllo della creazione di oggetti figlio in C++</span><span class="sxs-lookup"><span data-stu-id="38d4a-103">Controlling Child Object Creation in C++</span></span>

<span data-ttu-id="38d4a-104">È possibile utilizzare l'elenco DACL di un oggetto contenitore per controllare gli utenti autorizzati a creare oggetti figlio all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="38d4a-104">You can use the DACL of a container object to control who is allowed to create child objects within the container.</span></span> <span data-ttu-id="38d4a-105">Questo può essere importante perché il creatore di un oggetto viene in genere assegnato come proprietario dell'oggetto e il proprietario di un oggetto può controllare l'accesso all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="38d4a-105">This can be important because the creator of an object is typically assigned as the object's owner, and an object's owner can control access to the object.</span></span>

<span data-ttu-id="38d4a-106">I vari tipi di oggetti contenitore hanno diritti di accesso specifici che controllano la possibilità di creare oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="38d4a-106">The various types of container objects have specific access rights that control the ability to create child objects.</span></span> <span data-ttu-id="38d4a-107">Un thread, ad esempio, deve avere \_ \_ l'accesso key create Sub \_ Key a una chiave del registro di sistema per creare una sottochiave sotto la chiave.</span><span class="sxs-lookup"><span data-stu-id="38d4a-107">For example, a thread must have KEY\_CREATE\_SUB\_KEY access to a registry key to create a subkey under the key.</span></span> <span data-ttu-id="38d4a-108">L'elenco DACL di una chiave del registro di sistema può contenere voci ACE che consentono o negano il diritto di accesso.</span><span class="sxs-lookup"><span data-stu-id="38d4a-108">The DACL of a registry key can contain ACEs that allow or deny this access right.</span></span> <span data-ttu-id="38d4a-109">Analogamente, NTFS supporta il file \_ Add \_ FILE e file \_ Add \_ sottodirectory diritti di accesso per controllare la possibilità di creare file o directory in una directory.</span><span class="sxs-lookup"><span data-stu-id="38d4a-109">Similarly, NTFS supports the FILE\_ADD\_FILE and FILE\_ADD\_SUBDIRECTORY access rights for controlling the ability to create files or directories in a directory.</span></span>

<span data-ttu-id="38d4a-110">La \_ \_ \_ \_ creazione di un diritto di accesso figlio per gli annunci di dominio destro consente di controllare la creazione di oggetti figlio in un oggetto servizio directory (DS).</span><span class="sxs-lookup"><span data-stu-id="38d4a-110">The ADS\_RIGHT\_DS\_CREATE\_CHILD access right controls the creation of child objects in a directory service (DS) object.</span></span> <span data-ttu-id="38d4a-111">Tuttavia, gli oggetti DS possono contenere tipi diversi di oggetti, in modo che il sistema supporti una maggiore granularità del controllo.</span><span class="sxs-lookup"><span data-stu-id="38d4a-111">However, DS objects can contain different types of objects, so the system supports a finer granularity of control.</span></span> <span data-ttu-id="38d4a-112">È possibile utilizzare le [voci ACE specifiche dell'oggetto](object-specific-aces.md) per consentire o negare il diritto di creare un tipo specificato di oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="38d4a-112">You can use [object-specific ACEs](object-specific-aces.md) to allow or deny the right to create a specified type of child object.</span></span> <span data-ttu-id="38d4a-113">È possibile consentire a un utente di creare un tipo di oggetto figlio evitando all'utente di creare altri tipi di oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="38d4a-113">You can allow a user to create one type of child object while preventing the user from creating other types of child objects.</span></span>

<span data-ttu-id="38d4a-114">Nell'esempio seguente viene usata la funzione [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) per aggiungere una voce ACE specifica dell'oggetto a un ACL.</span><span class="sxs-lookup"><span data-stu-id="38d4a-114">The following example uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to add an object-specific ACE to an ACL.</span></span> <span data-ttu-id="38d4a-115">La voce ACE concede l'autorizzazione per creare un tipo specificato di oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="38d4a-115">The ACE grants permission to create a specified type of child object.</span></span> <span data-ttu-id="38d4a-116">Il membro **grfAccessPermissions** della struttura [**di \_ accesso esplicita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) è impostato su Ads \_ Rights \_ DS \_ Create \_ child per indicare che la voce ACE controlla la creazione dell'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="38d4a-116">The **grfAccessPermissions** member of the [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure is set to ADS\_RIGHT\_DS\_CREATE\_CHILD to indicate that the ACE controls the child object creation.</span></span> <span data-ttu-id="38d4a-117">Il membro **ObjectsPresent** della struttura [**Objects \_ e \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) è impostato sul \_ tipo di oggetto ACE \_ \_ presente per indicare che il membro **ObjectTypeGuid** contiene un GUID valido.</span><span class="sxs-lookup"><span data-stu-id="38d4a-117">The **ObjectsPresent** member of the [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure is set to ACE\_OBJECT\_TYPE\_PRESENT to indicate that the **ObjectTypeGuid** member contains a valid GUID.</span></span> <span data-ttu-id="38d4a-118">Il GUID identifica un tipo di oggetto figlio la cui creazione viene controllata.</span><span class="sxs-lookup"><span data-stu-id="38d4a-118">The GUID identifies a type of child object whose creation is being controlled.</span></span>

<span data-ttu-id="38d4a-119">Nell'esempio seguente, pOldDACL deve essere un puntatore valido a una struttura [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) esistente.</span><span class="sxs-lookup"><span data-stu-id="38d4a-119">In the following example, pOldDACL must be a valid pointer to an existing [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) structure.</span></span> <span data-ttu-id="38d4a-120">Per informazioni su come creare una struttura **ACL** per un oggetto, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="38d4a-120">For information about how to create an **ACL** structure for an object, see [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span></span>


```C++
DWORD dwRes;
PACL pOldDACL = NULL;
PACL pNewDACL = NULL;
GUID guidChildObjectType = GUID_NULL;   // GUID of object to control creation of
PSID pTrusteeSID = NULL;           // trustee for new ACE
EXPLICIT_ACCESS ea;
OBJECTS_AND_SID ObjectsAndSID;

// pOldDACL must be a valid pointer to an existing ACL structure.

// guidChildObjectType must be the GUID of an object type 
// that is a possible child of the object associated with pOldDACL.
 
// Initialize an OBJECTS_AND_SID structure with object type GUIDs and 
// the SID of the trustee for the new ACE. 

ZeroMemory(&ObjectsAndSID, sizeof(OBJECTS_AND_SID));
ObjectsAndSID.ObjectsPresent = ACE_OBJECT_TYPE_PRESENT;
ObjectsAndSID.ObjectTypeGuid = guidChildObjectType;
ObjectsAndSID.InheritedObjectTypeGuid  = GUID_NULL;
ObjectsAndSID.pSid = (SID *)pTrusteeSID;

// Initialize an EXPLICIT_ACCESS structure for the new ACE. 

ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_CREATE_CHILD;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= NO_INHERITANCE;
ea.Trustee.TrusteeForm = TRUSTEE_IS_OBJECTS_AND_SID;
ea.Trustee.ptstrName = (LPTSTR) &ObjectsAndSID;

// Create a new ACL that merges the new ACE
// into the existing DACL.

dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
```



 

 



