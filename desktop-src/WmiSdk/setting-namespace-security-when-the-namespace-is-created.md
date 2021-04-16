---
title: Impostazione della sicurezza per la creazione dello spazio dei nomi
description: Il file di Managed Object Format (MOF) che crea uno spazio dei nomi può anche definire i descrittori di sicurezza per lo spazio dei nomi includendo il qualificatore NamespaceSecuritySDDL con il descrittore di sicurezza in formato SDDL (Security Descriptor Definition Language).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530138"
---
# <a name="setting-security-on-namespace-creation"></a><span data-ttu-id="70525-103">Impostazione della sicurezza per la creazione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70525-103">Setting security on namespace creation</span></span>

<span data-ttu-id="70525-104">Il file di Managed Object Format (MOF) che crea uno spazio dei nomi può anche definire i [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly) per lo spazio dei nomi includendo il qualificatore **NamespaceSecuritySDDL** con il descrittore di sicurezza in formato [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="70525-104">The Managed Object Format (MOF) file that creates a namespace can also define the [*security descriptors*](/windows/desktop/SecGloss/s-gly) for the namespace by including the **NamespaceSecuritySDDL** qualifier with the security descriptor in [security descriptor definition language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span>

<span data-ttu-id="70525-105">È possibile usare **NamespaceSecuritySDDL** per proteggere qualsiasi spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="70525-105">You can use **NamespaceSecuritySDDL** to secure any namespace.</span></span> <span data-ttu-id="70525-106">È inoltre possibile utilizzare questo qualificatore in un semplice file MOF per modificare il descrittore di sicurezza in uno spazio dei nomi esistente.</span><span class="sxs-lookup"><span data-stu-id="70525-106">You can also use this qualifier in a simple MOF file to alter the security descriptor on an existing namespace.</span></span> <span data-ttu-id="70525-107">La stringa SDDL viene elaborata da WMI per stabilire la sicurezza dello spazio dei nomi, ma non viene archiviata come stringa.</span><span class="sxs-lookup"><span data-stu-id="70525-107">The SDDL string is processed by WMI to establish the namespace security but is not stored as a string.</span></span> <span data-ttu-id="70525-108">Se non viene specificato alcun descrittore di sicurezza, viene utilizzata la sicurezza predefinita.</span><span class="sxs-lookup"><span data-stu-id="70525-108">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="70525-109">Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="70525-109">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="70525-110">La procedura seguente consente di impostare il descrittore di sicurezza per lo spazio dei nomi MyNamespace *radice \\* .</span><span class="sxs-lookup"><span data-stu-id="70525-110">The following procedure sets the security descriptor for the *root\\MyNamespace* namespace.</span></span> <span data-ttu-id="70525-111">La stringa SDDL imposta il proprietario e il gruppo sugli utenti autenticati e specifica un [*elenco di controllo di accesso discrezionale (DACL)*](/windows/desktop/SecGloss/d-gly) ereditato dagli spazi dei nomi figlio.</span><span class="sxs-lookup"><span data-stu-id="70525-111">The SDDL string sets the owner and group to authenticated users and specifies a [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) that is inherited by child namespaces.</span></span> <span data-ttu-id="70525-112">L'elenco DACL consente all'utente di leggere i dati, eseguire metodi, scrivere dati nelle classi del provider e utilizzare accesso remoto **: \_ Abilita WBEM**, **\_ Metodo WBEM \_ Execute**, **\_ \_ provider di scrittura WBEM**, **\_ \_ accesso remoto WBEM**.</span><span class="sxs-lookup"><span data-stu-id="70525-112">The DACL allows the user the right to read data, execute methods, write data to provider classes and use remote access: **WBEM\_ENABLE**, **WBEM\_METHOD\_EXECUTE**, **WBEM\_WRITE\_PROVIDER**, **WBEM\_REMOTE\_ACCESS**.</span></span> <span data-ttu-id="70525-113">Per ulteriori informazioni, vedere [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="70525-113">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="70525-114">**Per impostare un DACL dello spazio dei nomi**</span><span class="sxs-lookup"><span data-stu-id="70525-114">**To set a namespace DACL**</span></span>

1.  <span data-ttu-id="70525-115">Creare un file di Managed Object Format (MOF) o modificare il file MOF esistente che definisce lo spazio dei nomi per aggiungere il qualificatore **NamespaceSecuritySDDL** con la stringa SDDL.</span><span class="sxs-lookup"><span data-stu-id="70525-115">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace to add the **NamespaceSecuritySDDL** qualifier with the SDDL string.</span></span>

    <span data-ttu-id="70525-116">L'esempio di codice seguente mostra che lo spazio dei nomi da modificare è radice \\ MyNamespace e il file è denominato MyNamespace \_ Security. mof.</span><span class="sxs-lookup"><span data-stu-id="70525-116">The following code example shows the namespace to be modified is root\\MyNamespace and the file is named MyNamespace\_security.mof.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  <span data-ttu-id="70525-117">Tenere presente che la stringa SDDL distingue tra maiuscole e minuscole: le lettere devono essere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="70525-117">Be aware that the SDDL string is case-sensitive: the letters must be capitalized.</span></span>

    <span data-ttu-id="70525-118">Nell'esempio di codice riportato di seguito vengono illustrate le lettere "o" e "g" nella stringa SDDL come minuscole e la Mofcomp.exe restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="70525-118">The following code example shows the letters "o" and "g" in the SDDL string as lowercase and will cause Mofcomp.exe to return an error.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  <span data-ttu-id="70525-119">Eseguire [**Mofcomp.exe**](mofcomp.md) per compilare il file MOF.</span><span class="sxs-lookup"><span data-stu-id="70525-119">Run [**Mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="70525-120">**c: \\ mofcomp MyNamespace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="70525-120">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="70525-121">In C++ usare i metodi [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="70525-121">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

4.  <span data-ttu-id="70525-122">Se il tentativo di impostare l'elenco DACL dello spazio dei nomi ha esito negativo, considerare i messaggi di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="70525-122">If your attempt to set the namespace DACL fails, consider the following error messages:</span></span>

    

    | <span data-ttu-id="70525-123">Errore</span><span class="sxs-lookup"><span data-stu-id="70525-123">Error</span></span>                           | <span data-ttu-id="70525-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70525-124">Description</span></span>                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="70525-125">**\_parametro WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="70525-125">**WBEM\_E\_INVALID\_PARAMETER**</span></span> | <span data-ttu-id="70525-126">Non esiste alcun DACL ereditato.</span><span class="sxs-lookup"><span data-stu-id="70525-126">There is no inherited DACL.</span></span> <span data-ttu-id="70525-127">In alternativa, il chiamante ha violato il DACL o la SD nello spazio dei nomi padre.</span><span class="sxs-lookup"><span data-stu-id="70525-127">Alternately, the caller has violated the DACL or the SD in the parent namespace.</span></span> |
    | <span data-ttu-id="70525-128">**accesso a WBEM \_ E \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="70525-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>     | <span data-ttu-id="70525-129">Il chiamante non dispone dell'autorizzazione per aggiornare SDDL in MOF.</span><span class="sxs-lookup"><span data-stu-id="70525-129">The caller does not have permission to update the SDDL in MOF.</span></span>                                               |

    

     

## <a name="related-topics"></a><span data-ttu-id="70525-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70525-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70525-131">Impostazione di descrittori di sicurezza dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70525-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="70525-132">**Costanti dei diritti di accesso allo spazio dei nomi**</span><span class="sxs-lookup"><span data-stu-id="70525-132">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
</dt> <dt>

[<span data-ttu-id="70525-133">**Costanti del flag ACE dello spazio dei nomi**</span><span class="sxs-lookup"><span data-stu-id="70525-133">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
</dt> <dt>

[<span data-ttu-id="70525-134">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="70525-134">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
