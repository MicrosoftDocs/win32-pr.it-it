---
title: Stringa di binding
description: A causa del numero di oggetti accessibili da un servizio directory, possono verificarsi conflitti di denominazione.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- ADSI stringa di binding
- ADsPath ADSI, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963448"
---
# <a name="binding-string"></a><span data-ttu-id="cb251-105">Stringa di binding</span><span class="sxs-lookup"><span data-stu-id="cb251-105">Binding String</span></span>

<span data-ttu-id="cb251-106">A causa del numero di oggetti accessibili da un servizio directory, possono verificarsi conflitti di denominazione.</span><span class="sxs-lookup"><span data-stu-id="cb251-106">Due to the number of objects accessible from a directory service, naming collisions can occur.</span></span> <span data-ttu-id="cb251-107">La stringa di associazione, nota in genere come ADsPath, consente di specificare un oggetto particolare senza causare un conflitto di denominazione.</span><span class="sxs-lookup"><span data-stu-id="cb251-107">The binding string, which is commonly referred to as the ADsPath, enables you to specify a particular object without causing a naming collision.</span></span> <span data-ttu-id="cb251-108">Questo può essere applicato per un singolo provider di servizi directory o per più provider di servizi di directory.</span><span class="sxs-lookup"><span data-stu-id="cb251-108">This can be applied for a single directory service provider or across multiple directory service providers.</span></span>

<span data-ttu-id="cb251-109">Un ADsPath è una stringa che identifica in modo univoco un oggetto ADSI in un servizio directory.</span><span class="sxs-lookup"><span data-stu-id="cb251-109">An ADsPath is a string that uniquely identifies an ADSI object on a directory service.</span></span> <span data-ttu-id="cb251-110">Poiché gli oggetti ADSI sono presenti nel contesto dello spazio dei nomi del servizio directory sottostante, una parte della sintassi di un nome ADsPath è specifica del provider.</span><span class="sxs-lookup"><span data-stu-id="cb251-110">Because ADSI objects exist within the context of the namespace of the underlying directory service, part of the syntax of an ADsPath name is provider-specific.</span></span>

<span data-ttu-id="cb251-111">Nella tabella seguente sono elencati i provider ADSI forniti per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cb251-111">The following table lists the ADSI providers provided by default.</span></span>



| <span data-ttu-id="cb251-112">Provider</span><span class="sxs-lookup"><span data-stu-id="cb251-112">Provider</span></span>         | <span data-ttu-id="cb251-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb251-113">Description</span></span>                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb251-114">WinNT</span><span class="sxs-lookup"><span data-stu-id="cb251-114">WinNT</span></span><br/> | <span data-ttu-id="cb251-115">Utilizzato per comunicare con i controller di dominio Windows.</span><span class="sxs-lookup"><span data-stu-id="cb251-115">Used to communicate with Windows domain controllers.</span></span> <span data-ttu-id="cb251-116">Per ulteriori informazioni sul ADsPath WinNT, vedere [WinNT ADsPath](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="cb251-116">For more information about the WinNT ADsPath, see [WinNT ADsPath](winnt-adspath.md).</span></span><br/>           |
| <span data-ttu-id="cb251-117">LDAP</span><span class="sxs-lookup"><span data-stu-id="cb251-117">LDAP</span></span><br/>  | <span data-ttu-id="cb251-118">Utilizzato per comunicare con i server LDAP, ad esempio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cb251-118">Used to communicate with LDAP servers, such as Active Directory.</span></span> <span data-ttu-id="cb251-119">Per ulteriori informazioni su LDAP ADsPath, vedere [LDAP ADsPath](ldap-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="cb251-119">For more information about the LDAP ADsPath, see [LDAP ADsPath](ldap-adspath.md).</span></span><br/>  |
| <span data-ttu-id="cb251-120">Annunci</span><span class="sxs-lookup"><span data-stu-id="cb251-120">ADs</span></span><br/>   | <span data-ttu-id="cb251-121">Fornisce un'implementazione di [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) che può essere utilizzata per enumerare tutti i provider ADSI installati nel client.</span><span class="sxs-lookup"><span data-stu-id="cb251-121">Provides an [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) implementation that can be used to enumerate all of the ADSI providers installed on the client.</span></span><br/> |



 

<span data-ttu-id="cb251-122">Usare questi nomi di provider per accedere allo spazio dei nomi del provider predefinito.</span><span class="sxs-lookup"><span data-stu-id="cb251-122">Use these provider names to access the default provider namespace.</span></span> <span data-ttu-id="cb251-123">Se ad esempio si esegue l'associazione a LDAP, ADSI viene associato a un contenitore che contiene l'oggetto di dominio attualmente connesso.</span><span class="sxs-lookup"><span data-stu-id="cb251-123">For example, if you bind to LDAP, ADSI binds to a container that contains the domain object currently logged on.</span></span> <span data-ttu-id="cb251-124">Se si esegue l'associazione a WinNT, ADSI viene associato a un contenitore che include oggetti correlati a tutti i domini nella rete.</span><span class="sxs-lookup"><span data-stu-id="cb251-124">If you bind to WinNT, ADSI binds to a container that holds objects that correlate to all domains on the network.</span></span>

<span data-ttu-id="cb251-125">Gli elementi iniziali della stringa ADsPath sono l'identificatore a livello di codice (progID) del provider ADSI, seguito da "://", seguito dalla sintassi dettata dallo spazio dei nomi del provider.</span><span class="sxs-lookup"><span data-stu-id="cb251-125">The initial elements of the ADsPath string are the programmatic identifier (progID) of the ADSI provider, followed by "://", followed by syntax dictated by the provider namespace.</span></span> <span data-ttu-id="cb251-126">La stringa progID può o meno fare distinzione tra maiuscole e minuscole, a seconda del provider.</span><span class="sxs-lookup"><span data-stu-id="cb251-126">The progID string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="cb251-127">Le stringhe progID per i provider elencate in precedenza fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cb251-127">The progID strings for the providers listed above are case-sensitive.</span></span>

<span data-ttu-id="cb251-128">La stringa di percorso può o meno fare distinzione tra maiuscole e minuscole, a seconda del provider.</span><span class="sxs-lookup"><span data-stu-id="cb251-128">The path string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="cb251-129">Le stringhe di percorso per i provider elencate sopra non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cb251-129">The path strings for the providers listed above are not case-sensitive.</span></span>

<span data-ttu-id="cb251-130">Di seguito sono riportati alcuni esempi di ADsPaths.</span><span class="sxs-lookup"><span data-stu-id="cb251-130">The following are examples of ADsPaths.</span></span>

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

<span data-ttu-id="cb251-131">Per trovare tutti i provider installati nel computer, eseguire l'associazione al provider ADs come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="cb251-131">To find all providers installed on your computer, bind to the ADs provider as shown in the following code example.</span></span>


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



<span data-ttu-id="cb251-132">Utilizzando il provider LDAP, è possibile specificare il ADsPath in un formato di nome distinto X. 500, a partire dal tag CN, oppure è possibile specificare l'inverso gerarchico, a partire dal tag O.</span><span class="sxs-lookup"><span data-stu-id="cb251-132">Using the LDAP provider, you can specify the ADsPath either in an X.500 distinguished name (DN) form, starting with the CN tag, or you can specify its hierarchical inverse, starting with the O tag.</span></span> <span data-ttu-id="cb251-133">Il form usato nella ADsPath iniziale determina l'ordine dei tag.</span><span class="sxs-lookup"><span data-stu-id="cb251-133">The form you use in the initial ADsPath determines the order of the tags.</span></span>

<span data-ttu-id="cb251-134">Nella tabella seguente sono elencati i caratteri speciali ADsPath.</span><span class="sxs-lookup"><span data-stu-id="cb251-134">The following table lists ADsPath special characters.</span></span>



| <span data-ttu-id="cb251-135">Nome</span><span class="sxs-lookup"><span data-stu-id="cb251-135">Name</span></span>                      | <span data-ttu-id="cb251-136">Carattere</span><span class="sxs-lookup"><span data-stu-id="cb251-136">Character</span></span>           | <span data-ttu-id="cb251-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb251-137">Description</span></span>                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb251-138">Virgoletta doppia</span><span class="sxs-lookup"><span data-stu-id="cb251-138">Double quote</span></span><br/>   | <span data-ttu-id="cb251-139">"</span><span class="sxs-lookup"><span data-stu-id="cb251-139">"</span></span><br/>        | <span data-ttu-id="cb251-140">Usato per citare qualsiasi parte di ADsPath che può contenere un carattere speciale in modo che la stringa venga interpretata letteralmente.</span><span class="sxs-lookup"><span data-stu-id="cb251-140">Used to quote any part of the ADsPath that may contain a special character so that the string is interpreted literally.</span></span> <span data-ttu-id="cb251-141">Ad esempio, "CN = nome/prefisso".</span><span class="sxs-lookup"><span data-stu-id="cb251-141">For example, "CN=Name/Prefix".</span></span><br/>                                     |
| <span data-ttu-id="cb251-142">Barra rovesciata</span><span class="sxs-lookup"><span data-stu-id="cb251-142">Backslash</span></span><br/>      | \\<br/>       | <span data-ttu-id="cb251-143">Usato per precedere i caratteri speciali per indicare che devono essere usati come valori letterali.</span><span class="sxs-lookup"><span data-stu-id="cb251-143">Used to precede special characters to signify they should be used as literals.</span></span> <span data-ttu-id="cb251-144">Per ulteriori informazioni e per un elenco di caratteri speciali, vedere [nomi distinti](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="cb251-144">For more information and a list of special characters, see [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span><br/> |
| <span data-ttu-id="cb251-145">Barra</span><span class="sxs-lookup"><span data-stu-id="cb251-145">Slash</span></span><br/>          | /<br/>        | <span data-ttu-id="cb251-146">Separatore componenti.</span><span class="sxs-lookup"><span data-stu-id="cb251-146">Component separator.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="cb251-147">Parentesi acute</span><span class="sxs-lookup"><span data-stu-id="cb251-147">Angle brackets</span></span><br/> | <><br/> | <span data-ttu-id="cb251-148">Delimitare un ADsPath all'interno di un'altra convenzione di denominazione.</span><span class="sxs-lookup"><span data-stu-id="cb251-148">Delimit an ADsPath within another naming convention.</span></span><br/>                                                                                                                                       |



 

<span data-ttu-id="cb251-149">Per delimitare un ADsPath in una specifica di ricerca o come parte di un URL, utilizzare la parentesi uncinata aperta (< >).</span><span class="sxs-lookup"><span data-stu-id="cb251-149">To delimit an ADsPath in a search specification or as part of a URL, use the left and right angle bracket (< >).</span></span> <span data-ttu-id="cb251-150">Ad esempio, " &lt; WinNT://mydomain/UserAccount &gt; ".</span><span class="sxs-lookup"><span data-stu-id="cb251-150">For example, "&lt;WinNT://MyDomain/UserAccount&gt;".</span></span>

<span data-ttu-id="cb251-151">Alcuni provider ADSI potrebbero avere aggiunto restrizioni di sintassi a causa dei requisiti dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cb251-151">Some ADSI providers may have added syntax restrictions due to namespace requirements.</span></span>

## <a name="active-directory-binding-options"></a><span data-ttu-id="cb251-152">Opzioni di associazione Active Directory</span><span class="sxs-lookup"><span data-stu-id="cb251-152">Active Directory Binding Options</span></span>

<span data-ttu-id="cb251-153">Active Directory fornisce la possibilità di eseguire l'associazione a un oggetto utilizzando diversi altri tipi di stringhe di associazione, ad esempio un identificatore univoco globale (GUID) COM o un ID di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="cb251-153">Active Directory provides the ability to bind to an object using several other types of binding strings, such as a COM globally unique identifier (GUID) or a security identifier (SID).</span></span> <span data-ttu-id="cb251-154">Per ulteriori informazioni, vedere [associazione a Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="cb251-154">For more information, see [Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span></span>

 

