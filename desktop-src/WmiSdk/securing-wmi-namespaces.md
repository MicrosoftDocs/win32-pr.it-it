---
description: L'accesso agli spazi dei nomi WMI e i relativi dati sono controllati dai descrittori di sicurezza.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Sicurezza degli spazi dei nomi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309890"
---
# <a name="securing-wmi-namespaces"></a><span data-ttu-id="873a1-103">Sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="873a1-103">Securing WMI Namespaces</span></span>

<span data-ttu-id="873a1-104">L'accesso agli spazi dei nomi WMI e i relativi dati sono controllati dai [*descrittori di sicurezza*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="873a1-104">Access to WMI namespaces and their data is controlled by [*security descriptors*](gloss-s.md).</span></span> <span data-ttu-id="873a1-105">È possibile proteggere i dati negli [*spazi dei nomi*](gloss-n.md) modificando il descrittore di sicurezza dello spazio dei nomi per controllare chi ha accesso ai dati e ai metodi.</span><span class="sxs-lookup"><span data-stu-id="873a1-105">You can protect data in your [*namespaces*](gloss-n.md) by adjusting the namespace security descriptor to control who has access to the data and methods.</span></span> <span data-ttu-id="873a1-106">Per ulteriori informazioni, vedere [accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="873a1-106">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>


<span data-ttu-id="873a1-107">Negli argomenti seguenti viene descritta la sicurezza dello spazio dei nomi WMI e viene illustrato come controllare l'accesso agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="873a1-107">The following topics describe WMI namespace security and how to control access to namespaces.</span></span>

<dl> <dt>

<span data-ttu-id="873a1-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)</span><span class="sxs-lookup"><span data-stu-id="873a1-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Access to WMI Namespaces](access-to-wmi-namespaces.md)</span></span>
</dt> <dd>

<span data-ttu-id="873a1-109">La sicurezza dello spazio dei nomi WMI si basa sugli [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) degli utenti di Windows standard e sugli elenchi di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="873a1-109">WMI namespace security relies on standard Windows user [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) and access control lists.</span></span> <span data-ttu-id="873a1-110">Gli amministratori e gli utenti dispongono di autorizzazioni predefinite diverse.</span><span class="sxs-lookup"><span data-stu-id="873a1-110">Administrators and users have different default permissions.</span></span>

</dd> <dt>

<span data-ttu-id="873a1-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Impostazione di descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="873a1-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md)</span></span>
</dt> <dd>

<span data-ttu-id="873a1-112">Quando uno spazio dei nomi è presente nel repository WMI, è possibile modificare la sicurezza sullo spazio dei nomi utilizzando il controllo WMI o chiamando i metodi di [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="873a1-112">After a namespace exists in the WMI repository, you can change the security on the namespace by using the WMI Control or by calling the methods of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="873a1-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="873a1-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="873a1-114">Il qualificatore **RequiresEncryption** in uno spazio dei nomi richiede che lo script o l'applicazione client WMI usi il livello di autenticazione che crittografa le chiamate di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="873a1-114">The **RequiresEncryption** qualifier on a namespace requires the WMI client application or script to use the authentication level which encrypts remote procedure calls.</span></span> <span data-ttu-id="873a1-115">È necessario crittografare le richieste di dati in ingresso e i callback asincroni.</span><span class="sxs-lookup"><span data-stu-id="873a1-115">Both incoming data requests and asynchronous callbacks must be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="873a1-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Definizione dell'ereditarietà della sicurezza dello spazio dei nomi](establishing-inheritance-of-namespace-security.md)</span><span class="sxs-lookup"><span data-stu-id="873a1-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establishing Inheritance of Namespace Security](establishing-inheritance-of-namespace-security.md)</span></span>
</dt> <dd>

<span data-ttu-id="873a1-117">È possibile controllare se uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre.</span><span class="sxs-lookup"><span data-stu-id="873a1-117">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="873a1-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="873a1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="873a1-119">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="873a1-119">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="873a1-120">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="873a1-120">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="873a1-121">Creazione di uno spazio dei nomi con l'API WMI</span><span class="sxs-lookup"><span data-stu-id="873a1-121">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[<span data-ttu-id="873a1-122">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="873a1-122">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
