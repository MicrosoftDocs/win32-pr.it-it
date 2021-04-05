---
title: Associazione al catalogo globale
description: Il catalogo globale è uno spazio dei nomi che contiene i dati di directory per tutti i domini in una foresta.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Associazione al catalogo globale AD
- ANNUNCIO globale del catalogo, associazione a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046555"
---
# <a name="binding-to-the-global-catalog"></a><span data-ttu-id="fada0-105">Associazione al catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fada0-105">Binding to the Global Catalog</span></span>

<span data-ttu-id="fada0-106">Il catalogo globale è uno spazio dei nomi che contiene i dati di directory per tutti i domini in una foresta.</span><span class="sxs-lookup"><span data-stu-id="fada0-106">The Global Catalog is a namespace that contains directory data for all domains in a forest.</span></span> <span data-ttu-id="fada0-107">Il catalogo globale contiene una replica parziale di ogni directory di dominio.</span><span class="sxs-lookup"><span data-stu-id="fada0-107">The Global Catalog contains a partial replica of every domain directory.</span></span> <span data-ttu-id="fada0-108">Contiene una voce per ogni oggetto nella foresta aziendale, ma non contiene tutte le proprietà di ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="fada0-108">It contains an entry for every object in the enterprise forest, but does not contain all the properties of each object.</span></span> <span data-ttu-id="fada0-109">Contiene invece solo le proprietà specificate per l'inclusione nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="fada0-109">Instead, it contains only the properties specified for inclusion in the Global Catalog.</span></span>

<span data-ttu-id="fada0-110">Il catalogo globale viene archiviato in server specifici nell'intera organizzazione.</span><span class="sxs-lookup"><span data-stu-id="fada0-110">The Global Catalog is stored on specific servers throughout the enterprise.</span></span> <span data-ttu-id="fada0-111">Solo i controller di dominio possono fungere da server di catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="fada0-111">Only domain controllers can serve as Global Catalog servers.</span></span> <span data-ttu-id="fada0-112">Gli amministratori indicano se un determinato controller di dominio dispone di un catalogo globale usando il Active Directory gestione siti e servizi.</span><span class="sxs-lookup"><span data-stu-id="fada0-112">Administrators indicate whether a given domain controller holds a Global Catalog by using the Active Directory Sites and Services Manager.</span></span>

<span data-ttu-id="fada0-113">Per eseguire l'associazione al catalogo globale con ADSI, usare il moniker "GC:".</span><span class="sxs-lookup"><span data-stu-id="fada0-113">To bind to the Global Catalog with ADSI, use the "GC:" moniker.</span></span>

<span data-ttu-id="fada0-114">Esistono due modi per eseguire l'associazione al catalogo globale per eseguire una ricerca in una foresta:</span><span class="sxs-lookup"><span data-stu-id="fada0-114">There are two ways to bind to the Global Catalog to perform a search in a forest:</span></span>

-   <span data-ttu-id="fada0-115">Eseguire l'associazione all'oggetto radice aziendale per eseguire la ricerca in tutti i domini della foresta.</span><span class="sxs-lookup"><span data-stu-id="fada0-115">Bind to the enterprise root object to search across all domains in the forest.</span></span>
-   <span data-ttu-id="fada0-116">Eseguire l'associazione a un oggetto specifico per eseguire la ricerca dell'oggetto e dei relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="fada0-116">Bind to a specific object to search that object and its children.</span></span> <span data-ttu-id="fada0-117">Se ad esempio si esegue l'associazione a un dominio con due domini sotto di esso in un albero di dominio nella foresta, è possibile eseguire ricerche in questi tre domini.</span><span class="sxs-lookup"><span data-stu-id="fada0-117">For example, if you bind to a domain that has two domains beneath it in a domain tree in the forest, you can search across those three domains.</span></span> <span data-ttu-id="fada0-118">Tenere presente che il nome distinto dell'oggetto a cui eseguire l'associazione è identico a quello del nome distinto utilizzato per l'associazione allo spazio dei nomi "LDAP:".</span><span class="sxs-lookup"><span data-stu-id="fada0-118">Be aware that the distinguished name for the object to bind to is exactly the same as the distinguished name used to bind to the "LDAP:" namespace.</span></span> <span data-ttu-id="fada0-119">Si ricordi che "LDAP:" è una replica completa di un singolo dominio e che "GC:" è una replica parziale di tutti i domini della foresta.</span><span class="sxs-lookup"><span data-stu-id="fada0-119">Recall that "LDAP:" is a full replica of a single domain and that "GC:" is a partial replica of all domains in the forest.</span></span>

<span data-ttu-id="fada0-120">Come per il moniker "LDAP:", è possibile usare il binding senza server o eseguire il binding a un server di catalogo globale specifico.</span><span class="sxs-lookup"><span data-stu-id="fada0-120">As with the "LDAP:" moniker, you can use serverless binding or bind to a specific Global Catalog server.</span></span> <span data-ttu-id="fada0-121">Se si esegue la ricerca nella foresta corrente, utilizzare un'associazione senza server.</span><span class="sxs-lookup"><span data-stu-id="fada0-121">If searching in the current forest, use serverless binding.</span></span> <span data-ttu-id="fada0-122">Tuttavia, se si esegue la ricerca in un'altra foresta, specificare un nome di dominio o un server di catalogo globale a cui eseguire l'associazione, come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="fada0-122">However, if searching in another forest, specify either a domain name or a Global Catalog server to bind to, such as shown in the following examples.</span></span>

<span data-ttu-id="fada0-123">Associa usando il nome di dominio:</span><span class="sxs-lookup"><span data-stu-id="fada0-123">Bind using the domain name:</span></span>

``` syntax
GC://fabrikam.com
```

<span data-ttu-id="fada0-124">Associa utilizzando il nome del server:</span><span class="sxs-lookup"><span data-stu-id="fada0-124">Bind using the server name:</span></span>

``` syntax
GC://servername
```

<span data-ttu-id="fada0-125">È anche possibile eseguire l'associazione a un oggetto specifico all'interno del catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="fada0-125">You can also bind to a specific object within the Global Catalog.</span></span> <span data-ttu-id="fada0-126">Per eseguire l'associazione all'oggetto Sales nel dominio fabrikam, utilizzare il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="fada0-126">To bind to the sales object in the fabrikam domain, use the following format.</span></span>

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="fada0-127">In alternativa, per eseguire l'associazione all'oggetto Sales nel server, utilizzare il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="fada0-127">Or, to bind to the sales object on the server, use the following format.</span></span>

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="fada0-128">**Per eseguire una ricerca nell'intera foresta**</span><span class="sxs-lookup"><span data-stu-id="fada0-128">**To search the entire forest**</span></span>

1.  <span data-ttu-id="fada0-129">Associare alla radice dello spazio dei nomi del catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="fada0-129">Bind to the root of the Global Catalog namespace.</span></span>
2.  <span data-ttu-id="fada0-130">Enumerare il contenitore del catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="fada0-130">Enumerate the Global Catalog container.</span></span> <span data-ttu-id="fada0-131">Il contenitore catalogo globale contiene un singolo oggetto che è possibile usare per eseguire ricerche nell'intera foresta.</span><span class="sxs-lookup"><span data-stu-id="fada0-131">The Global Catalog container contains a single object that you can use to search the entire forest.</span></span>
3.  <span data-ttu-id="fada0-132">Usare l'oggetto nel contenitore per eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="fada0-132">Use the object in the container to perform the search.</span></span> <span data-ttu-id="fada0-133">In C/C++ chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) sull'oggetto in modo da poter usare l'interfaccia **IDirectorySearch** per eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="fada0-133">In C/C++, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer on the object so that you can use the **IDirectorySearch** interface to perform the search.</span></span> <span data-ttu-id="fada0-134">In Visual Basic usare l'oggetto restituito dall'enumerazione nella query ADO.</span><span class="sxs-lookup"><span data-stu-id="fada0-134">In Visual Basic, use the object returned from the enumeration in your ADO query.</span></span>

<span data-ttu-id="fada0-135">Per enumerare i server di catalogo globale in un sito, eseguire una ricerca di sottoalbero LDAP di "CN = <yoursite> , CN = Sites <DN of the configurationNamingContext> ", usando la stringa di filtro seguente.</span><span class="sxs-lookup"><span data-stu-id="fada0-135">To enumerate the Global Catalog servers in a site, perform an LDAP subtree search of "cn=<yoursite>,cn=sites,<DN of the configurationNamingContext>", using the following filter string.</span></span>

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

<span data-ttu-id="fada0-136">Questo filtro usa il **bit della regola di corrispondenza LDAP \_ \_ \_ \_ e** l'operatore di regola di corrispondenza (1.2.840.113556.1.4.803) per trovare gli oggetti **NTDSDSA** con il bit di ordine inferiore impostato nella maschera di bit dell'attributo **options** .</span><span class="sxs-lookup"><span data-stu-id="fada0-136">This filter uses the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator (1.2.840.113556.1.4.803) to find **nTDSDSA** objects that have the low-order bit set in the bitmask of the **options** attribute.</span></span> <span data-ttu-id="fada0-137">Il bit di ordine inferiore, che corrisponde a **NTDSDSA \_ opt \_ è \_** la costante GC definita in ntdsapi. h, identifica l'oggetto **NTDSDSA** di un server di catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="fada0-137">The low-order bit, which corresponds to the **NTDSDSA\_OPT\_IS\_GC** constant defined in Ntdsapi.h, identifies the **nTDSDSA** object of a Global Catalog server.</span></span> <span data-ttu-id="fada0-138">Per altre informazioni sulle regole di corrispondenza, vedere [sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="fada0-138">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="fada0-139">L'elemento padre dell'oggetto **NTDSDSA** è l'oggetto server e la proprietà **dNSHostName** dell'oggetto server è il nome DNS del server di catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="fada0-139">The parent of the **nTDSDSA** object is the server object, and the **dNSHostName** property of the server object is the DNS name of the Global Catalog server.</span></span>

<span data-ttu-id="fada0-140">Non è possibile usare \# le costanti define, ad esempio **NTDSDSA \_ opz \_ è \_** un bit della regola di corrispondenza GC e **LDAP \_ \_ \_ \_ e** direttamente in una stringa di filtro di ricerca.</span><span class="sxs-lookup"><span data-stu-id="fada0-140">You cannot use \#define constants such as **NTDSDSA\_OPT\_IS\_GC** and **LDAP\_MATCHING\_RULE\_BIT\_AND** directly in a search filter string.</span></span> <span data-ttu-id="fada0-141">Tuttavia, è possibile usare queste costanti come argomenti per una funzione, ad esempio [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) , per inserire i valori costanti in una stringa di filtro.</span><span class="sxs-lookup"><span data-stu-id="fada0-141">However, you could use these constants as arguments to a function such as [**swprintf\_s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) to insert the constant values into a filter string.</span></span>

<span data-ttu-id="fada0-142">Il catalogo globale non rappresenta l'intera struttura ad albero della foresta.</span><span class="sxs-lookup"><span data-stu-id="fada0-142">The global catalog does not represent the entire forest tree structure.</span></span> <span data-ttu-id="fada0-143">Si supponga, ad esempio, che l'esempio di codice seguente enumera tutti i domini della foresta e tutti gli oggetti figlio di ogni dominio.</span><span class="sxs-lookup"><span data-stu-id="fada0-143">For example, you might expect that the following code example would enumerate all of the domains in the forest and all child objects of each domain.</span></span> <span data-ttu-id="fada0-144">In realtà, ciò che realmente fa è enumerare tutti i domini della foresta, ma nessuno degli oggetti di dominio enumerati contiene elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="fada0-144">In reality, what it actually does is enumerate all of the domains in the forest, but none of the enumerated domain objects contain any children.</span></span> <span data-ttu-id="fada0-145">Si tratta di una limitazione del catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="fada0-145">This is a limitation of the global catalog.</span></span>


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="fada0-146">Per risolvere il problema, è necessario eseguire l'associazione a ogni oggetto di dominio e quindi enumerare gli oggetti figlio di ogni dominio.</span><span class="sxs-lookup"><span data-stu-id="fada0-146">To correct this, it is necessary to bind to each domain object and then enumerate the child objects of each domain.</span></span> <span data-ttu-id="fada0-147">La tecnica corretta è illustrata nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="fada0-147">The proper technique is shown in the following code example.</span></span>


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="fada0-148">Per ulteriori informazioni ed esempi di codice che illustrano come eseguire la ricerca in un'intera foresta, vedere [il codice di esempio per la ricerca in una foresta](example-code-for-searching-a-forest.md).</span><span class="sxs-lookup"><span data-stu-id="fada0-148">For more information and code examples that show how to search an entire forest, see [Example Code for Searching a Forest](example-code-for-searching-a-forest.md).</span></span>

 

 