---
title: Ricerca con ActiveX Data Objects (ADO)
description: Il modello ADO (ActiveX Data Object) è costituito da oggetti elencati nella tabella seguente.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI, ricerca con ADO
- Ricerca con ActiveX Data Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300458"
---
# <a name="searching-with-activex-data-objects-ado"></a><span data-ttu-id="b84ba-105">Ricerca con ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="b84ba-105">Searching with ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="b84ba-106">Il modello ADO (ActiveX Data Object) è costituito da oggetti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b84ba-106">The ActiveX Data Object (ADO) model consists of objects listed in the following table.</span></span>



| <span data-ttu-id="b84ba-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="b84ba-107">Object</span></span>         | <span data-ttu-id="b84ba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b84ba-108">Description</span></span>                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b84ba-109">**Connection**</span><span class="sxs-lookup"><span data-stu-id="b84ba-109">**Connection**</span></span> | <span data-ttu-id="b84ba-110">Connessione aperta a un'origine dati OLE DB, ad esempio ADSI.</span><span class="sxs-lookup"><span data-stu-id="b84ba-110">An open connection to an OLE DB data source such as ADSI.</span></span>                                                                          |
| <span data-ttu-id="b84ba-111">**Comando**</span><span class="sxs-lookup"><span data-stu-id="b84ba-111">**Command**</span></span>    | <span data-ttu-id="b84ba-112">Definisce un comando specifico da eseguire sull'origine dati.</span><span class="sxs-lookup"><span data-stu-id="b84ba-112">Defines a specific command to run against the data source.</span></span>                                                                         |
| <span data-ttu-id="b84ba-113">**Parametro**</span><span class="sxs-lookup"><span data-stu-id="b84ba-113">**Parameter**</span></span>  | <span data-ttu-id="b84ba-114">Raccolta facoltativa per tutti i parametri da fornire all'oggetto Command.</span><span class="sxs-lookup"><span data-stu-id="b84ba-114">An optional collection for any parameters to provide to the command object.</span></span>                                                        |
| <span data-ttu-id="b84ba-115">**RecordSet**</span><span class="sxs-lookup"><span data-stu-id="b84ba-115">**RecordSet**</span></span>  | <span data-ttu-id="b84ba-116">Set di record da una tabella, da un oggetto comando o da una sintassi SQL.</span><span class="sxs-lookup"><span data-stu-id="b84ba-116">A set of records from a table, command object, or SQL syntax.</span></span> <span data-ttu-id="b84ba-117">È possibile creare un recordset senza oggetti connessione sottostanti.</span><span class="sxs-lookup"><span data-stu-id="b84ba-117">A recordset can be created without any underlying connection object.</span></span> |
| <span data-ttu-id="b84ba-118">**Campo**</span><span class="sxs-lookup"><span data-stu-id="b84ba-118">**Field**</span></span>      | <span data-ttu-id="b84ba-119">Una singola colonna di dati in un recordset.</span><span class="sxs-lookup"><span data-stu-id="b84ba-119">A single column of data in a recordset.</span></span>                                                                                            |
| <span data-ttu-id="b84ba-120">**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="b84ba-120">**Property**</span></span>   | <span data-ttu-id="b84ba-121">Raccolta di valori forniti dal provider per ADO.</span><span class="sxs-lookup"><span data-stu-id="b84ba-121">A collection of values supplied by the provider for ADO.</span></span>                                                                           |
| <span data-ttu-id="b84ba-122">**Error (Errore) (Error (Errore)e)**</span><span class="sxs-lookup"><span data-stu-id="b84ba-122">**Error**</span></span>      | <span data-ttu-id="b84ba-123">Contiene i dati relativi agli errori di accesso ai dati.</span><span class="sxs-lookup"><span data-stu-id="b84ba-123">Contains data about data access errors.</span></span> <span data-ttu-id="b84ba-124">Aggiornato quando si verifica un errore in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="b84ba-124">Refreshed when an error occurs in a single operation.</span></span>                                      |



 

<span data-ttu-id="b84ba-125">Per la comunicazione di ADO con ADSI, devono essere presenti almeno due oggetti ADO: **Connection** e **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b84ba-125">For ADO to communicate with ADSI, there must be, at least, two ADO objects: **Connection** and **RecordSet**.</span></span> <span data-ttu-id="b84ba-126">Questi oggetti ADO servono per autenticare gli utenti ed enumerare rispettivamente i risultati.</span><span class="sxs-lookup"><span data-stu-id="b84ba-126">These ADO objects serve to authenticate users and enumerate results, respectively.</span></span> <span data-ttu-id="b84ba-127">In genere, si userà anche un oggetto **Command** per mantenere una connessione attiva, specificare i parametri di query, ad esempio le dimensioni della pagina e l'ambito di ricerca, ed eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="b84ba-127">Typically, you will also use a **Command** object to maintain an active connection, specify query parameters, such as page size and search scope, and perform a query.</span></span> <span data-ttu-id="b84ba-128">Per ulteriori informazioni sulla sintassi del filtro di ricerca, vedere la [sintassi del filtro di ricerca](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b84ba-128">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="b84ba-129">L'oggetto **Connection** carica il provider OLE DB e convalida le credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b84ba-129">The **Connection** object loads the OLE DB provider, and validates user credentials.</span></span> <span data-ttu-id="b84ba-130">In Visual Basic chiamare la funzione **CreateObject** con "ADODB. Connection "per creare un'istanza di un oggetto **Connection** , quindi impostare la proprietà **provider** dell'oggetto **Connection** su" ADSDSOObject ".</span><span class="sxs-lookup"><span data-stu-id="b84ba-130">In Visual Basic, call the **CreateObject** function with "ADODB.Connection" to create an instance of a **Connection** object, and then set the **Provider** property of the **Connection** object to "ADsDSOObject".</span></span> <span data-ttu-id="b84ba-131">Oggetto ADODB. Connection "è il ProgID dell'oggetto **Connection** e" ADSDSOObject "è il nome del provider OLE DB in ADSI.</span><span class="sxs-lookup"><span data-stu-id="b84ba-131">"ADODB.Connection" is the ProgID of the **Connection** object and "ADsDSOObject" is the name of the OLE DB provider in ADSI.</span></span> <span data-ttu-id="b84ba-132">Se non viene specificata alcuna credenziale, vengono utilizzate le credenziali dell'utente attualmente connesso.</span><span class="sxs-lookup"><span data-stu-id="b84ba-132">If no credentials are specified, the credentials of the currently logged on user are used.</span></span>

<span data-ttu-id="b84ba-133">Nell'esempio di codice riportato di seguito viene illustrato come creare un'istanza di un oggetto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="b84ba-133">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="b84ba-134">Nell'esempio di codice riportato di seguito viene illustrato come creare un'istanza di un oggetto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="b84ba-134">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



<span data-ttu-id="b84ba-135">Nell'esempio di codice riportato di seguito viene illustrato come creare un'istanza di un oggetto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="b84ba-135">The following code example shows how to create an instance of a **Connection** object.</span></span> <span data-ttu-id="b84ba-136">Tenere presente che è necessario includere la libreria dei tipi ADO (msadoXX.dll) come uno dei riferimenti del progetto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b84ba-136">Be aware that you must include the ADO type library (msadoXX.dll) as one of the references in the Visual Basic project.</span></span>


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="b84ba-137">Specificare i dati di autenticazione utente impostando le proprietà dell'oggetto **connessione** .</span><span class="sxs-lookup"><span data-stu-id="b84ba-137">Specify user authentication data by setting the properties of the **Connection** object.</span></span> <span data-ttu-id="b84ba-138">Nella tabella seguente sono elencate le proprietà di autenticazione utente supportate da ADSI.</span><span class="sxs-lookup"><span data-stu-id="b84ba-138">The following table lists ADSI-supported user-authentication properties.</span></span>



| <span data-ttu-id="b84ba-139">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b84ba-139">Property</span></span>           | <span data-ttu-id="b84ba-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b84ba-140">Description</span></span>                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b84ba-141">"User ID"</span><span class="sxs-lookup"><span data-stu-id="b84ba-141">"User ID"</span></span>          | <span data-ttu-id="b84ba-142">Stringa che identifica l'utente il cui contesto di sicurezza viene utilizzato quando si esegue la ricerca.</span><span class="sxs-lookup"><span data-stu-id="b84ba-142">A string that identifies the user whose security context is used when performing the search.</span></span> <span data-ttu-id="b84ba-143">Per ulteriori informazioni sul formato della stringa del nome utente, vedere [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span><span class="sxs-lookup"><span data-stu-id="b84ba-143">For more information about the format of the user name string, see [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span></span> <span data-ttu-id="b84ba-144">Se non specificato, il valore predefinito è l'utente connesso o l'utente rappresentato dal processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="b84ba-144">If not specified, the default is the logged on user, or the user impersonated by the calling process.</span></span> |
| <span data-ttu-id="b84ba-145">"Password"</span><span class="sxs-lookup"><span data-stu-id="b84ba-145">"Password"</span></span>         | <span data-ttu-id="b84ba-146">Stringa che specifica la password dell'utente identificato da "User ID".</span><span class="sxs-lookup"><span data-stu-id="b84ba-146">A string that specifies the password of the user identified by "User ID".</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b84ba-147">"Crittografa password"</span><span class="sxs-lookup"><span data-stu-id="b84ba-147">"Encrypt Password"</span></span> | <span data-ttu-id="b84ba-148">Valore booleano che specifica se la password è crittografata.</span><span class="sxs-lookup"><span data-stu-id="b84ba-148">A Boolean value that specifies whether the password is encrypted.</span></span> <span data-ttu-id="b84ba-149">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="b84ba-149">The default is **false**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b84ba-150">"Flag ADSI"</span><span class="sxs-lookup"><span data-stu-id="b84ba-150">"ADSI Flag"</span></span>        | <span data-ttu-id="b84ba-151">Set di flag dell'enumerazione dell'enumerazione di [**\_ \_ autenticazione ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) che specificano le opzioni di autenticazione del binding.</span><span class="sxs-lookup"><span data-stu-id="b84ba-151">A set of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration that specify the binding authentication options.</span></span> <span data-ttu-id="b84ba-152">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="b84ba-152">The default is zero.</span></span>                                                                                                                                                                         |



 

<span data-ttu-id="b84ba-153">Nell'esempio di codice seguente viene illustrata la modalità di impostazione delle proprietà prima di creare l'oggetto **Command** .</span><span class="sxs-lookup"><span data-stu-id="b84ba-153">The following code example shows how the properties are set before creating the **Command** object.</span></span>


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



<span data-ttu-id="b84ba-154">Il secondo oggetto ADO è l'oggetto **Command** .</span><span class="sxs-lookup"><span data-stu-id="b84ba-154">The second ADO object is the **Command** object.</span></span> <span data-ttu-id="b84ba-155">Il ProgID dell'oggetto **Command** è "ADODB. Command".</span><span class="sxs-lookup"><span data-stu-id="b84ba-155">The ProgID of the **Command** object is "ADODB.Command".</span></span> <span data-ttu-id="b84ba-156">Questo oggetto consente di inviare istruzioni di query e altri comandi ad ADSI utilizzando la connessione attiva.</span><span class="sxs-lookup"><span data-stu-id="b84ba-156">This object enables you to issue query statements and other commands to ADSI using the active connection.</span></span> <span data-ttu-id="b84ba-157">L'oggetto **Command** usa la relativa proprietà **ActiveConnection** per mantenere una connessione attiva.</span><span class="sxs-lookup"><span data-stu-id="b84ba-157">The **Command** object uses its **ActiveConnection** property to maintain an active connection.</span></span> <span data-ttu-id="b84ba-158">Mantiene inoltre la proprietà **CommandText** per mantenere le istruzioni di query rilasciate da un utente.</span><span class="sxs-lookup"><span data-stu-id="b84ba-158">It also maintains the **CommandText** property to hold query statements issued by a user.</span></span> <span data-ttu-id="b84ba-159">Le istruzioni di query sono espresse nel dialetto [SQL](sql-dialect.md) o nel [sottolinguaggio LDAP](ldap-dialect.md).</span><span class="sxs-lookup"><span data-stu-id="b84ba-159">The query statements are expressed in either the [SQL dialect](sql-dialect.md) or the [LDAP dialect](ldap-dialect.md).</span></span>

<span data-ttu-id="b84ba-160">Negli esempi di codice seguenti viene illustrato come creare un oggetto **comando** .</span><span class="sxs-lookup"><span data-stu-id="b84ba-160">The following code examples show how to create a **Command** object.</span></span>


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



<span data-ttu-id="b84ba-161">Nell'esempio di codice seguente, includere la libreria dei tipi ADO (msadoXX.dll) come uno dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="b84ba-161">In the following code example, include ADO type library (msadoXX.dll) as one of the references.</span></span>


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



<span data-ttu-id="b84ba-162">Le opzioni di ricerca per l'oggetto **Command** vengono specificate impostando la proprietà **Properties** .</span><span class="sxs-lookup"><span data-stu-id="b84ba-162">Search options for the **Command** object are specified by setting the **Properties** property.</span></span> <span data-ttu-id="b84ba-163">Nella tabella seguente sono elencate le proprietà denominate accettabili per le **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="b84ba-163">The following table lists acceptable named properties for **Properties**.</span></span>



| <span data-ttu-id="b84ba-164">Proprietà denominata</span><span class="sxs-lookup"><span data-stu-id="b84ba-164">Named property</span></span>      | <span data-ttu-id="b84ba-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b84ba-165">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b84ba-166">Asincrona</span><span class="sxs-lookup"><span data-stu-id="b84ba-166">"Asynchronous"</span></span>      | <span data-ttu-id="b84ba-167">Valore booleano che specifica se la ricerca è sincrona o asincrona.</span><span class="sxs-lookup"><span data-stu-id="b84ba-167">A Boolean value that specifies whether the search is synchronous or asynchronous.</span></span> <span data-ttu-id="b84ba-168">Il valore predefinito è false (sincrono).</span><span class="sxs-lookup"><span data-stu-id="b84ba-168">The default is False (synchronous).</span></span> <span data-ttu-id="b84ba-169">Un blocco di ricerca sincrono fino a quando il server non restituisce l'intero risultato o per una ricerca di paging, l'intera pagina.</span><span class="sxs-lookup"><span data-stu-id="b84ba-169">A synchronous search blocks until the server returns the entire result, or for a paged search, the entire page.</span></span> <span data-ttu-id="b84ba-170">Un blocco di ricerca asincrono finché non è disponibile una riga dei risultati della ricerca o fino a quando non scade il tempo specificato dalla proprietà "timeout".</span><span class="sxs-lookup"><span data-stu-id="b84ba-170">An asynchronous search blocks until one row of the search results is available, or until the time specified by the "Timeout" property elapses.</span></span>                           |
| <span data-ttu-id="b84ba-171">"Risultati della cache"</span><span class="sxs-lookup"><span data-stu-id="b84ba-171">"Cache results"</span></span>     | <span data-ttu-id="b84ba-172">Valore booleano che specifica se il risultato deve essere memorizzato nella cache sul lato client.</span><span class="sxs-lookup"><span data-stu-id="b84ba-172">A Boolean value that specifies whether the result should be cached on the client side.</span></span> <span data-ttu-id="b84ba-173">Il valore predefinito è **true**; Il set di risultati viene memorizzato nella cache ADSI.</span><span class="sxs-lookup"><span data-stu-id="b84ba-173">The default is **true**; ADSI caches the result set.</span></span> <span data-ttu-id="b84ba-174">La disattivazione di questa opzione può essere utile per set di risultati di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b84ba-174">Turning off this option may be desirable for large result sets.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="b84ba-175">"Riferimenti inseguiti"</span><span class="sxs-lookup"><span data-stu-id="b84ba-175">"Chase referrals"</span></span>   | <span data-ttu-id="b84ba-176">Valore dell' [**\_ enum ADS Chase \_ referentes \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) che specifica il modo in cui la ricerca insegue i riferimenti.</span><span class="sxs-lookup"><span data-stu-id="b84ba-176">A value from the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) that specifies how the search chases referrals.</span></span> <span data-ttu-id="b84ba-177">Per impostazione predefinita, i **\_ riferimenti Chase di ADS non sono \_ \_ mai**. Per ulteriori informazioni su questa proprietà, vedere [riferimenti](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="b84ba-177">The default is **ADS\_CHASE\_REFERRALS\_NEVER**.For more information about this property, see [Referrals](/windows/desktop/AD/referrals).</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="b84ba-178">"Solo nomi di colonna"</span><span class="sxs-lookup"><span data-stu-id="b84ba-178">"Column Names Only"</span></span> | <span data-ttu-id="b84ba-179">Valore booleano che indica che la ricerca deve recuperare solo il nome degli attributi a cui sono stati assegnati i valori.</span><span class="sxs-lookup"><span data-stu-id="b84ba-179">A Boolean value that indicates that the search should retrieve only the name of attributes to which values have been assigned.</span></span> <span data-ttu-id="b84ba-180">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="b84ba-180">The default is **false**.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b84ba-181">"Alias Deref"</span><span class="sxs-lookup"><span data-stu-id="b84ba-181">"Deref Aliases"</span></span>     | <span data-ttu-id="b84ba-182">Valore booleano che specifica se gli alias degli oggetti trovati vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="b84ba-182">A Boolean value that specifies whether aliases of found objects are resolved.</span></span> <span data-ttu-id="b84ba-183">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="b84ba-183">The default is **false**.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="b84ba-184">"Dimensioni pagina"</span><span class="sxs-lookup"><span data-stu-id="b84ba-184">"Page size"</span></span>         | <span data-ttu-id="b84ba-185">Valore intero che attiva il paging e specifica il numero massimo di oggetti da restituire in un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="b84ba-185">An integer value that turns on paging and specifies the maximum number of objects to return in a results set.</span></span> <span data-ttu-id="b84ba-186">Il valore predefinito è nessuna dimensione di pagina.</span><span class="sxs-lookup"><span data-stu-id="b84ba-186">The default is no page size.</span></span> <span data-ttu-id="b84ba-187">Per ulteriori informazioni, vedere [recupero di set di risultati di grandi dimensioni](retrieving-large-results-sets.md).</span><span class="sxs-lookup"><span data-stu-id="b84ba-187">For more information, see [Retrieving Large Results Sets](retrieving-large-results-sets.md).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="b84ba-188">SearchScope</span><span class="sxs-lookup"><span data-stu-id="b84ba-188">"SearchScope"</span></span>       | <span data-ttu-id="b84ba-189">Valore dell'enumerazione [**Ads \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) che specifica l'ambito di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b84ba-189">A value from the [**ADS\_SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) enumeration that specifies the search scope.</span></span> <span data-ttu-id="b84ba-190">Il valore predefinito è il **\_ \_ sottoalbero dell'ambito ADS**.</span><span class="sxs-lookup"><span data-stu-id="b84ba-190">The default is **ADS\_SCOPE\_SUBTREE**.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b84ba-191">"Limite dimensioni"</span><span class="sxs-lookup"><span data-stu-id="b84ba-191">"Size Limit"</span></span>        | <span data-ttu-id="b84ba-192">Valore intero che specifica il limite di dimensioni per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="b84ba-192">An integer value that specifies the size limit for the search.</span></span> <span data-ttu-id="b84ba-193">Per Active Directory, il limite di dimensioni specifica il numero massimo di oggetti restituiti.</span><span class="sxs-lookup"><span data-stu-id="b84ba-193">For Active Directory, the size limit specifies the maximum number of returned objects.</span></span> <span data-ttu-id="b84ba-194">Il server interrompe la ricerca quando viene raggiunto il limite di dimensioni e restituisce i risultati accumulati.</span><span class="sxs-lookup"><span data-stu-id="b84ba-194">The server stops searching when the size limit is reached and returns the results accumulated.</span></span> <span data-ttu-id="b84ba-195">Il valore predefinito non è limite.</span><span class="sxs-lookup"><span data-stu-id="b84ba-195">The default is no limit.</span></span>                                                                                                                                  |
| <span data-ttu-id="b84ba-196">"Ordina su"</span><span class="sxs-lookup"><span data-stu-id="b84ba-196">"Sort on"</span></span>           | <span data-ttu-id="b84ba-197">Stringa che specifica un elenco delimitato da virgole di attributi da utilizzare come chiavi di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="b84ba-197">A string that specifies a comma-separated list of attributes to use as sort keys.</span></span> <span data-ttu-id="b84ba-198">Questa proprietà funziona solo per i server di directory che supportano il controllo LDAP per l'ordinamento sul lato server.</span><span class="sxs-lookup"><span data-stu-id="b84ba-198">This property works only for directory servers that support the LDAP control for server-side sorting.</span></span> <span data-ttu-id="b84ba-199">Active Directory supporta il controllo di ordinamento, ma può influisca sulle prestazioni del server, in particolare se il set di risultati è di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b84ba-199">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="b84ba-200">Tenere presente che Active Directory supporta solo una singola chiave di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="b84ba-200">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="b84ba-201">Il valore predefinito non è ordinamento.</span><span class="sxs-lookup"><span data-stu-id="b84ba-201">The default is no sorting.</span></span> |
| <span data-ttu-id="b84ba-202">"Limite di tempo"</span><span class="sxs-lookup"><span data-stu-id="b84ba-202">"Time Limit"</span></span>        | <span data-ttu-id="b84ba-203">Valore intero che specifica il limite di tempo, in secondi, per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="b84ba-203">An integer value that specifies the time limit, in seconds, for the search.</span></span> <span data-ttu-id="b84ba-204">Quando viene raggiunto il limite di tempo, il server interrompe la ricerca e restituisce i risultati accumulati.</span><span class="sxs-lookup"><span data-stu-id="b84ba-204">When the time limit is reached, the server stops searching and returns the results accumulated.</span></span> <span data-ttu-id="b84ba-205">Il valore predefinito non è alcun limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="b84ba-205">The default is no time limit.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="b84ba-206">Timeout</span><span class="sxs-lookup"><span data-stu-id="b84ba-206">"Timeout"</span></span>           | <span data-ttu-id="b84ba-207">Valore intero che specifica il valore di timeout sul lato client, in secondi.</span><span class="sxs-lookup"><span data-stu-id="b84ba-207">An integer value that specifies the client-side timeout value, in seconds.</span></span> <span data-ttu-id="b84ba-208">Questo valore indica il tempo di attesa del client per i risultati del server prima di arrestare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="b84ba-208">This value indicates the time the client waits for results from the server before stopping the search.</span></span> <span data-ttu-id="b84ba-209">Il valore predefinito non prevede alcun timeout.</span><span class="sxs-lookup"><span data-stu-id="b84ba-209">The default is no time-out.</span></span>                                                                                                                                                                                                  |



 

<span data-ttu-id="b84ba-210">Nell'esempio di codice riportato di seguito viene illustrato come impostare le opzioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b84ba-210">The following code example shows how to set search options.</span></span>


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



<span data-ttu-id="b84ba-211">Il terzo oggetto ADO è **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b84ba-211">The third ADO object is **RecordSet**.</span></span> <span data-ttu-id="b84ba-212">Questo oggetto viene ottenuto quando si richiama il metodo **Execute** su un oggetto **Command** .</span><span class="sxs-lookup"><span data-stu-id="b84ba-212">You obtain this object when you invoke the **Execute** method on a **Command** object.</span></span> <span data-ttu-id="b84ba-213">La funzione primaria dell'oggetto **Recordset** consiste nell'enumerare il set di risultati e ottenere i dati.</span><span class="sxs-lookup"><span data-stu-id="b84ba-213">The primary function of the **RecordSet** object is to enumerate the result set and obtain the data.</span></span> <span data-ttu-id="b84ba-214">Il set di risultati può contenere valori per gli attributi con valori singoli o multipli.</span><span class="sxs-lookup"><span data-stu-id="b84ba-214">The result set can contain values for attributes that have both single or multiple values.</span></span> <span data-ttu-id="b84ba-215">Il recupero di un attributo a valore singolo è semplice, in modo analogo al recupero del valore della colonna nel database relazionale, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b84ba-215">Getting a single-valued attribute is simple, similar to getting the column value in the relational database, for example:</span></span>


```VB
Fields('name').Value
```



<span data-ttu-id="b84ba-216">Il recupero di un attributo con più valori, tuttavia, è più complesso.</span><span class="sxs-lookup"><span data-stu-id="b84ba-216">Getting an attribute with multiple values, however, is more challenging.</span></span> <span data-ttu-id="b84ba-217">In questo caso, il **campo. Value** è una matrice ed è necessario controllare il limite inferiore e superiore della matrice, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b84ba-217">In this case, the **Field.Value** is an array and you must check the lower and upper bound of the array, as shown in the following code example.</span></span>


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



<span data-ttu-id="b84ba-218">Nell'esempio di codice seguente gli account utente vengono disabilitati in un server LDAP.</span><span class="sxs-lookup"><span data-stu-id="b84ba-218">The following code example disables the user accounts on an LDAP server.</span></span>


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



<span data-ttu-id="b84ba-219">Per ulteriori informazioni sul modello a oggetti ADO, vedere [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span><span class="sxs-lookup"><span data-stu-id="b84ba-219">For more information about the ADO object model, see [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span></span>

 

