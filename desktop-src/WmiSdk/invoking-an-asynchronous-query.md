---
description: Una query asincrona, sebbene un po' più complessa da scrivere, è il tipo preferito di query quando le prestazioni di sistema o di rete saranno interessate dall'esecuzione di query su un gruppo di dati di grandi dimensioni.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Richiamo di una query asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a0e297c6a1955d0006d888fc95f5e827f5cb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885390"
---
# <a name="invoking-an-asynchronous-query"></a><span data-ttu-id="36e34-103">Richiamo di una query asincrona</span><span class="sxs-lookup"><span data-stu-id="36e34-103">Invoking an Asynchronous Query</span></span>

<span data-ttu-id="36e34-104">Una query asincrona, sebbene un po' più complessa da scrivere, è il tipo preferito di query quando le prestazioni di sistema o di rete saranno interessate dall'esecuzione di query su un gruppo di dati di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="36e34-104">An asynchronous query, while somewhat more complex to write, is the preferred type of query when system or network performance will be affected by querying a large group of data.</span></span> <span data-ttu-id="36e34-105">Nello script, la creazione di un oggetto [**SWbemSink**](swbemsink.md) e subroutine per gestire gli eventi che il sink può ricevere sono le uniche attività aggiuntive oltre la query di base.</span><span class="sxs-lookup"><span data-stu-id="36e34-105">In script, creating an [**SWbemSink**](swbemsink.md) object and subroutines to handle the events that the sink could receive are the only additional tasks beyond the basic query.</span></span>

> [!Note]  
> <span data-ttu-id="36e34-106">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="36e34-106">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="36e34-107">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="36e34-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="36e34-108">Le query script abbreviate seguenti per tutti i file di dati nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="36e34-108">The following abbreviated script queries for all of the data files on the local machine.</span></span> <span data-ttu-id="36e34-109">Questa query potrebbe richiedere una quantità di tempo eccessiva se è stata eseguita per tutti i computer in una rete.</span><span class="sxs-lookup"><span data-stu-id="36e34-109">This query could take an excessive amount of time if it were executed for all of the machines on a network.</span></span> <span data-ttu-id="36e34-110">Viene configurato un oggetto [**SWbemSink**](swbemsink.md) e l'unico evento gestito è l'evento OnCompleted.</span><span class="sxs-lookup"><span data-stu-id="36e34-110">An [**SWbemSink**](swbemsink.md) object is set up and the only event that is handled is the OnCompleted event.</span></span>


```VB
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
    WScript.Echo "Asynchronous operation is done."
End Sub

Set service = GetObject("winmgmts:")
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
service.ExecQueryAsync sink, "SELECT * FROM Win32_DataFile"
WScript.Echo "Waiting for instances."
sink.Cancel()
set sink= Nothing
```



<span data-ttu-id="36e34-111">Per informazioni dettagliate sulla creazione di chiamate di metodo asincrone nello script, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="36e34-111">For detailed information about constructing asynchronous method calls in script, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="36e34-112">Nelle applicazioni C++, una query asincrona genera un processo separato per la ricezione dei dati di query.</span><span class="sxs-lookup"><span data-stu-id="36e34-112">In C++ applications, an asynchronous query spawns a separate process to receive query data.</span></span> <span data-ttu-id="36e34-113">Una query asincrona è più complessa di una query sincrona, in quanto è necessario codificare un'applicazione multithreading.</span><span class="sxs-lookup"><span data-stu-id="36e34-113">An asynchronous query is more complex than a synchronous query, as you must code a multithreaded application.</span></span> <span data-ttu-id="36e34-114">Tuttavia, una query asincrona non monopolizza il thread principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="36e34-114">However, an asynchronous query does not monopolize the main thread of your application.</span></span>

<span data-ttu-id="36e34-115">Nella procedura seguente viene descritto come eseguire una query asincrona in C++.</span><span class="sxs-lookup"><span data-stu-id="36e34-115">The following procedure describes how to perform an asynchronous query in C++.</span></span>

<span data-ttu-id="36e34-116">**Per eseguire una query asincrona in C++**</span><span class="sxs-lookup"><span data-stu-id="36e34-116">**To perform an asynchronous query in C++**</span></span>

1.  <span data-ttu-id="36e34-117">Implementare un oggetto **IWbemSink** .</span><span class="sxs-lookup"><span data-stu-id="36e34-117">Implement an **IWbemSink** object.</span></span>

    <span data-ttu-id="36e34-118">Un oggetto **IWbemSink** riceve informazioni su un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="36e34-118">An **IWbemSink** object receives information about an asynchronous operation.</span></span>

2.  <span data-ttu-id="36e34-119">Descrivere la query in una chiamata a [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span><span class="sxs-lookup"><span data-stu-id="36e34-119">Describe your query in a call to [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span></span>

    <span data-ttu-id="36e34-120">WMI sposta immediatamente il processo che esegue query sul CIM in un altro thread e libera il thread che ha eseguito la query per un'altra attività.</span><span class="sxs-lookup"><span data-stu-id="36e34-120">WMI immediately moves the process that queries the CIM to another thread and frees up the thread that executed the query for another task.</span></span>

3.  <span data-ttu-id="36e34-121">Attendere che WMI chiami il metodo [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="36e34-121">Wait for WMI to call the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

    <span data-ttu-id="36e34-122">Al termine, le chiamate WMI [**indicano**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) a di segnalare all'applicazione che la query è stata completata.</span><span class="sxs-lookup"><span data-stu-id="36e34-122">When finished, WMI calls [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to signal your application that the query is complete.</span></span> <span data-ttu-id="36e34-123">WMI restituisce inoltre i risultati della query al sink come puntatore a un puntatore di interfaccia [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="36e34-123">WMI also returns results of the query to the sink as a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="36e34-124">Come per una query sincrona, usare il puntatore per accedere agli oggetti che costituiscono il risultato della query.</span><span class="sxs-lookup"><span data-stu-id="36e34-124">As with a synchronous query, use the pointer to access the objects that make up the result of your query.</span></span>

<span data-ttu-id="36e34-125">L'esempio di codice seguente non viene compilato senza errori perché la classe QuerySink non è stata definita.</span><span class="sxs-lookup"><span data-stu-id="36e34-125">The following code example does not compile without an error because the class QuerySink has not been defined.</span></span> <span data-ttu-id="36e34-126">Per la definizione della classe QuerySink, vedere [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="36e34-126">For the definition of the QuerySink class, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="36e34-127">L'esempio di codice richiede anche le seguenti istruzioni di riferimento e di \# inclusione.</span><span class="sxs-lookup"><span data-stu-id="36e34-127">The code example also requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="36e34-128">Nell'esempio di codice seguente viene illustrato come eseguire una chiamata asincrona per eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="36e34-128">The following code example shows how to make an asynchronous call to issue a query.</span></span>


```C++
void ExecQuery(IWbemServices *pSvc)
{
    // Create a new sink object.
    QuerySink *pSink = new QuerySink;

    // Initialize the query and query language.
    BSTR strQuery = SysAllocString(L"SELECT * FROM ClassName");
    BSTR strQueryLang = SysAllocString(L"WQL");
    
    // Issue the query.
    HRESULT hRes = pSvc->ExecQueryAsync(strQueryLang, strQuery, 0,
        NULL, pSink);

    // Clean up.
    SysFreeString(strQuery);
    SysFreeString(strQueryLang);
    
    if (hRes)
    {
        printf("ExecQueryAsync failed with = 0x%X\n", hRes);
        return;
    }
    
    printf("Completed.\n");
}
```



<span data-ttu-id="36e34-129">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="36e34-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 



