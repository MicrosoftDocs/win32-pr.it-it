---
title: Sottolinguaggio SQL
description: Il sottolinguaggio SQL, derivato dalla Structured Query Language, usa espressioni leggibili per definire istruzioni di query.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- Linguaggio ADSI SQL
- dialetto ADSI, sottolinguaggio SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297648"
---
# <a name="sql-dialect"></a><span data-ttu-id="6f4f1-105">Sottolinguaggio SQL</span><span class="sxs-lookup"><span data-stu-id="6f4f1-105">SQL Dialect</span></span>

<span data-ttu-id="6f4f1-106">Il sottolinguaggio SQL, derivato dalla Structured Query Language, usa espressioni leggibili per definire istruzioni di query.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-106">The SQL dialect, derived from the Structured Query Language, uses human-readable expressions to define query statements.</span></span> <span data-ttu-id="6f4f1-107">Utilizzare un'istruzione di query SQL con le interfacce di ricerca ADSI seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f4f1-107">Use a SQL query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="6f4f1-108">Le interfacce [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , ovvero interfacce di automazione che utilizzano OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="6f4f1-109">[OLE DB](searching-with-ole-db.md), ovvero un set di interfacce C/C++ per l'esecuzione di query sui database.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>

<span data-ttu-id="6f4f1-110">Le istruzioni SQL richiedono la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-110">SQL statements require the following syntax.</span></span>


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



<span data-ttu-id="6f4f1-111">Nella tabella seguente sono elencate le parole chiave dell'istruzione di query SQL.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-111">The following table lists SQL query statement keywords.</span></span>



| <span data-ttu-id="6f4f1-112">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="6f4f1-112">Keyword</span></span>  | <span data-ttu-id="6f4f1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f4f1-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4f1-114">SELECT</span><span class="sxs-lookup"><span data-stu-id="6f4f1-114">SELECT</span></span>   | <span data-ttu-id="6f4f1-115">Specifica un elenco delimitato da virgole di attributi da recuperare per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-115">Specifies a comma-separated list of attributes to retrieve for each object.</span></span> <span data-ttu-id="6f4f1-116">Se si specifica \* , la query recupera solo il ADsPath di ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-116">If you specify \*, the query retrieves only the ADsPath of each object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6f4f1-117">FROM</span><span class="sxs-lookup"><span data-stu-id="6f4f1-117">FROM</span></span>     | <span data-ttu-id="6f4f1-118">Specifica il ADsPath della base della ricerca.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-118">Specifies the ADsPath of the base of the search.</span></span> <span data-ttu-id="6f4f1-119">Ad esempio, il ADsPath del contenitore degli utenti in un dominio Active Directory potrebbe essere ' LDAP://CN = Users, DC = Fabrikam, DC = COM '.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-119">For example, the ADsPath of the Users container in an Active Directory domain might be 'LDAP://CN=Users,DC=Fabrikam,DC=COM'.</span></span> <span data-ttu-id="6f4f1-120">Tenere presente che il percorso è racchiuso tra virgolette singole (').</span><span class="sxs-lookup"><span data-stu-id="6f4f1-120">Be aware that the path is enclosed in a pair of single quotation marks (').</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6f4f1-121">WHERE</span><span class="sxs-lookup"><span data-stu-id="6f4f1-121">WHERE</span></span>    | <span data-ttu-id="6f4f1-122">Parola chiave facoltativa che specifica il filtro per la query.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-122">An optional keyword that specifies the query filter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6f4f1-123">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="6f4f1-123">ORDER BY</span></span> | <span data-ttu-id="6f4f1-124">Parola chiave facoltativa che genera un ordinamento sul lato server se il server supporta il controllo di ordinamento LDAP.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-124">An optional keyword that generates a server-side sort if the server supports the LDAP sort control.</span></span> <span data-ttu-id="6f4f1-125">Active Directory supporta il controllo di ordinamento, ma può influisca sulle prestazioni del server, in particolare se il set di risultati è di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-125">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="6f4f1-126">Sort-list è un elenco delimitato da virgole di attributi su cui eseguire l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-126">The sort-list is a comma-separated list of attributes on which to sort.</span></span> <span data-ttu-id="6f4f1-127">Tenere presente che Active Directory supporta solo una singola chiave di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-127">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="6f4f1-128">È possibile usare le parole chiave ASC e DESC facoltative per specificare l'ordinamento crescente o decrescente. il valore predefinito è Ascending.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-128">You can use the optional ASC and DESC keywords to specify ascending or descending sort order; the default is ascending.</span></span> <span data-ttu-id="6f4f1-129">La parola chiave ORDER BY esegue l'override di qualsiasi chiave di ordinamento specificata con la proprietà "Sort on" dell'oggetto comando ADO.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-129">The ORDER BY keyword overrides any sort key specified with the "Sort on" property of the ADO Command object.</span></span> |



 

> [!Note]  
> <span data-ttu-id="6f4f1-130">Nei casi in cui viene utilizzato un set di caratteri MultiByte, se la ricerca viene eseguita da ADO con il sottolinguaggio SQL, non è possibile utilizzare una barra rovesciata per eseguire il escape dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-130">In cases where a MultiByte Character Set is being used, if the search is performed by ADO with the SQL dialect, then a backslash cannot be used to escape characters.</span></span> <span data-ttu-id="6f4f1-131">Al contrario, è necessario usare le sequenze di escape elencate in [caratteri speciali](search-filter-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="6f4f1-131">Instead, the escape sequences listed in [Special Characters](search-filter-syntax.md) must be used.</span></span> <span data-ttu-id="6f4f1-132">Ad esempio, per un'istruzione che usava la sintassi "samAccountName = \( test", che usa la barra rovesciata " \\ ", per eseguire l'escape della parentesi di apertura "(", invece, sostituire la barra rovesciata con il carattere speciale " \\ 28", come segue: "sAMAccountName = \\ 28Test".</span><span class="sxs-lookup"><span data-stu-id="6f4f1-132">For example, for a statement that used the syntax "samAccountName=\(Test", which uses the backslash, "\\", to escape the open parenthesis, "(", instead, you would replace the backslash with the special character "\\28", as follows: "samAccountName=\\28Test".</span></span>

 

<span data-ttu-id="6f4f1-133">Le istruzioni di query seguenti sono esempi di sottolinguaggio SQL in ADSI.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-133">The following query statements are examples of SQL dialect in ADSI.</span></span>

<span data-ttu-id="6f4f1-134">Per cercare tutti gli oggetti gruppo.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-134">To search for all the group objects.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



<span data-ttu-id="6f4f1-135">Per cercare tutti gli utenti il cui cognome inizia con la lettera H.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-135">To search for all the users whose Last Name starts with letter H.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



<span data-ttu-id="6f4f1-136">La grammatica formale per le query SQL è definita nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-136">The formal grammar for SQL queries is defined in the following code example.</span></span> <span data-ttu-id="6f4f1-137">Tutte le parole chiave non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-137">All keywords are case-insensitive.</span></span>


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



<span data-ttu-id="6f4f1-138">I join interni di SQL non sono supportati dal provider Active Directory OLE DB, ma è possibile usare SQL per aggiungere dati SQL e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-138">SQL inner joins are not supported by the Active Directory OLE DB provider, but you can use SQL to join SQL and Active Directory data.</span></span> <span data-ttu-id="6f4f1-139">Per ulteriori informazioni, vedere [creazione di un join eterogeneo tra SQL Server e Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span><span class="sxs-lookup"><span data-stu-id="6f4f1-139">For more information, see [Creating a Heterogeneous Join between SQL Server and Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f4f1-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f4f1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f4f1-141">Sintassi del filtro di ricerca</span><span class="sxs-lookup"><span data-stu-id="6f4f1-141">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="6f4f1-142">Dialetto LDAP</span><span class="sxs-lookup"><span data-stu-id="6f4f1-142">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="6f4f1-143">Ricerca con l'interfaccia IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="6f4f1-143">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="6f4f1-144">Ricerca con ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="6f4f1-144">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="6f4f1-145">Ricerca con OLE DB</span><span class="sxs-lookup"><span data-stu-id="6f4f1-145">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




