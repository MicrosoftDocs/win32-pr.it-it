---
title: Unione di dati eterogenei
description: Le organizzazioni tipiche archiviano i dati in più database eterogenei. I dati delle risorse umane possono essere archiviati in SQL Server, mentre i dati di gestione degli account vengono archiviati nella directory. Altri dati possono essere archiviati in formati proprietari.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6d0303ee933b81f0c8553b6b0adae64db7f48d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103858033"
---
# <a name="joining-heterogeneous-data"></a><span data-ttu-id="4c57c-105">Unione di dati eterogenei</span><span class="sxs-lookup"><span data-stu-id="4c57c-105">Joining Heterogeneous Data</span></span>

<span data-ttu-id="4c57c-106">Le organizzazioni tipiche archiviano i dati in più database eterogenei.</span><span class="sxs-lookup"><span data-stu-id="4c57c-106">Typical organizations store data in multiple heterogeneous databases.</span></span> <span data-ttu-id="4c57c-107">I dati delle risorse umane possono essere archiviati in SQL Server, mentre i dati di gestione degli account vengono archiviati nella directory.</span><span class="sxs-lookup"><span data-stu-id="4c57c-107">Human Resources data may be stored in SQL Server, while account management data is stored in the directory.</span></span> <span data-ttu-id="4c57c-108">Altri dati possono essere archiviati in formati proprietari.</span><span class="sxs-lookup"><span data-stu-id="4c57c-108">Other data may be stored in proprietary formats.</span></span>

<span data-ttu-id="4c57c-109">Con, SQL Server 7,0, ADSI e il provider di OLE DB, è possibile unire i dati da Active Directory ai dati in SQL Server e creare una vista dei dati aggiunti.</span><span class="sxs-lookup"><span data-stu-id="4c57c-109">With, SQL Server 7.0, ADSI, and the OLE DB Provider, it is possible to join data from Active Directory to data in SQL Server and create a view of the joined data.</span></span>

<span data-ttu-id="4c57c-110">**Per aggiungere Active Directory dati con SQL Server dati**</span><span class="sxs-lookup"><span data-stu-id="4c57c-110">**To join Active Directory Data with SQL Server Data**</span></span>

1.  <span data-ttu-id="4c57c-111">Eseguire **SQL Query Analyzer** (avvia \| programmi \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="4c57c-111">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
2.  <span data-ttu-id="4c57c-112">Accedere al computer SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4c57c-112">Log on to the SQL Server computer.</span></span>
3.  <span data-ttu-id="4c57c-113">Eseguire la riga seguente (evidenziando e premendo CTRL + E):</span><span class="sxs-lookup"><span data-stu-id="4c57c-113">Execute the following line (by highlighting it and pressing CTRL+E):</span></span>

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    <span data-ttu-id="4c57c-114">In questa riga, gli argomenti per la stored procedure di sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c57c-114">In this line, the arguments for the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure are as follows:</span></span>

    -   <span data-ttu-id="4c57c-115">"ADSI" è l'argomento del **Server** , che sarà il nome del server collegato.</span><span class="sxs-lookup"><span data-stu-id="4c57c-115">" ADSI" is the **server** argument, which will be the name of this linked server.</span></span>
    -   <span data-ttu-id="4c57c-116">"Active Directory Services" è l'argomento **srvproduct** , ovvero il nome dell'origine dati OLE DB che si sta aggiungendo come server collegato.</span><span class="sxs-lookup"><span data-stu-id="4c57c-116">"Active Directory Services" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
    -   <span data-ttu-id="4c57c-117">"ADSDSOObject" è l'argomento del **\_ nome del provider** e indica che si sta usando il provider di OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4c57c-117">"ADSDSOObject" is the **provider\_name** argument and indicates you are using the OLE DB Provider.</span></span>
    -   <span data-ttu-id="4c57c-118">"adsdatasource" è l' **\_ argomento dell'origine dati**, ovvero il nome dell'origine dati interpretato dal provider OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4c57c-118">"adsdatasource" is the **data\_source argument**, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

    <span data-ttu-id="4c57c-119">È ora possibile usare il server collegato per accedere a Active Directory da SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4c57c-119">You can now use the linked server to access Active Directory from SQL Server.</span></span>

4.  <span data-ttu-id="4c57c-120">Nell'esempio successivo viene eseguita una query utilizzando l'istruzione [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4c57c-120">The next example performs a query using the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="4c57c-121">Questa istruzione ha due argomenti: ADSI, ovvero il nome del server collegato appena creato e un'istruzione di query.</span><span class="sxs-lookup"><span data-stu-id="4c57c-121">This statement has two arguments: ADSI, which is the name of the linked server that you just created, and a query statement.</span></span> <span data-ttu-id="4c57c-122">L'istruzione di query contiene gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c57c-122">The query statement contains the following items:</span></span>

    -   <span data-ttu-id="4c57c-123">L'istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene l'elenco dei dati che verranno ottenuti dal servizio directory.</span><span class="sxs-lookup"><span data-stu-id="4c57c-123">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="4c57c-124">È necessario usare il nome visualizzato LDAP per indicare i dati che si stanno cercando.</span><span class="sxs-lookup"><span data-stu-id="4c57c-124">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
    -   <span data-ttu-id="4c57c-125">L'istruzione [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene il nome del server di directory collegato da cui verranno ottenute queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="4c57c-125">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
    -   <span data-ttu-id="4c57c-126">L'istruzione [where](https://msdn.microsoft.com/library/Aa260674.aspx) fornisce le condizioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4c57c-126">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="4c57c-127">In questo esempio è in corso la ricerca di utenti.</span><span class="sxs-lookup"><span data-stu-id="4c57c-127">In this example, it is searching for users.</span></span>

    <span data-ttu-id="4c57c-128">Digitare ed eseguire:</span><span class="sxs-lookup"><span data-stu-id="4c57c-128">Type and execute:</span></span>

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    <span data-ttu-id="4c57c-129">È anche possibile usare il [dialetto ADSI LDAP](ldap-dialect.md).</span><span class="sxs-lookup"><span data-stu-id="4c57c-129">You can also use the ADSI [LDAP dialect](ldap-dialect.md).</span></span> <span data-ttu-id="4c57c-130">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4c57c-130">For example:</span></span>

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    <span data-ttu-id="4c57c-131">Nell'esempio precedente la query LDAP è costituita da quattro parti:</span><span class="sxs-lookup"><span data-stu-id="4c57c-131">In the previous example, the LDAP query has four parts:</span></span>

    -   <span data-ttu-id="4c57c-132">" <LDAP://DC=Fabrikam,DC=COM> " è il nome distinto del server di directory in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="4c57c-132">"<LDAP://DC=Fabrikam,DC=COM>" is the distinguished name of the directory server to search.</span></span>
    -   <span data-ttu-id="4c57c-133">"(& (objectCategory = person) (objectClass = user))" è il filtro di ricerca LDAP (vedere la [sintassi del filtro di ricerca](search-filter-syntax.md)).</span><span class="sxs-lookup"><span data-stu-id="4c57c-133">"(&(objectCategory=Person)(objectClass=user))" is the LDAP search filter (see [Search Filter Syntax](search-filter-syntax.md)).</span></span>
    -   <span data-ttu-id="4c57c-134">"Name, ADsPath" sono i nomi (usando il formato del nome visualizzato LDAP) degli attributi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="4c57c-134">"name, adspath" are the names (using the LDAP display name format) of the attributes to retrieve.</span></span>
    -   <span data-ttu-id="4c57c-135">"sottoalbero" indica l' [ambito](scope-of-query.md) della ricerca.</span><span class="sxs-lookup"><span data-stu-id="4c57c-135">"subtree" indicates the [scope](scope-of-query.md) of the search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c57c-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c57c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c57c-137">Creazione ed esecuzione di una visualizzazione</span><span class="sxs-lookup"><span data-stu-id="4c57c-137">Creating and Executing a View</span></span>](creating-and-executing-a-view.md)
</dt> </dl>

 

 




