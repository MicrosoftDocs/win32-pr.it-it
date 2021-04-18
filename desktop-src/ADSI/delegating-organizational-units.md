---
title: Delega di unità organizzative
description: La società Fabrikam ingaggia due amministratori, Mike e Paul, per gestire rispettivamente le unità organizzative East e West.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297689"
---
# <a name="delegating-organizational-units"></a><span data-ttu-id="a85f2-103">Delega di unità organizzative</span><span class="sxs-lookup"><span data-stu-id="a85f2-103">Delegating Organizational Units</span></span>

<span data-ttu-id="a85f2-104">La società Fabrikam ingaggia due amministratori, Mike e Paul, per gestire rispettivamente le unità organizzative East e West.</span><span class="sxs-lookup"><span data-stu-id="a85f2-104">The Fabrikam company hires two administrators, Mike and Paul, to manage the East and West organizational units, respectively.</span></span> <span data-ttu-id="a85f2-105">Davide delega le sue responsabilità amministrative in modo che possano creare ed eliminare gli utenti nelle rispettive unità organizzative.</span><span class="sxs-lookup"><span data-stu-id="a85f2-105">Joe delegates his administrative responsibilities to them so that they can create and delete users in their respective organizational units.</span></span>

<span data-ttu-id="a85f2-106">Prima di vedere come configurare queste unità organizzative in Mike e Paul, è necessario comprendere come configurare l'accesso agli oggetti in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a85f2-106">Before seeing how to set up these organizational units under Mike and Paul, you must understand how to set up access to objects in Active Directory.</span></span> <span data-ttu-id="a85f2-107">Ogni oggetto in Active Directory dispone di un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a85f2-107">Each object in Active Directory has a security descriptor.</span></span> <span data-ttu-id="a85f2-108">Con il descrittore di sicurezza è possibile modificare le autorizzazioni per l'oggetto, propagare le autorizzazioni, abilitare il controllo e così via.</span><span class="sxs-lookup"><span data-stu-id="a85f2-108">With the security descriptor, you can modify permissions on the object, propagate permissions, enable auditing, and so on.</span></span> <span data-ttu-id="a85f2-109">Il descrittore di sicurezza dispone di due elenchi di controllo di accesso (ACL): un ACL discrezionale (DACL) e un ACL di sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="a85f2-109">The security descriptor itself has two access control lists (ACLs): a discretionary ACL (DACL) and a system ACL (SACL).</span></span> <span data-ttu-id="a85f2-110">Ogni ACL può contenere voci di controllo di accesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="a85f2-110">Each ACL can contain access control entries (ACEs).</span></span> <span data-ttu-id="a85f2-111">Con una voce ACE è possibile impostare l'accesso consentito o negato per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="a85f2-111">With an ACE, you can set allowed or denied access on an object.</span></span> <span data-ttu-id="a85f2-112">Inoltre, è possibile specificare azioni specifiche da concedere o negare.</span><span class="sxs-lookup"><span data-stu-id="a85f2-112">In addition, you can specify specific actions to allow or deny.</span></span> <span data-ttu-id="a85f2-113">Esempi di azioni includono Create Child, Delete Child, Read Property e Write Property.</span><span class="sxs-lookup"><span data-stu-id="a85f2-113">Examples of actions include Create Child, Delete Child, Read Property, and Write Property.</span></span> <span data-ttu-id="a85f2-114">Questi diritti vengono specificati con [**accessMask**](iadsaccesscontrolentry-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a85f2-114">These rights are specified with the [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span></span>

<span data-ttu-id="a85f2-115">Successivamente, è possibile specificare le classi o gli attributi a cui è associata questa voce ACE.</span><span class="sxs-lookup"><span data-stu-id="a85f2-115">Next, you may specify the classes or attributes to which this ACE is associated.</span></span> <span data-ttu-id="a85f2-116">Nell'esempio di Fabrikam che segue, Davide sceglie la classe utente in modo che ogni amministratore possa aggiungere utenti al sistema.</span><span class="sxs-lookup"><span data-stu-id="a85f2-116">In the Fabrikam example that follows, Joe picks the user class so that each administrator can add users to the system.</span></span> <span data-ttu-id="a85f2-117">Successivamente, è necessario rispondere alla domanda: "chi sarà il beneficiario di questo ACE?"</span><span class="sxs-lookup"><span data-stu-id="a85f2-117">Next, you must answer the question: "Who will be the beneficiary of this ACE?"</span></span> <span data-ttu-id="a85f2-118">Joe specificherà Mike.</span><span class="sxs-lookup"><span data-stu-id="a85f2-118">Joe will specify Mike.</span></span>

<span data-ttu-id="a85f2-119">Infine, è possibile impostare il comportamento di ereditarietà ACE, ad esempio è possibile specificare ACE per propagare la gerarchia.</span><span class="sxs-lookup"><span data-stu-id="a85f2-119">Finally, you can set the ACE inheritance behavior—for example, ACEs can be specified to propagate down the hierarchy.</span></span> <span data-ttu-id="a85f2-120">In breve, l'esempio precedente comporterà la creazione ed eliminazione di oggetti utente nell'unità organizzativa Sales East.</span><span class="sxs-lookup"><span data-stu-id="a85f2-120">In summary, the previous example will result in Mike being able to create and delete user objects under the East Sales organizational unit.</span></span>

<span data-ttu-id="a85f2-121">Joe usa l'esempio di codice seguente per configurare le voci ACE e ACL nell'unità organizzativa East.</span><span class="sxs-lookup"><span data-stu-id="a85f2-121">Joe uses the following code example to set up the ACEs and ACLs on the East organizational unit.</span></span>


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



<span data-ttu-id="a85f2-122">Nella figura seguente viene illustrato il menu Active Directory **Crea nuovo visualizzazione** dopo l'esecuzione del codice.</span><span class="sxs-lookup"><span data-stu-id="a85f2-122">The following figure shows the Active Directory **Create New View** menu after the code runs.</span></span> <span data-ttu-id="a85f2-123">Quando Joe, l'amministratore, accede, vede diverse classi che è possibile creare.</span><span class="sxs-lookup"><span data-stu-id="a85f2-123">When Joe, the administrator, logs on, he sees several classes that he can create.</span></span> <span data-ttu-id="a85f2-124">Tuttavia, quando Mike si connette, può solo creare oggetti utente.</span><span class="sxs-lookup"><span data-stu-id="a85f2-124">However, when Mike logs on, he is able only to create user objects.</span></span>

![menu di opzione Crea nuova vista](images/adadsi5.png)

<span data-ttu-id="a85f2-126">Per altre informazioni, vedere [modello di sicurezza ADSI](adsi-security-model.md).</span><span class="sxs-lookup"><span data-stu-id="a85f2-126">For more information, see [ADSI Security Model](adsi-security-model.md).</span></span>

 

 




