---
title: Attributi dell'oggetto utente
description: Un oggetto utente dispone di più attributi. Questa sezione illustra gli attributi chiave usati da Windows, strumenti di amministrazione e la Rubrica di Windows (WAB). Non descrive tutti gli attributi. molti attributi non vengono usati per l'oggetto utente.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- AD degli attributi degli oggetti utente
- Utenti AD, attributi degli oggetti utente
- Oggetti AD, utente, attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c90d8d5f28c41971f5f6910cfb8bef1fafd6f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956295"
---
# <a name="user-object-attributes"></a><span data-ttu-id="f9963-108">Attributi dell'oggetto utente</span><span class="sxs-lookup"><span data-stu-id="f9963-108">User Object Attributes</span></span>

<span data-ttu-id="f9963-109">Un oggetto utente dispone di più attributi.</span><span class="sxs-lookup"><span data-stu-id="f9963-109">A user object has multiple attributes.</span></span> <span data-ttu-id="f9963-110">Questa sezione illustra gli attributi chiave usati da Windows, strumenti di amministrazione e la Rubrica di Windows (WAB).</span><span class="sxs-lookup"><span data-stu-id="f9963-110">This section documents key attributes used by Windows, administrative tools, and the Windows Address Book (WAB).</span></span> <span data-ttu-id="f9963-111">Non descrive tutti gli attributi. molti attributi non vengono usati per l'oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="f9963-111">It does not describe all attributes; many attributes are not used for the user object.</span></span>

<span data-ttu-id="f9963-112">Alcuni attributi vengono archiviati nella directory, ad esempio [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)e così via, e replicati in tutti i controller di dominio all'interno di un dominio.</span><span class="sxs-lookup"><span data-stu-id="f9963-112">Some attributes are stored in the directory, such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), and so on, and replicated to all domain controllers within a domain.</span></span> <span data-ttu-id="f9963-113">Un subset di questi attributi viene inoltre replicato nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="f9963-113">A subset of these attributes is also replicated to the global catalog.</span></span>

<span data-ttu-id="f9963-114">Gli attributi non replicati vengono archiviati in ogni controller di dominio, ma non vengono replicati altrove, ad esempio [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**LastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**LastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)e così via.</span><span class="sxs-lookup"><span data-stu-id="f9963-114">Non-replicated attributes are stored on each domain controller, but are not replicated elsewhere, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), and so on.</span></span> <span data-ttu-id="f9963-115">Gli attributi non replicati sono attributi che riguardano un particolare controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="f9963-115">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="f9963-116">Ad esempio, **LastLogon** è l'ultima data e ora in cui l'accesso alla rete utente è stato convalidato dal particolare controller di dominio che restituisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="f9963-116">For example, **lastLogon** is the last date and time that the user network logon was validated by the particular domain controller that is returning the property.</span></span>

<span data-ttu-id="f9963-117">Un oggetto utente dispone inoltre di attributi costruiti che non sono archiviati nella directory, ma vengono calcolati dal controller di dominio, ad esempio [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**Distinguishname**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes)e così via.</span><span class="sxs-lookup"><span data-stu-id="f9963-117">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), and so on.</span></span>

<span data-ttu-id="f9963-118">Gli attributi per gli oggetti utente sono classificati come:</span><span class="sxs-lookup"><span data-stu-id="f9963-118">Attributes for user objects are classified as:</span></span>

<dl> <dt>

<span data-ttu-id="f9963-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Attributi dell'oggetto di base</span><span class="sxs-lookup"><span data-stu-id="f9963-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Base Object Attributes</span></span>
</dt> <dd>

<span data-ttu-id="f9963-120">Questa categoria include gli attributi necessari per tutti gli oggetti directory, ad esempio [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)e così via.</span><span class="sxs-lookup"><span data-stu-id="f9963-120">This category includes attributes required for all directory objects, such as [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and so on.</span></span>

</dd> <dt>

<span data-ttu-id="f9963-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Attributi di denominazione</span><span class="sxs-lookup"><span data-stu-id="f9963-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Naming Attributes</span></span>
</dt> <dd>

<span data-ttu-id="f9963-122">Questa categoria include attributi usati per fare riferimento a o identificare l'oggetto, ad esempio [**Distinguishname**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid)e così via.</span><span class="sxs-lookup"><span data-stu-id="f9963-122">This category includes attributes used to refer to or identify the object, such as [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), and so on.</span></span> <span data-ttu-id="f9963-123">Per ulteriori informazioni sulla denominazione degli attributi degli oggetti utente, vedere [attributi di denominazione degli utenti](naming-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f9963-123">For more information about naming attributes for user objects, see [User Naming Attributes](naming-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9963-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Attributi di sicurezza</span><span class="sxs-lookup"><span data-stu-id="f9963-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Security Attributes</span></span>
</dt> <dd>

<span data-ttu-id="f9963-125">Questa categoria include gli attributi per il controllo di accesso e accesso.</span><span class="sxs-lookup"><span data-stu-id="f9963-125">This category includes attributes for logon and access control.</span></span> <span data-ttu-id="f9963-126">Per ulteriori informazioni sugli attributi di sicurezza per gli oggetti utente, vedere [attributi di sicurezza utente](security-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f9963-126">For more information about security attributes for user objects, see [User Security Attributes](security-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9963-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Attributi Rubrica</span><span class="sxs-lookup"><span data-stu-id="f9963-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Address Book Attributes</span></span>
</dt> <dd>

<span data-ttu-id="f9963-128">Questa categoria include gli attributi per la posta elettronica e i dati utente.</span><span class="sxs-lookup"><span data-stu-id="f9963-128">This category includes attributes for email and user data.</span></span> <span data-ttu-id="f9963-129">Per ulteriori informazioni sugli attributi degli indirizzi Rubrica per gli oggetti utente, vedere attributi della rubrica [utente](address-book-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f9963-129">For more information about address book attributes for user objects, see [User Address Book Attributes](address-book-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9963-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Attributi specifici dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f9963-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Application Specific Attributes</span></span>
</dt> <dd>

<span data-ttu-id="f9963-131">Questa categoria include i dati di configurazione specifici dell'utente per applicazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="f9963-131">This category includes user-specific configuration data for specific applications.</span></span>

</dd> </dl>

<span data-ttu-id="f9963-132">Per ulteriori informazioni sulla lettura e la modifica degli attributi per un oggetto utente, vedere [lettura e scrittura degli attributi degli oggetti in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="f9963-132">For more information about reading and modifying attributes for a user object, see [Reading and Writing Attributes of Objects in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="f9963-133">Per ulteriori informazioni sulla classe utente, incluso un elenco completo degli attributi [**mayContain**](/windows/desktop/ADSchema/a-maycontain) e [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) della classe, vedere [**User**](/windows/desktop/ADSchema/c-user).</span><span class="sxs-lookup"><span data-stu-id="f9963-133">For more information about the User class, including a complete list of the [**mayContain**](/windows/desktop/ADSchema/a-maycontain) and [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) attributes of the class, see [**User**](/windows/desktop/ADSchema/c-user).</span></span>

## <a name="setting-passwords"></a><span data-ttu-id="f9963-134">Impostazione delle password</span><span class="sxs-lookup"><span data-stu-id="f9963-134">Setting Passwords</span></span>

<span data-ttu-id="f9963-135">Non è possibile modificare direttamente la password di un utente perché questa operazione comporterebbe l'invio di una password non crittografata sulla rete.</span><span class="sxs-lookup"><span data-stu-id="f9963-135">The password for a user cannot be modified directly because this would involve sending an unencrypted password over the network.</span></span> <span data-ttu-id="f9963-136">Per impostare la password per un utente, è necessario usare il metodo [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) o [**IADsUser. sepassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="f9963-136">To set the password for a user, it is necessary to use the [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) or [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="f9963-137">Il metodo **IADsUser. ChangePassword** viene utilizzato quando l'applicazione consente all'utente di modificare la propria password.</span><span class="sxs-lookup"><span data-stu-id="f9963-137">The **IADsUser.ChangePassword** method is used when the application is allowing the user to change their own password.</span></span> <span data-ttu-id="f9963-138">Il metodo **IADsUser. sepassword** viene utilizzato quando l'applicazione consente a un amministratore di reimpostare una password.</span><span class="sxs-lookup"><span data-stu-id="f9963-138">The **IADsUser.SetPassword** method is used when the application enables an administrator to reset a password.</span></span>

 

 