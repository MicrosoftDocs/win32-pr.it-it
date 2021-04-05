---
title: Ricerca di oggetti
description: Julie Bankert deve trovare i numeri di telefono per tutti i Program Manager che lavorano nel reparto 101. Per eseguire questa operazione, è possibile creare uno script che usa ADO e ADSI.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- ricerca di oggetti ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103858041"
---
# <a name="searching-for-objects"></a><span data-ttu-id="a4e14-105">Ricerca di oggetti</span><span class="sxs-lookup"><span data-stu-id="a4e14-105">Searching for Objects</span></span>

<span data-ttu-id="a4e14-106">Julie Bankert deve trovare i numeri di telefono per tutti i Program Manager che lavorano nel reparto 101.</span><span class="sxs-lookup"><span data-stu-id="a4e14-106">Julie Bankert must find telephone numbers for all Program Managers who work in Department 101.</span></span> <span data-ttu-id="a4e14-107">Per eseguire questa operazione, è possibile creare uno script che usa ADO e ADSI.</span><span class="sxs-lookup"><span data-stu-id="a4e14-107">She can create a script that uses ADO and ADSI to accomplish this.</span></span>

<span data-ttu-id="a4e14-108">Quando si utilizza il provider ADO per eseguire una query, il set di risultati restituirà solo i primi 1000 oggetti.</span><span class="sxs-lookup"><span data-stu-id="a4e14-108">When using the ADO provider to perform a query, the result set will only return the first 1000 objects.</span></span> <span data-ttu-id="a4e14-109">Per questo motivo, è importante usare una query di paging per poter recuperare tutti gli oggetti nel set di risultati, purché il servizio directory non sia stato impostato per limitare il numero di elementi in un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="a4e14-109">For this reason, it is important to use a paged query so that you can retrieve all of the objects in the result set, as long as the directory service has not been set to limit the number of items in a result set.</span></span> <span data-ttu-id="a4e14-110">I set restituiti conterranno il numero di elementi specificati nelle dimensioni della pagina e i set di paging continueranno a essere restituiti finché non verranno restituiti tutti gli elementi del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="a4e14-110">Return sets will contain the number of items that you specify in the page size, and paged sets will continue to be returned until all items in the result set have been returned.</span></span>


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



<span data-ttu-id="a4e14-111">Per eseguire una ricerca ADSI in Visual Basic o in un ambiente di scripting, sono necessari tre componenti ADO, ovvero **connessione**, **comando** e **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a4e14-111">To perform an ADSI search in Visual Basic or a scripting environment, three ADO components are required: **Connection**, **Command**, and **Recordset**.</span></span> <span data-ttu-id="a4e14-112">L'oggetto **Connection** consente di specificare il nome del provider, le credenziali alternative, se applicabile, e altri flag.</span><span class="sxs-lookup"><span data-stu-id="a4e14-112">The **Connection** object enables you to specify the provider name, alternate credentials, if applicable, and other flags.</span></span> <span data-ttu-id="a4e14-113">L'oggetto **Command** consente di specificare le preferenze di ricerca e la stringa di query.</span><span class="sxs-lookup"><span data-stu-id="a4e14-113">The **Command** object enables you to specify search preferences and the query string.</span></span> <span data-ttu-id="a4e14-114">È necessario associare l'oggetto **connessione** a un oggetto **comando** prima dell'esecuzione della query.</span><span class="sxs-lookup"><span data-stu-id="a4e14-114">You must associate the **Connection** object to a **Command** object before the execution of the query.</span></span> <span data-ttu-id="a4e14-115">Infine, viene utilizzato l'oggetto **Recordset** per scorrere il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="a4e14-115">Finally, the **Recordset** object is used to iterate the result set.</span></span>

<span data-ttu-id="a4e14-116">ADSI supporta due tipi di stringhe di query o dialetti.</span><span class="sxs-lookup"><span data-stu-id="a4e14-116">ADSI supports two types of query strings or dialects.</span></span> <span data-ttu-id="a4e14-117">Nell'esempio di codice precedente viene usato il sottolinguaggio SQL.</span><span class="sxs-lookup"><span data-stu-id="a4e14-117">The preceding code example uses the SQL dialect.</span></span> <span data-ttu-id="a4e14-118">È anche possibile usare il dialetto LDAP.</span><span class="sxs-lookup"><span data-stu-id="a4e14-118">You can also use the LDAP dialect.</span></span> <span data-ttu-id="a4e14-119">La stringa di query del dialetto LDAP è basata su [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (un documento RFC è una richiesta di commenti, che costituisce la base per lo sviluppo di standard LDAP).</span><span class="sxs-lookup"><span data-stu-id="a4e14-119">The LDAP dialect query string is based on [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (an RFC is a Request For Comments document, which is the basis for developing LDAP standards).</span></span> <span data-ttu-id="a4e14-120">L'esempio precedente può essere convertito nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="a4e14-120">The preceding example can be translated to the following code example.</span></span>


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



<span data-ttu-id="a4e14-121">Perché la parola "subtree" è alla fine della stringa?</span><span class="sxs-lookup"><span data-stu-id="a4e14-121">Why is the word "subtree" at the end of the string?</span></span> <span data-ttu-id="a4e14-122">Nel mondo della directory è possibile specificare l'ambito di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a4e14-122">In the directory world, you can specify the scope of search.</span></span> <span data-ttu-id="a4e14-123">Le scelte disponibili sono: "base", "unlivello" e "sottoalbero".</span><span class="sxs-lookup"><span data-stu-id="a4e14-123">The choices are: "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="a4e14-124">"base" viene usato per leggere l'oggetto stesso; "unlivello" si riferisce agli elementi figlio immediati, in modo analogo al comando **dir** ; il "sottoalbero" viene usato per eseguire ricerche in più livelli (in modo analogo a **dir/s**).</span><span class="sxs-lookup"><span data-stu-id="a4e14-124">"base" is used to read the object itself; "onelevel" refers to the immediate children, similar to the **dir** command; "subtree" is used to search deep or down multiple levels (similar to **dir /s**).</span></span>

<span data-ttu-id="a4e14-125">Con il sottolinguaggio SQL, è possibile specificare l'ambito nella proprietà Command, ad esempio nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="a4e14-125">With the SQL dialect, you can specify scope in the command property, such as in the following code example.</span></span>


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



<span data-ttu-id="a4e14-126">Se l'ambito non è specificato, per impostazione predefinita viene usata la ricerca del sottoalbero.</span><span class="sxs-lookup"><span data-stu-id="a4e14-126">If scope is not specified, by default it uses a subtree search.</span></span>

> [!Note]  
> <span data-ttu-id="a4e14-127">Se si usa C++, è possibile usare l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) di ADSI.</span><span class="sxs-lookup"><span data-stu-id="a4e14-127">If you use C++, you can use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface from ADSI.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a4e14-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4e14-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4e14-129">Riorganizzazione</span><span class="sxs-lookup"><span data-stu-id="a4e14-129">Reorganization</span></span>](reorganization.md)
</dt> </dl>

 

 




