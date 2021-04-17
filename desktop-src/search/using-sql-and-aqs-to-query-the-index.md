---
description: Sono disponibili diversi modi per utilizzare la ricerca di Windows per eseguire una query sull'indice. Questo argomento descrive gli approcci basati su AQS (Advanced Query Syntax) e Structured Query Language (SQL).
ms.assetid: 544f03b3-cdf8-4550-a6da-e4a3bfc44744
title: Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641bea0e6109182b5896aa1f0f981695fd91b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306067"
---
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a><span data-ttu-id="cc558-104">Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice</span><span class="sxs-lookup"><span data-stu-id="cc558-104">Using SQL and AQS Approaches to Query the Index</span></span>

<span data-ttu-id="cc558-105">Sono disponibili diversi modi per utilizzare la ricerca di Windows per eseguire una query sull'indice.</span><span class="sxs-lookup"><span data-stu-id="cc558-105">There are several ways to use Windows Search to query the index.</span></span> <span data-ttu-id="cc558-106">Questo argomento descrive gli approcci basati su AQS (Advanced Query Syntax) e Structured Query Language (SQL).</span><span class="sxs-lookup"><span data-stu-id="cc558-106">This topic outlines Advanced Query Syntax (AQS) and Structured Query Language (SQL) based approaches.</span></span>

<span data-ttu-id="cc558-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="cc558-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="cc558-108">Query basate su SQL</span><span class="sxs-lookup"><span data-stu-id="cc558-108">SQL Based Queries</span></span>](#sql-based-queries)
  - [<span data-ttu-id="cc558-109">Utilizzo di OLE DB</span><span class="sxs-lookup"><span data-stu-id="cc558-109">Using OLE DB</span></span>](#using-ole-db)
  - [<span data-ttu-id="cc558-110">Utilizzo di ADO e ADO.NET</span><span class="sxs-lookup"><span data-stu-id="cc558-110">Using ADO and ADO.NET</span></span>](#using-ado-and-adonet)
  - [<span data-ttu-id="cc558-111">Uso di SQL in query locali e remote</span><span class="sxs-lookup"><span data-stu-id="cc558-111">Using SQL in Local and Remote Queries</span></span>](#using-sql-in-local-and-remote-queries)
- [<span data-ttu-id="cc558-112">Query basate su AQS</span><span class="sxs-lookup"><span data-stu-id="cc558-112">AQS Based Queries</span></span>](#aqs-based-queries)
  - [<span data-ttu-id="cc558-113">Uso di ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="cc558-113">Using ISearchQueryHelper</span></span>](#using-isearchqueryhelper)
  - [<span data-ttu-id="cc558-114">Uso del protocollo search-ms</span><span class="sxs-lookup"><span data-stu-id="cc558-114">Using the search-ms Protocol</span></span>](#using-the-search-ms-protocol)
- [<span data-ttu-id="cc558-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc558-115">Related topics</span></span>](#related-topics)

## <a name="sql-based-queries"></a><span data-ttu-id="cc558-116">Query basate su SQL</span><span class="sxs-lookup"><span data-stu-id="cc558-116">SQL Based Queries</span></span>

<span data-ttu-id="cc558-117">SQL è un linguaggio testuale che definisce le query.</span><span class="sxs-lookup"><span data-stu-id="cc558-117">SQL is a text language that defines queries.</span></span> <span data-ttu-id="cc558-118">SQL è comune in molte tecnologie di database diverse.</span><span class="sxs-lookup"><span data-stu-id="cc558-118">SQL is common across many different database technologies.</span></span> <span data-ttu-id="cc558-119">Windows Search USA SQL, ne implementa un subset e lo estende aggiungendo elementi al linguaggio.</span><span class="sxs-lookup"><span data-stu-id="cc558-119">Windows Search uses SQL, implements a subset of it, and extends it by adding elements to the language.</span></span> <span data-ttu-id="cc558-120">Windows Search SQL usato da Windows Search estende le parti della sintassi di query di database SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo.</span><span class="sxs-lookup"><span data-stu-id="cc558-120">The Windows Search SQL used by Windows Search extends portions of the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span> <span data-ttu-id="cc558-121">Tutte le funzionalità di Windows Search SQL sono compatibili con Windows Search in Windows XP e Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc558-121">All features of Windows Search SQL are compatible with Windows Search on Windows XP and Windows Server 2003, and later.</span></span>

<span data-ttu-id="cc558-122">Per ulteriori informazioni sull'utilizzo della sintassi SQL di Windows Search, vedere [esecuzione di query sull'indice con la sintassi](-search-sql-windowssearch-entry.md) SQL di ricerca di Windows e [Panoramica della sintassi SQL di Windows Search](-search-sql-ovwofsearchquery.md).</span><span class="sxs-lookup"><span data-stu-id="cc558-122">For more information about using Windows Search SQL syntax, see [Querying the Index with Windows Search SQL Syntax](-search-sql-windowssearch-entry.md) and [Overview of Windows Search SQL Syntax](-search-sql-ovwofsearchquery.md).</span></span>

<span data-ttu-id="cc558-123">Gli approcci seguenti per l'esecuzione di query sull'indice sono basati su SQL.</span><span class="sxs-lookup"><span data-stu-id="cc558-123">The following approaches for querying the index are SQL based.</span></span>

### <a name="using-ole-db"></a><span data-ttu-id="cc558-124">Utilizzo di OLE DB</span><span class="sxs-lookup"><span data-stu-id="cc558-124">Using OLE DB</span></span>

<span data-ttu-id="cc558-125">Il collegamento a oggetti e il database di incorporamento (OLE DB) è un'API Component Object Model (COM) che consente di accedere a diversi tipi di archivi dati in modo uniforme, inclusi i database non relazionali come i fogli di calcolo.</span><span class="sxs-lookup"><span data-stu-id="cc558-125">The Object Linking and Embedding Database (OLE DB) is a Component Object Model (COM) API that enables you to access different types of data stores uniformly, including non-relational databases like spreadsheets.</span></span> <span data-ttu-id="cc558-126">OLE DB separa l'archivio dati dall'applicazione che vi accede tramite un set di astrazioni che includono l'origine dati della shell, la sessione, il comando e i set di righe.</span><span class="sxs-lookup"><span data-stu-id="cc558-126">OLE DB separates the data store from the application accessing it through a set of abstractions that include the Shell data source, session, command, and rowsets.</span></span> <span data-ttu-id="cc558-127">Un provider OLE DB è un componente software che implementa l'interfaccia OLE DB per fornire dati alle applicazioni da un archivio dati specifico.</span><span class="sxs-lookup"><span data-stu-id="cc558-127">An OLE DB provider is a software component that implements the OLE DB interface to provide data to applications from a particular data store.</span></span>

<span data-ttu-id="cc558-128">È possibile accedere al provider di OLE DB di ricerca di Windows a livello di codice utilizzando gli oggetti OleDbConnection e OleDbSession in C \# e utilizzando il supporto OLE DB incorporato in Active Template Library (ATL) in C++ (tramite atlclidb. h).</span><span class="sxs-lookup"><span data-stu-id="cc558-128">You can access the Windows Search OLE DB provider programmatically by using the OleDbConnection and OleDbSession objects in C\# and by using the OLE DB support built into Active Template Library (ATL) in C++ (via atlclidb.h).</span></span> <span data-ttu-id="cc558-129">L'unica proprietà che deve essere impostata è la stringa del provider.</span><span class="sxs-lookup"><span data-stu-id="cc558-129">The only property that has to be set is the provider string.</span></span>

<span data-ttu-id="cc558-130">È possibile usare la stringa seguente:</span><span class="sxs-lookup"><span data-stu-id="cc558-130">You can use the following string:</span></span>

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

<span data-ttu-id="cc558-131">In alternativa, è possibile ottenere la stringa di connessione chiamando [**ISearchQueryHelper:: Get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="cc558-131">Alternatively, you can get the connection string by calling [**ISearchQueryHelper::get\_ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span> <span data-ttu-id="cc558-132">Per un esempio, vedere uso di [ISearchQueryHelper](#using-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="cc558-132">See Using [ISearchQueryHelper](#using-isearchqueryhelper) for an example.</span></span>

> [!Note]  
> <span data-ttu-id="cc558-133">Il provider di OLE DB di ricerca di Windows è di sola lettura e supporta le istruzioni SELECT e GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="cc558-133">The Windows Search OLE DB provider is read-only, and support SELECT and GROUP ON statements.</span></span> <span data-ttu-id="cc558-134">Le istruzioni INSERT e DELETE non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="cc558-134">INSERT and DELETE statements are not supported.</span></span>

```cpp
#include <atldbcli.h>
CDataSource cDataSource;
hr = cDataSource.OpenFromInitializationString(L"provider=Search.CollatorDSO.1;EXTENDED PROPERTIES=\"Application=Windows\"");

if (SUCCEEDED(hr))
{
    CSession cSession;
    hr = cSession.Open(cDataSource);

    if (SUCCEEDED(hr))
    {
        CCommand<CDynamicAccessor, CRowset> cCommand;
        hr = cCommand.Open(cSession, pszSQL);

        if (SUCCEEDED(hr))
        {
            for (hr = cCommand.MoveFirst(); S_OK == hr; hr = cCommand.MoveNext())
            {
                for (DBORDINAL i = 1; i <= cCommand.GetColumnCount(); i++)
                {
                    PCWSTR pszName = cCommand.GetColumnName(i);
                    // do something with the column here
                }
            }
            cCommand.Close();
        }
    }
}
```

<span data-ttu-id="cc558-135">Per ulteriori informazioni su OLE DB, vedere [Cenni preliminari sulla programmazione OLE DB](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="cc558-135">For more information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span></span> <span data-ttu-id="cc558-136">Per informazioni sul provider di dati di .NET Framework per OLE DB, vedere la documentazione [dello spazio dei nomi System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .</span><span class="sxs-lookup"><span data-stu-id="cc558-136">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) documentation.</span></span>

### <a name="using-ado-and-adonet"></a><span data-ttu-id="cc558-137">Utilizzo di ADO e ADO.NET</span><span class="sxs-lookup"><span data-stu-id="cc558-137">Using ADO and ADO.NET</span></span>

<span data-ttu-id="cc558-138">Microsoft ActiveX Data Objects (ADO) e ADO.NET consentono di scrivere applicazioni client per accedere e modificare i dati in un server di database tramite un provider.</span><span class="sxs-lookup"><span data-stu-id="cc558-138">Microsoft ActiveX Data Objects (ADO) and ADO.NET enable you to write client applications to access and manipulate data in a database server through a provider.</span></span> <span data-ttu-id="cc558-139">Windows Search è una tecnologia di sola lettura: è possibile recuperare i dati utilizzando la ricerca desktop, ma non è possibile modificare i dati utilizzando Windows Search.</span><span class="sxs-lookup"><span data-stu-id="cc558-139">Windows Search is a read-only technology: you can retrieve data using Desktop Search but you can't change data using Windows Search.</span></span> <span data-ttu-id="cc558-140">È tuttavia possibile passare i risultati di una ricerca a una tecnologia in grado di modificare i dati.</span><span class="sxs-lookup"><span data-stu-id="cc558-140">You can, however, pass the results of a search over to a technology that can change data.</span></span>

<span data-ttu-id="cc558-141">Negli esempi di codice seguenti viene illustrato come aprire una connessione all'origine dati, creare e aprire un RecordSet con un'istruzione SQL SELECT di [Windows Search](-search-sql-ovwofsearchquery.md) e ottenere gli URL dei cinque file più grandi dall'indice.</span><span class="sxs-lookup"><span data-stu-id="cc558-141">The following code examples demonstrate how to open a connection to the data source, create and open a RecordSet with a [Windows Search SQL](-search-sql-ovwofsearchquery.md) SELECT statement, and get the URLs of the five largest files from the index.</span></span>

> [!Note]  
> <span data-ttu-id="cc558-142">Per informazioni su come ottenere la stringa di connessione, vedere [esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)e [ISearchQueryHelper:: Get \_ Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="cc558-142">For information on how to obtain the connection string, see [Querying the Index with ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md), and [ISearchQueryHelper::get\_Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span>

#### <a name="ado-and-vbscript"></a><span data-ttu-id="cc558-143">ADO e VBScript</span><span class="sxs-lookup"><span data-stu-id="cc558-143">ADO and VBScript</span></span>

```VB
'To run this snippet, save it to a file and run it using cscript.exe from a command line.
'Running the .vbs file with Windows Script Host may cause dialog boxes to open for each item returned from the index.

On Error Resume Next

Set objConnection = CreateObject("ADODB.Connection")
Set objRecordSet = CreateObject("ADODB.Recordset")

objConnection.Open "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"

objRecordSet.Open "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC", objConnection

objRecordSet.MoveFirst
Do Until objRecordset.EOF
    Wscript.Echo objRecordset.Fields.Item("System.ItemPathDisplay")
    objRecordset.MoveNext
Loop
```

#### <a name="ado-and-c"></a><span data-ttu-id="cc558-144">ADO e C++</span><span class="sxs-lookup"><span data-stu-id="cc558-144">ADO and C++</span></span>

```cpp
#import "msado15.dll" rename_namespace("ADO") rename("EOF", "EndOfFile") implementation_only

ADO::_ConnectionPtr connection = NULL;
HRESULT hr = connection.CreateInstance(__uuidof(ADO::Connection));
if (SUCCEEDED(hr))
{
    ADO::_RecordsetPtr recordset = NULL;
    hr = recordset.CreateInstance(__uuidof(ADO::Recordset));
    if (SUCCEEDED(hr))
    {
        connection->CursorLocation = ADO::adUseClient;
        hr = connection->Open(L"Provider=Search.CollatorDSO;Extended Properties='Application=Windows';",
            L"", L"", ADO::adConnectUnspecified);
        if (SUCCEEDED(hr))
        {
            hr = recordset->Open("SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC",
            connection.GetInterfacePtr(), ADO::adOpenForwardOnly, ADO::adLockReadOnly, ADO::adCmdText);
            if (SUCCEEDED(hr))
            {
                while (!recordset->EndOfFile)
                {
                    _variant_t var;
                    var = recordset->Fields->GetItem(L"System.ItemPathDisplay")->GetValue();
                    std::cout << static_cast<char *>(_bstr_t(var.bstrVal)) << std::endl;
                    recordset->MoveNext();
                };
                recordset->Close();
            }
            connection->Close();
        }
    }
}

```

#### <a name="ado-and-visualbasic"></a><span data-ttu-id="cc558-145">ADO e VisualBasic</span><span class="sxs-lookup"><span data-stu-id="cc558-145">ADO and VisualBasic</span></span>

<span data-ttu-id="cc558-146">Aggiungere prima di tutto un riferimento a ADODB nel progetto</span><span class="sxs-lookup"><span data-stu-id="cc558-146">First add a reference to ADODB in your project</span></span>

```VB
Dim con As ADODB.Connection
Dim rst As ADODB.Recordset

con = New ADODB.Connection
rst = New ADODB.Recordset

Dim sConString As String
Dim sSQLString As String

sConString = "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"
con.Open(sConString)

sSQLString = "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC"

rst = con.Execute(sSQLString)

Do Until (rst.EOF)
    Print(1, rst("System.ItemPathDisplay").Value)
    rst.MoveNext
Loop

rst.Close
rst = Nothing

con.Close
con = Nothing
```

#### <a name="adonet-and-c"></a><span data-ttu-id="cc558-147">ADO.NET e C\#</span><span class="sxs-lookup"><span data-stu-id="cc558-147">ADO.NET and C\#</span></span>

```csharp
string query = @"SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC";

using (OleDbConnection objConnection =
    new OleDbConnection
    ("Provider=Search.CollatorDSO.1;Extended?Properties='Application=Windows';"))
{
    objConnection.Open();
    OleDbCommand cmd = new OleDbCommand(query, objConnection);
    using (OleDbDataReader rdr = cmd.ExecuteReader())
    {
        for (int i = 0; i < rdr.FieldCount; i++)
        {
            Console.Write(rdr.GetName(i));
            Console.Write('\t');
        }
        while (rdr.Read())
        {
            Console.WriteLine();
            for (int i = 0; i < rdr.FieldCount; i++)
            {
                Console.Write(rdr[i]);
                Console.Write('\t');
            }
        }
        Console.ReadKey();
    }
}
```

### <a name="using-sql-in-local-and-remote-queries"></a><span data-ttu-id="cc558-148">Uso di SQL in query locali e remote</span><span class="sxs-lookup"><span data-stu-id="cc558-148">Using SQL in Local and Remote Queries</span></span>

<span data-ttu-id="cc558-149">È possibile eseguire le query in locale o in remoto.</span><span class="sxs-lookup"><span data-stu-id="cc558-149">You can execute your queries either locally or remotely.</span></span> <span data-ttu-id="cc558-150">Nell'esempio seguente viene illustrata una query locale che usa la [clausola from](-search-sql-from.md) .</span><span class="sxs-lookup"><span data-stu-id="cc558-150">A local query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="cc558-151">Una query locale esegue una query solo nel catalogo SystemIndex locale.</span><span class="sxs-lookup"><span data-stu-id="cc558-151">A local query queries the local SystemIndex catalog only.</span></span>

```sql
FROM SystemIndex
```

<span data-ttu-id="cc558-152">Nell'esempio seguente viene illustrata una query remota che usa la [clausola from](-search-sql-from.md) .</span><span class="sxs-lookup"><span data-stu-id="cc558-152">A remote query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="cc558-153">L'aggiunta di ComputerName trasforma l'esempio precedente in una query remota.</span><span class="sxs-lookup"><span data-stu-id="cc558-153">Adding ComputerName transforms the previous example into a remote query.</span></span>

```sql
FROM [<ComputerName>.]SystemIndex
```

<span data-ttu-id="cc558-154">Per impostazione predefinita, Windows XP e Windows Server 2003 non hanno installato Windows Search.</span><span class="sxs-lookup"><span data-stu-id="cc558-154">By default, Windows XP and Windows Server 2003 do not have Windows Search installed.</span></span> <span data-ttu-id="cc558-155">Solo Windows Search 4 (WS4) fornisce il supporto per le query remote.</span><span class="sxs-lookup"><span data-stu-id="cc558-155">Only Windows Search 4 (WS4) provides remote query support.</span></span> <span data-ttu-id="cc558-156">Le versioni precedenti di Windows Desktop Search (WDS), ad esempio 3,01 e versioni precedenti, non supportano l'esecuzione di query remote.</span><span class="sxs-lookup"><span data-stu-id="cc558-156">Previous versions of Windows Desktop Search (WDS), such as 3.01 and earlier, do not support remote querying.</span></span> <span data-ttu-id="cc558-157">Con Esplora risorse è possibile eseguire una query sull'indice locale di un computer remoto per file system elementi (elementi gestiti dal protocollo "file:").</span><span class="sxs-lookup"><span data-stu-id="cc558-157">With Windows Explorer you can query the local index of a remote computer for file system items (items handled by the "file:" protocol).</span></span>

<span data-ttu-id="cc558-158">Per recuperare un elemento in base a una query remota, è necessario che l'elemento soddisfi i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc558-158">To retrieve an item by remote query, the item must meet the following requirements:</span></span>

- <span data-ttu-id="cc558-159">Essere accessibile tramite il percorso Universal Naming Convention (UNC).</span><span class="sxs-lookup"><span data-stu-id="cc558-159">Be accessible via Universal Naming Convention (UNC) path.</span></span>
- <span data-ttu-id="cc558-160">Esistere nel computer remoto a cui il client ha accesso.</span><span class="sxs-lookup"><span data-stu-id="cc558-160">Exist on the remote computer to which the client has access.</span></span>
- <span data-ttu-id="cc558-161">Impostare la sicurezza per consentire al client di disporre dell'accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="cc558-161">Have its security set to allow the client to have Read access.</span></span>

<span data-ttu-id="cc558-162">Esplora risorse include funzionalità per la condivisione di elementi, tra cui una condivisione "pubblica" ( \\ \\ computer \\ pubblico \\ ...) nel **centro di rete e condivisione** e una condivisione "Users" ( \\ \\ \\ utenti computer \\ ...) per gli elementi condivisi tramite la procedura guidata di condivisione.</span><span class="sxs-lookup"><span data-stu-id="cc558-162">Windows Explorer has features for sharing items including a "Public" share (\\\\Machine\\Public\\...) in the **Network and Sharing Center**, and a "Users" share (\\\\Machine\\Users\\...) for items shared through the Sharing Wizard.</span></span> <span data-ttu-id="cc558-163">Una volta condivise le cartelle, è possibile eseguire una query sull'indice locale specificando il nome computer del computer remoto nella clausola FROM e un percorso UNC nel computer remoto nella clausola SCOPE, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="cc558-163">After you share the folder(s), you can query the local index by specifying the remote computer's machine name in the FROM clause, and a UNC path on the remote machine in the SCOPE clause, as shown in the following example:</span></span>

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a><span data-ttu-id="cc558-164">Query basate su AQS</span><span class="sxs-lookup"><span data-stu-id="cc558-164">AQS Based Queries</span></span>

<span data-ttu-id="cc558-165">AQS è la sintassi di query predefinita utilizzata da Windows Search per eseguire una query sull'indice e per perfezionare e restringere i parametri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cc558-165">AQS is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="cc558-166">Sebbene AQS sia principalmente utente, può essere utilizzato dagli sviluppatori per compilare query a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="cc558-166">While AQS is primarily user facing, it can be used by developers to build queries programmatically.</span></span> <span data-ttu-id="cc558-167">In Windows 7 Canonical AQS è stato introdotto e deve essere usato in Windows 7 e versioni successive per generare query AQS a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="cc558-167">In Windows 7 canonical AQS was introduced, and must be used in Windows 7 and later, to programmatically generate AQS queries.</span></span> <span data-ttu-id="cc558-168">Per informazioni dettagliate su AQS, vedere [uso della sintassi avanzata delle query a livello di codice](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="cc558-168">For detailed information on AQS, see [Using Advanced Query Syntax Programmatically](-search-3x-advancedquerysyntax.md).</span></span>

<span data-ttu-id="cc558-169">Gli approcci seguenti per l'esecuzione di query sull'indice sono basati su AQS.</span><span class="sxs-lookup"><span data-stu-id="cc558-169">The following approaches for querying the index are AQS based.</span></span>

### <a name="using-isearchqueryhelper"></a><span data-ttu-id="cc558-170">Uso di ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="cc558-170">Using ISearchQueryHelper</span></span>

<span data-ttu-id="cc558-171">È possibile sviluppare una classe componente o helper per eseguire una query sull'indice usando l'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , che consente di sfruttare alcune funzionalità del sistema e di semplificare l'uso di Windows Search.</span><span class="sxs-lookup"><span data-stu-id="cc558-171">You can develop a component or helper class to query the index by using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, which enables you to take advantage of some features of the system and simplify your use of Windows Search.</span></span> <span data-ttu-id="cc558-172">Questa interfaccia consente di:</span><span class="sxs-lookup"><span data-stu-id="cc558-172">This interface helps you:</span></span>

- <span data-ttu-id="cc558-173">Ottenere una stringa di connessione OLE DB per connettersi al database di Windows Search.</span><span class="sxs-lookup"><span data-stu-id="cc558-173">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
- <span data-ttu-id="cc558-174">Consente di convertire le query utente da AQS a SQL Search di Windows.</span><span class="sxs-lookup"><span data-stu-id="cc558-174">Convert user queries from AQS to Windows Search SQL.</span></span>

<span data-ttu-id="cc558-175">Questa interfaccia viene implementata come classe helper per [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) ed è ottenuta tramite la chiamata a [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), come illustrato nel seguente esempio di C++.</span><span class="sxs-lookup"><span data-stu-id="cc558-175">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), as shown in the following C++ example.</span></span>

```cpp
HRESULT GetQueryHelper(ISearchQueryHelper **ppQueryHelper)
{
    *ppQueryHelper = NULL;

    // Create an instance of the search manager

    ISearchManager *pSearchManager;
    HRESULT hr = CoCreateInstance(__uuidof(CSearchManager), NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));
    if (SUCCEEDED(hr))
    {
        // Get the catalog manager from the search manager
        ISearchCatalogManager *pSearchCatalogManager;
        hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
        if (SUCCEEDED(hr))
        {
            // Get the query helper from the catalog manager
            hr = pSearchCatalogManager->GetQueryHelper(ppQueryHelper);
            pSearchCatalogManager->Release();
        }
        pSearchManager->Release();
    }

    return hr;
}
```

<span data-ttu-id="cc558-176">Per implementare l'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , vedere [uso dell'interfaccia ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md) e dell'argomento di riferimento [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="cc558-176">To implement the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, see [Using the ISearchQueryHelper Interface](-search-3x-wds-qryidx-searchqueryhelper.md) and the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) reference topic.</span></span>

> [!Note]  
> <span data-ttu-id="cc558-177">Compatibilità con le versioni precedenti di Microsoft Windows Desktop Search (WDS) 2x: nei computer che eseguono Windows XP e Windows Server 2003 e versioni successive, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) è deprecato.</span><span class="sxs-lookup"><span data-stu-id="cc558-177">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and Windows Server 2003 and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="cc558-178">Gli sviluppatori devono invece usare [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) per ottenere una stringa di connessione, analizzare la query dell'utente in SQL e quindi eseguire query OLE DB.</span><span class="sxs-lookup"><span data-stu-id="cc558-178">Instead, developers should use [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string, parse the user's query into SQL, and then query through OLE DB.</span></span>

### <a name="using-the-search-ms-protocol"></a><span data-ttu-id="cc558-179">Uso del protocollo search-ms</span><span class="sxs-lookup"><span data-stu-id="cc558-179">Using the search-ms Protocol</span></span>

<span data-ttu-id="cc558-180">Il [protocollo di applicazione](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) **search-ms** è una convenzione per l'avvio di un'applicazione, ad esempio Esplora risorse, per eseguire query sull'indice di ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="cc558-180">The **search-ms** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for starting an application, like Windows Explorer, to query the Windows Search index.</span></span> <span data-ttu-id="cc558-181">Consente la compilazione di query con argomenti di valore di parametro, inclusi argomenti di proprietà, ricerche salvate in precedenza, sintassi di query avanzate (AQS), sintassi di query naturale (NQS) e identificatori di codice della lingua (LCID) sia per l'indicizzatore che per la query stessa.</span><span class="sxs-lookup"><span data-stu-id="cc558-181">It enables queries to be built with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="cc558-182">Per informazioni dettagliate sulla sintassi del protocollo search-ms, vedere [esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md).</span><span class="sxs-lookup"><span data-stu-id="cc558-182">For detailed information on the search-ms protocol syntax, see [Querying the Index with the search-ms Protocol](-search-3x-wds-qryidx-searchms.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc558-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc558-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc558-184">Esecuzione di query sull'indice a livello di codice</span><span class="sxs-lookup"><span data-stu-id="cc558-184">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="cc558-185">Esecuzione di query sull'indice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="cc558-185">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="cc558-186">Esecuzione di query sull'indice con il protocollo search-ms</span><span class="sxs-lookup"><span data-stu-id="cc558-186">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="cc558-187">Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="cc558-187">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="cc558-188">Uso della sintassi avanzata delle query a livello di codice</span><span class="sxs-lookup"><span data-stu-id="cc558-188">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>
