---
title: Query distribuite
description: Poiché ADSI è un provider di OLE DB, può partecipare alla query distribuita introdotta in Microsoft SQL Server 7,0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- query ADSI, query distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "106299453"
---
# <a name="distributed-query"></a><span data-ttu-id="888ad-104">Query distribuite</span><span class="sxs-lookup"><span data-stu-id="888ad-104">Distributed Query</span></span>

<span data-ttu-id="888ad-105">Poiché ADSI è un provider di OLE DB, può partecipare alla query distribuita introdotta in Microsoft SQL Server 7,0.</span><span class="sxs-lookup"><span data-stu-id="888ad-105">Because ADSI is an OLE DB Provider, it can participate in Distributed Query introduced in Microsoft SQL Server 7.0.</span></span> <span data-ttu-id="888ad-106">Gli scenari possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="888ad-106">The following are possible scenarios:</span></span>

-   <span data-ttu-id="888ad-107">Unione di Active Directory oggetti con dati SQL Server.</span><span class="sxs-lookup"><span data-stu-id="888ad-107">Joining Active Directory objects with SQL Server data.</span></span>
-   <span data-ttu-id="888ad-108">Aggiornamento dei dati SQL da oggetti Active Directory.</span><span class="sxs-lookup"><span data-stu-id="888ad-108">Updating SQL data from Active Directory objects.</span></span>
-   <span data-ttu-id="888ad-109">Creazione di join a tre vie o a quattro vie con altri provider di OLE DB.</span><span class="sxs-lookup"><span data-stu-id="888ad-109">Creating three-way or four-way joins with other OLE DB Providers.</span></span> <span data-ttu-id="888ad-110">Ad esempio, index server, SQL Server e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="888ad-110">For example, Index Server, SQL Server, and Active Directory.</span></span>

<span data-ttu-id="888ad-111">Il provider OLE DB supporta due dialetti dei comandi, LDAP e SQL, per accedere al servizio directory e restituire i risultati in un formato tabulare su cui è possibile eseguire query con SQL Server query distribuite.</span><span class="sxs-lookup"><span data-stu-id="888ad-111">The OLE DB Provider supports two command dialects, LDAP and SQL, to access the directory service and return results in a tabular form that can be queried with SQL Server distributed queries.</span></span>

<span data-ttu-id="888ad-112">**Per avviare SQL Query Analyzer**</span><span class="sxs-lookup"><span data-stu-id="888ad-112">**To start the SQL Query Analyzer**</span></span>

1.  <span data-ttu-id="888ad-113">Per prima cosa, aprire [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) nel SQL Server collegato al servizio directory (vedere Creazione di un server collegato).</span><span class="sxs-lookup"><span data-stu-id="888ad-113">First, open the [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) on the SQL Server that is linked to the directory service (see Creating a Linked Server).</span></span>
2.  <span data-ttu-id="888ad-114">Eseguire **SQL Query Analyzer** (avvia \| programmi \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="888ad-114">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
3.  <span data-ttu-id="888ad-115">Accedere al computer SQL Server.</span><span class="sxs-lookup"><span data-stu-id="888ad-115">Log on to the SQL Server computer.</span></span>
4.  <span data-ttu-id="888ad-116">Immettere la query SQL nel riquadro Editor della finestra query.</span><span class="sxs-lookup"><span data-stu-id="888ad-116">Enter the SQL Query into the Editor pane of the query window.</span></span>
5.  <span data-ttu-id="888ad-117">Eseguire la query premendo F5.</span><span class="sxs-lookup"><span data-stu-id="888ad-117">Execute the query by pressing F5.</span></span>

<span data-ttu-id="888ad-118">Le sezioni seguenti forniscono maggiori dettagli:</span><span class="sxs-lookup"><span data-stu-id="888ad-118">The following sections provide more detail:</span></span>

-   [<span data-ttu-id="888ad-119">Creazione di un server collegato</span><span class="sxs-lookup"><span data-stu-id="888ad-119">Creating a Linked Server</span></span>](#creating-a-linked-server)
-   [<span data-ttu-id="888ad-120">Creazione di un account di accesso con autenticazione SQL Server</span><span class="sxs-lookup"><span data-stu-id="888ad-120">Creating a SQL Server Authenticated Login</span></span>](#creating-a-sql-server-authenticated-login)
-   [<span data-ttu-id="888ad-121">Esecuzione di query sul servizio directory</span><span class="sxs-lookup"><span data-stu-id="888ad-121">Querying the Directory Service</span></span>](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a><span data-ttu-id="888ad-122">Creazione di un server collegato</span><span class="sxs-lookup"><span data-stu-id="888ad-122">Creating a Linked Server</span></span>

<span data-ttu-id="888ad-123">Per configurare un join distribuito in un servizio directory di Windows Server 2000, creare un server collegato.</span><span class="sxs-lookup"><span data-stu-id="888ad-123">To set up a distributed join on a Windows 2000 Server directory service, create a linked server.</span></span> <span data-ttu-id="888ad-124">A tale scopo, configurare il mapping ADSI utilizzando la stored procedure di sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) .</span><span class="sxs-lookup"><span data-stu-id="888ad-124">To do this, set up ADSI mapping by using the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure.</span></span> <span data-ttu-id="888ad-125">Questa procedura collega un nome a un nome di provider OLE DB.</span><span class="sxs-lookup"><span data-stu-id="888ad-125">This procedure links a name to an OLE DB Provider name.</span></span>

<span data-ttu-id="888ad-126">Nell'esempio seguente si noti che esistono diversi argomenti utilizzati con la stored procedure di sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) :</span><span class="sxs-lookup"><span data-stu-id="888ad-126">In the following example, note that there are several arguments used with the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="888ad-127">"ADSI" è l'argomento del **Server** e sarà il nome del server collegato.</span><span class="sxs-lookup"><span data-stu-id="888ad-127">"ADSI" is the **server** argument and will be the name of this linked server.</span></span>
-   <span data-ttu-id="888ad-128">"Active Directory Services 2,5" è l'argomento **srvproduct** , ovvero il nome dell'origine dati OLE DB che si sta aggiungendo come server collegato.</span><span class="sxs-lookup"><span data-stu-id="888ad-128">"Active Directory Services 2.5" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
-   <span data-ttu-id="888ad-129">"ADSDSOObject" è l'argomento del **\_ nome del provider** .</span><span class="sxs-lookup"><span data-stu-id="888ad-129">"ADSDSOObject" is the **provider\_name** argument.</span></span>
-   <span data-ttu-id="888ad-130">"adsdatasource" è l'argomento dell' **\_ origine dati** , ovvero il nome dell'origine dati interpretato dal provider OLE DB.</span><span class="sxs-lookup"><span data-stu-id="888ad-130">"adsdatasource" is the **data\_source** argument, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

<span data-ttu-id="888ad-131">Il comando [Exec](https://msdn.microsoft.com/library/Aa258848.aspx) viene utilizzato per eseguire stored procedure di sistema.</span><span class="sxs-lookup"><span data-stu-id="888ad-131">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



<span data-ttu-id="888ad-132">Per gli account di accesso con autenticazione di Windows, il mapping automatico è sufficiente per accedere alla directory con SQL Server delega di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="888ad-132">For Windows-authenticated logins, the self-mapping is sufficient to access the directory with SQL Server Security Delegation.</span></span> <span data-ttu-id="888ad-133">Poiché per impostazione predefinita il mapping automatico viene creato per i server collegati creati tramite [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), non è necessario alcun altro mapping degli account di accesso.</span><span class="sxs-lookup"><span data-stu-id="888ad-133">Because the self-mapping is created by default for linked servers created through [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), no other login mapping is necessary.</span></span>

<span data-ttu-id="888ad-134">Per gli account di accesso con autenticazione SQL Server, è possibile configurare account di accesso e password appropriati per la connessione al servizio directory tramite la stored procedure di sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="888ad-134">For SQL Server–authenticated logins, you can configure suitable logins and passwords for connecting to the directory service by using the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

> [!Note]  
> <span data-ttu-id="888ad-135">Se possibile, usare l'autenticazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="888ad-135">When possible, use Windows Authentication.</span></span>

 

## <a name="creating-a-sql-server-authenticated-login"></a><span data-ttu-id="888ad-136">Creazione di un account di accesso con autenticazione SQL Server</span><span class="sxs-lookup"><span data-stu-id="888ad-136">Creating a SQL Server Authenticated Login</span></span>

<span data-ttu-id="888ad-137">Se si preferisce usare un account di accesso con autenticazione SQL Server anziché l'autenticazione di Windows, aggiungere un account di accesso al server collegato. vedere la sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="888ad-137">If you prefer to use a SQL Server–authenticated login rather than Windows Authentication, add a login to the linked server (see the previous section).</span></span> <span data-ttu-id="888ad-138">A tale scopo, usare la stored procedure di sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="888ad-138">To do this, use the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

<span data-ttu-id="888ad-139">Nell'esempio seguente sono presenti diversi argomenti usati con la stored procedure di sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) :</span><span class="sxs-lookup"><span data-stu-id="888ad-139">In the following example, there are several arguments that are used with the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="888ad-140">"ADSI" è l'argomento **rmtsvrname** , ovvero il nome del server collegato creato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="888ad-140">"ADSI" is the **rmtsvrname** argument, which is the name of the linked server created in the previous example.</span></span>
-   <span data-ttu-id="888ad-141">" \\ Amministratore Fabrikam" è l'argomento **locallogin** , che è l'account di accesso nel server locale e può essere il SQL Server account di accesso o un utente di Windows NT.</span><span class="sxs-lookup"><span data-stu-id="888ad-141">"Fabrikam\\Administrator" is the **locallogin** argument, which is the login on the local server and can be the SQL Server login or a Windows NT user.</span></span>
-   <span data-ttu-id="888ad-142">"CN = Administrator, OU = Sales, DC = activeds, DC = Fabrikam, DC = com" è l'argomento **rmtuser** , che corrisponde al nome utente usato per la connessione perché **useself** è **false**.</span><span class="sxs-lookup"><span data-stu-id="888ad-142">"CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" is the **rmtuser** argument, which is the user name that you use to connect because **useself** is **false**.</span></span>
-   <span data-ttu-id="888ad-143">"Secret \* \* 2000" è **rmtpassword**, che è la password associata a **rmtuser**</span><span class="sxs-lookup"><span data-stu-id="888ad-143">"secret\*\*2000" is the **rmtpassword**, which is the password associated to **rmtuser**</span></span>

<span data-ttu-id="888ad-144">Il comando [Exec](https://msdn.microsoft.com/library/Aa258848.aspx) viene utilizzato per eseguire stored procedure di sistema.</span><span class="sxs-lookup"><span data-stu-id="888ad-144">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a><span data-ttu-id="888ad-145">Esecuzione di query sul servizio directory</span><span class="sxs-lookup"><span data-stu-id="888ad-145">Querying the Directory Service</span></span>

<span data-ttu-id="888ad-146">Dopo aver creato un server collegato, usare un'istruzione [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) per inviare una query al servizio directory.</span><span class="sxs-lookup"><span data-stu-id="888ad-146">After you have created a linked server, use an [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement to send a query to the Directory Service.</span></span> <span data-ttu-id="888ad-147">La query SQL seguente crea una tabella virtuale in cui conservare i risultati della query utilizzando l'istruzione [Create View](https://msdn.microsoft.com/library/Aa258253.aspx) .</span><span class="sxs-lookup"><span data-stu-id="888ad-147">The following SQL query creates a virtual table to hold your query results by using the [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) statement.</span></span> <span data-ttu-id="888ad-148">La vista creata è denominata "viewADContacts".</span><span class="sxs-lookup"><span data-stu-id="888ad-148">The view that is created is named "viewADContacts".</span></span>

<span data-ttu-id="888ad-149">La prima istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) definisce le informazioni su cui viene eseguita una query dal servizio directory e ne esegue il mapping a una colonna della tabella.</span><span class="sxs-lookup"><span data-stu-id="888ad-149">The first [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement defines the information that is being queried from the directory service and maps it to a column in the table.</span></span> <span data-ttu-id="888ad-150">Le informazioni racchiuse tra parentesi quadre indicano i dati inseriti nella tabella virtuale.</span><span class="sxs-lookup"><span data-stu-id="888ad-150">Information surrounded by brackets indicates the data that is put into the virtual table.</span></span> <span data-ttu-id="888ad-151">Le informazioni non tra parentesi quadre indicano i dati recuperati dal servizio directory.</span><span class="sxs-lookup"><span data-stu-id="888ad-151">The information that is not in brackets indicates the data that is retrieved from the directory service.</span></span> <span data-ttu-id="888ad-152">Si noti che è necessario fare riferimento alle informazioni recuperate dal servizio directory tramite il relativo nome visualizzato LDAP.</span><span class="sxs-lookup"><span data-stu-id="888ad-152">Notice that the information that is being retrieved from the directory service must be referenced by its LDAP display name.</span></span>

<span data-ttu-id="888ad-153">L'istruzione successiva è l'istruzione [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="888ad-153">The next statement is the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="888ad-154">Questa istruzione ha due argomenti: ADSI, ovvero il nome del server collegato creato e un'istruzione di query.</span><span class="sxs-lookup"><span data-stu-id="888ad-154">This statement has two arguments: ADSI, which is the name of the linked server that you created, and a query statement.</span></span> <span data-ttu-id="888ad-155">L'istruzione di query contiene gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="888ad-155">The query statement contains the following items:</span></span>

-   <span data-ttu-id="888ad-156">L'istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene l'elenco dei dati che verranno ottenuti dal servizio directory.</span><span class="sxs-lookup"><span data-stu-id="888ad-156">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="888ad-157">È necessario usare il nome visualizzato LDAP per indicare i dati che si stanno cercando.</span><span class="sxs-lookup"><span data-stu-id="888ad-157">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
-   <span data-ttu-id="888ad-158">L'istruzione [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene il nome del server di directory collegato da cui verranno ottenute queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="888ad-158">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
-   <span data-ttu-id="888ad-159">L'istruzione [where](https://msdn.microsoft.com/library/Aa260674.aspx) fornisce le condizioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="888ad-159">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="888ad-160">In questo esempio è in corso la ricerca di contatti.</span><span class="sxs-lookup"><span data-stu-id="888ad-160">In this example, it is searching for contacts.</span></span>

<span data-ttu-id="888ad-161">L'istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) finale viene utilizzata per prelevare i risultati dalla visualizzazione da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="888ad-161">The final [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement is used to pick up results from the view to display.</span></span>


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




