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
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a>Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice

Sono disponibili diversi modi per utilizzare la ricerca di Windows per eseguire una query sull'indice. Questo argomento descrive gli approcci basati su AQS (Advanced Query Syntax) e Structured Query Language (SQL).

Questo argomento è organizzato nel modo seguente:

- [Query basate su SQL](#sql-based-queries)
  - [Utilizzo di OLE DB](#using-ole-db)
  - [Utilizzo di ADO e ADO.NET](#using-ado-and-adonet)
  - [Uso di SQL in query locali e remote](#using-sql-in-local-and-remote-queries)
- [Query basate su AQS](#aqs-based-queries)
  - [Uso di ISearchQueryHelper](#using-isearchqueryhelper)
  - [Uso del protocollo search-ms](#using-the-search-ms-protocol)
- [Argomenti correlati](#related-topics)

## <a name="sql-based-queries"></a>Query basate su SQL

SQL è un linguaggio testuale che definisce le query. SQL è comune in molte tecnologie di database diverse. Windows Search USA SQL, ne implementa un subset e lo estende aggiungendo elementi al linguaggio. Windows Search SQL usato da Windows Search estende le parti della sintassi di query di database SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo. Tutte le funzionalità di Windows Search SQL sono compatibili con Windows Search in Windows XP e Windows Server 2003 e versioni successive.

Per ulteriori informazioni sull'utilizzo della sintassi SQL di Windows Search, vedere [esecuzione di query sull'indice con la sintassi](-search-sql-windowssearch-entry.md) SQL di ricerca di Windows e [Panoramica della sintassi SQL di Windows Search](-search-sql-ovwofsearchquery.md).

Gli approcci seguenti per l'esecuzione di query sull'indice sono basati su SQL.

### <a name="using-ole-db"></a>Utilizzo di OLE DB

Il collegamento a oggetti e il database di incorporamento (OLE DB) è un'API Component Object Model (COM) che consente di accedere a diversi tipi di archivi dati in modo uniforme, inclusi i database non relazionali come i fogli di calcolo. OLE DB separa l'archivio dati dall'applicazione che vi accede tramite un set di astrazioni che includono l'origine dati della shell, la sessione, il comando e i set di righe. Un provider OLE DB è un componente software che implementa l'interfaccia OLE DB per fornire dati alle applicazioni da un archivio dati specifico.

È possibile accedere al provider di OLE DB di ricerca di Windows a livello di codice utilizzando gli oggetti OleDbConnection e OleDbSession in C \# e utilizzando il supporto OLE DB incorporato in Active Template Library (ATL) in C++ (tramite atlclidb. h). L'unica proprietà che deve essere impostata è la stringa del provider.

È possibile usare la stringa seguente:

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

In alternativa, è possibile ottenere la stringa di connessione chiamando [**ISearchQueryHelper:: Get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring). Per un esempio, vedere uso di [ISearchQueryHelper](#using-isearchqueryhelper) .

> [!Note]  
> Il provider di OLE DB di ricerca di Windows è di sola lettura e supporta le istruzioni SELECT e GROUP ON. Le istruzioni INSERT e DELETE non sono supportate.

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

Per ulteriori informazioni su OLE DB, vedere [Cenni preliminari sulla programmazione OLE DB](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx). Per informazioni sul provider di dati di .NET Framework per OLE DB, vedere la documentazione [dello spazio dei nomi System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .

### <a name="using-ado-and-adonet"></a>Utilizzo di ADO e ADO.NET

Microsoft ActiveX Data Objects (ADO) e ADO.NET consentono di scrivere applicazioni client per accedere e modificare i dati in un server di database tramite un provider. Windows Search è una tecnologia di sola lettura: è possibile recuperare i dati utilizzando la ricerca desktop, ma non è possibile modificare i dati utilizzando Windows Search. È tuttavia possibile passare i risultati di una ricerca a una tecnologia in grado di modificare i dati.

Negli esempi di codice seguenti viene illustrato come aprire una connessione all'origine dati, creare e aprire un RecordSet con un'istruzione SQL SELECT di [Windows Search](-search-sql-ovwofsearchquery.md) e ottenere gli URL dei cinque file più grandi dall'indice.

> [!Note]  
> Per informazioni su come ottenere la stringa di connessione, vedere [esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)e [ISearchQueryHelper:: Get \_ Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).

#### <a name="ado-and-vbscript"></a>ADO e VBScript

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

#### <a name="ado-and-c"></a>ADO e C++

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

#### <a name="ado-and-visualbasic"></a>ADO e VisualBasic

Aggiungere prima di tutto un riferimento a ADODB nel progetto

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

#### <a name="adonet-and-c"></a>ADO.NET e C\#

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

### <a name="using-sql-in-local-and-remote-queries"></a>Uso di SQL in query locali e remote

È possibile eseguire le query in locale o in remoto. Nell'esempio seguente viene illustrata una query locale che usa la [clausola from](-search-sql-from.md) . Una query locale esegue una query solo nel catalogo SystemIndex locale.

```sql
FROM SystemIndex
```

Nell'esempio seguente viene illustrata una query remota che usa la [clausola from](-search-sql-from.md) . L'aggiunta di ComputerName trasforma l'esempio precedente in una query remota.

```sql
FROM [<ComputerName>.]SystemIndex
```

Per impostazione predefinita, Windows XP e Windows Server 2003 non hanno installato Windows Search. Solo Windows Search 4 (WS4) fornisce il supporto per le query remote. Le versioni precedenti di Windows Desktop Search (WDS), ad esempio 3,01 e versioni precedenti, non supportano l'esecuzione di query remote. Con Esplora risorse è possibile eseguire una query sull'indice locale di un computer remoto per file system elementi (elementi gestiti dal protocollo "file:").

Per recuperare un elemento in base a una query remota, è necessario che l'elemento soddisfi i requisiti seguenti:

- Essere accessibile tramite il percorso Universal Naming Convention (UNC).
- Esistere nel computer remoto a cui il client ha accesso.
- Impostare la sicurezza per consentire al client di disporre dell'accesso in lettura.

Esplora risorse include funzionalità per la condivisione di elementi, tra cui una condivisione "pubblica" ( \\ \\ computer \\ pubblico \\ ...) nel **centro di rete e condivisione** e una condivisione "Users" ( \\ \\ \\ utenti computer \\ ...) per gli elementi condivisi tramite la procedura guidata di condivisione. Una volta condivise le cartelle, è possibile eseguire una query sull'indice locale specificando il nome computer del computer remoto nella clausola FROM e un percorso UNC nel computer remoto nella clausola SCOPE, come illustrato nell'esempio seguente:

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a>Query basate su AQS

AQS è la sintassi di query predefinita utilizzata da Windows Search per eseguire una query sull'indice e per perfezionare e restringere i parametri di ricerca. Sebbene AQS sia principalmente utente, può essere utilizzato dagli sviluppatori per compilare query a livello di codice. In Windows 7 Canonical AQS è stato introdotto e deve essere usato in Windows 7 e versioni successive per generare query AQS a livello di codice. Per informazioni dettagliate su AQS, vedere [uso della sintassi avanzata delle query a livello di codice](-search-3x-advancedquerysyntax.md).

Gli approcci seguenti per l'esecuzione di query sull'indice sono basati su AQS.

### <a name="using-isearchqueryhelper"></a>Uso di ISearchQueryHelper

È possibile sviluppare una classe componente o helper per eseguire una query sull'indice usando l'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , che consente di sfruttare alcune funzionalità del sistema e di semplificare l'uso di Windows Search. Questa interfaccia consente di:

- Ottenere una stringa di connessione OLE DB per connettersi al database di Windows Search.
- Consente di convertire le query utente da AQS a SQL Search di Windows.

Questa interfaccia viene implementata come classe helper per [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) ed è ottenuta tramite la chiamata a [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), come illustrato nel seguente esempio di C++.

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

Per implementare l'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , vedere [uso dell'interfaccia ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md) e dell'argomento di riferimento [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .

> [!Note]  
> Compatibilità con le versioni precedenti di Microsoft Windows Desktop Search (WDS) 2x: nei computer che eseguono Windows XP e Windows Server 2003 e versioni successive, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) è deprecato. Gli sviluppatori devono invece usare [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) per ottenere una stringa di connessione, analizzare la query dell'utente in SQL e quindi eseguire query OLE DB.

### <a name="using-the-search-ms-protocol"></a>Uso del protocollo search-ms

Il [protocollo di applicazione](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) **search-ms** è una convenzione per l'avvio di un'applicazione, ad esempio Esplora risorse, per eseguire query sull'indice di ricerca di Windows. Consente la compilazione di query con argomenti di valore di parametro, inclusi argomenti di proprietà, ricerche salvate in precedenza, sintassi di query avanzate (AQS), sintassi di query naturale (NQS) e identificatori di codice della lingua (LCID) sia per l'indicizzatore che per la query stessa.

Per informazioni dettagliate sulla sintassi del protocollo search-ms, vedere [esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Uso della sintassi avanzata delle query a livello di codice](-search-3x-advancedquerysyntax.md)
</dt> </dl>
