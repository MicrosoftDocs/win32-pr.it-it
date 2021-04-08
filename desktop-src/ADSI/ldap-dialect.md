---
title: Dialetto LDAP
description: Il dialetto LDAP è un formato per le istruzioni di query che usano la sintassi del filtro di ricerca LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- ADSI dialetto LDAP
- dialetti ADSI, dialetto LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855289"
---
# <a name="ldap-dialect"></a><span data-ttu-id="4837d-105">Dialetto LDAP</span><span class="sxs-lookup"><span data-stu-id="4837d-105">LDAP Dialect</span></span>

<span data-ttu-id="4837d-106">Il dialetto LDAP è un formato per le istruzioni di query che usano la [sintassi del filtro di ricerca LDAP](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="4837d-106">The LDAP dialect is a format for query statements that use the [LDAP search filter syntax](search-filter-syntax.md).</span></span> <span data-ttu-id="4837d-107">Usare un'istruzione di query LDAP con le interfacce di ricerca ADSI seguenti:</span><span class="sxs-lookup"><span data-stu-id="4837d-107">Use an LDAP query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="4837d-108">Le interfacce [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , ovvero interfacce di automazione che utilizzano OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4837d-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="4837d-109">[OLE DB](searching-with-ole-db.md), ovvero un set di interfacce C/C++ per l'esecuzione di query sui database.</span><span class="sxs-lookup"><span data-stu-id="4837d-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>
-   <span data-ttu-id="4837d-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), ovvero l'interfaccia C/C++ per Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4837d-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), which is the C/C++ interface for Active Directory.</span></span>

<span data-ttu-id="4837d-111">Una stringa di dialetto LDAP è costituita da quattro parti separate da punti e virgola (;).</span><span class="sxs-lookup"><span data-stu-id="4837d-111">An LDAP dialect string consists of four parts separated by semicolons (;).</span></span>

-   <span data-ttu-id="4837d-112">Nome distinto di base.</span><span class="sxs-lookup"><span data-stu-id="4837d-112">Base distinguished name.</span></span> <span data-ttu-id="4837d-113">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4837d-113">For example:</span></span>

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   <span data-ttu-id="4837d-114">Filtri di ricerca LDAP.</span><span class="sxs-lookup"><span data-stu-id="4837d-114">LDAP search filters.</span></span> <span data-ttu-id="4837d-115">Per altre informazioni sui filtri di ricerca, vedere [sintassi del filtro di ricerca](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="4837d-115">For more information about search filters, see [Search Filter Syntax](search-filter-syntax.md).</span></span>
-   <span data-ttu-id="4837d-116">Nome visualizzato LDAP degli attributi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="4837d-116">The LDAP display name of the attributes to retrieve.</span></span> <span data-ttu-id="4837d-117">Più attributi sono separati da una virgola.</span><span class="sxs-lookup"><span data-stu-id="4837d-117">Multiple attributes are separated by a comma.</span></span>
-   <span data-ttu-id="4837d-118">Specifica l'ambito della ricerca.</span><span class="sxs-lookup"><span data-stu-id="4837d-118">Specifies the scope of the search.</span></span> <span data-ttu-id="4837d-119">I valori validi sono "base", "unlivello" e "sottoalbero".</span><span class="sxs-lookup"><span data-stu-id="4837d-119">Valid values are "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="4837d-120">L'ambito specificato in una stringa di query LDAP sostituisce qualsiasi ambito di ricerca specificato con la proprietà "SearchScope" dell'oggetto comando ADO.</span><span class="sxs-lookup"><span data-stu-id="4837d-120">The scope specified in an LDAP query string overrides any search scope specified with the "SearchScope" property of the ADO Command object.</span></span>

<span data-ttu-id="4837d-121">Di seguito è riportato un esempio di codice del dialetto LDAP in ADSI che cerca tutti gli oggetti nel sottoalbero.</span><span class="sxs-lookup"><span data-stu-id="4837d-121">The following is a code example of the LDAP dialect in ADSI that searches all the objects in the subtree.</span></span>


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



<span data-ttu-id="4837d-122">Non tutte le opzioni di ricerca (ad esempio, le dimensioni della pagina di ricerca) possono essere espresse nel dialetto LDAP, quindi è necessario impostare le opzioni prima che l'esecuzione effettiva della query venga avviata.</span><span class="sxs-lookup"><span data-stu-id="4837d-122">Not all search options (search page size, for example) can be expressed in the LDAP dialect, so you must set the options before the actual query execution starts.</span></span>

## <a name="example-code-for-performing-an-ldap-query"></a><span data-ttu-id="4837d-123">Codice di esempio per l'esecuzione di una query LDAP</span><span class="sxs-lookup"><span data-stu-id="4837d-123">Example Code for Performing an LDAP Query</span></span>

<span data-ttu-id="4837d-124">Nell'esempio di codice seguente viene illustrato come utilizzare una query LDAP</span><span class="sxs-lookup"><span data-stu-id="4837d-124">The following code example shows how to use an LDAP query</span></span>


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



<span data-ttu-id="4837d-125">Per informazioni dettagliate sulla sintassi di query, vedere [sintassi del filtro di ricerca](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="4837d-125">For details about the query syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4837d-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4837d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4837d-127">Sintassi del filtro di ricerca</span><span class="sxs-lookup"><span data-stu-id="4837d-127">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="4837d-128">Sottolinguaggio SQL</span><span class="sxs-lookup"><span data-stu-id="4837d-128">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="4837d-129">Ricerca con l'interfaccia IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="4837d-129">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="4837d-130">Ricerca con ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="4837d-130">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="4837d-131">Ricerca con OLE DB</span><span class="sxs-lookup"><span data-stu-id="4837d-131">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




