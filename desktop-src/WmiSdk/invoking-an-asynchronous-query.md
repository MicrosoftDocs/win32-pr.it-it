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
# <a name="invoking-an-asynchronous-query"></a>Richiamo di una query asincrona

Una query asincrona, sebbene un po' più complessa da scrivere, è il tipo preferito di query quando le prestazioni di sistema o di rete saranno interessate dall'esecuzione di query su un gruppo di dati di grandi dimensioni. Nello script, la creazione di un oggetto [**SWbemSink**](swbemsink.md) e subroutine per gestire gli eventi che il sink può ricevere sono le uniche attività aggiuntive oltre la query di base.

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

Le query script abbreviate seguenti per tutti i file di dati nel computer locale. Questa query potrebbe richiedere una quantità di tempo eccessiva se è stata eseguita per tutti i computer in una rete. Viene configurato un oggetto [**SWbemSink**](swbemsink.md) e l'unico evento gestito è l'evento OnCompleted.


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



Per informazioni dettagliate sulla creazione di chiamate di metodo asincrone nello script, vedere [chiamata a un metodo](calling-a-method.md).

Nelle applicazioni C++, una query asincrona genera un processo separato per la ricezione dei dati di query. Una query asincrona è più complessa di una query sincrona, in quanto è necessario codificare un'applicazione multithreading. Tuttavia, una query asincrona non monopolizza il thread principale dell'applicazione.

Nella procedura seguente viene descritto come eseguire una query asincrona in C++.

**Per eseguire una query asincrona in C++**

1.  Implementare un oggetto **IWbemSink** .

    Un oggetto **IWbemSink** riceve informazioni su un'operazione asincrona.

2.  Descrivere la query in una chiamata a [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).

    WMI sposta immediatamente il processo che esegue query sul CIM in un altro thread e libera il thread che ha eseguito la query per un'altra attività.

3.  Attendere che WMI chiami il metodo [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

    Al termine, le chiamate WMI [**indicano**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) a di segnalare all'applicazione che la query è stata completata. WMI restituisce inoltre i risultati della query al sink come puntatore a un puntatore di interfaccia [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Come per una query sincrona, usare il puntatore per accedere agli oggetti che costituiscono il risultato della query.

L'esempio di codice seguente non viene compilato senza errori perché la classe QuerySink non è stata definita. Per la definizione della classe QuerySink, vedere [**IWbemObjectSink**](iwbemobjectsink.md). L'esempio di codice richiede anche le seguenti istruzioni di riferimento e di \# inclusione.


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



Nell'esempio di codice seguente viene illustrato come eseguire una chiamata asincrona per eseguire una query.


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



Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

 



