---
description: Una query asincrona, anche se più complessa da scrivere, è il tipo preferito di query quando le prestazioni di sistema o di rete saranno interessate dall'esecuzione di query su un gruppo di dati di grandi dimensioni.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Chiamata di una query asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ae188e3826562b1de68357db34dca6cea60a40e4be07c16946b13ed3eb3007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993071"
---
# <a name="invoking-an-asynchronous-query"></a>Chiamata di una query asincrona

Una query asincrona, anche se più complessa da scrivere, è il tipo preferito di query quando le prestazioni di sistema o di rete saranno interessate dall'esecuzione di query su un gruppo di dati di grandi dimensioni. Nello script, la creazione di un [**oggetto SWbemSink**](swbemsink.md) e di subroutine per gestire gli eventi che il sink può ricevere sono le uniche attività aggiuntive oltre alla query di base.

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile usare la comunicazione semisincrona anziché asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

 

Lo script abbreviato seguente esegue query per tutti i file di dati nel computer locale. Questa query potrebbe richiedere una quantità eccessiva di tempo se viene eseguita per tutti i computer in una rete. Viene [**configurato un oggetto SWbemSink**](swbemsink.md) e l'unico evento gestito è l'evento OnCompleted.


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



Per informazioni dettagliate sulla costruzione di chiamate asincrone ai metodi nello script, vedere [Chiamata di un metodo](calling-a-method.md).

Nelle applicazioni C++ una query asincrona genera un processo separato per ricevere i dati delle query. Una query asincrona è più complessa di una query sincrona, perché è necessario codificare un'applicazione multithreading. Tuttavia, una query asincrona non monopolizza il thread principale dell'applicazione.

La procedura seguente descrive come eseguire una query asincrona in C++.

**Per eseguire una query asincrona in C++**

1.  Implementare **un oggetto IWbemSink.**

    Un **oggetto IWbemSink** riceve informazioni su un'operazione asincrona.

2.  Descrivere la query in una chiamata a [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).

    WMI sposta immediatamente il processo che esegue query cim su un altro thread e libera il thread che ha eseguito la query per un'altra attività.

3.  Attendere che WMI chiami il [**metodo IWbemObjectSink::Indicate.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)

    Al termine, WMI chiama [**Indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) per segnalare all'applicazione che la query è stata completata. WMI restituisce anche i risultati della query al sink come puntatore a un puntatore a interfaccia [**IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) Come per una query sincrona, usare il puntatore per accedere agli oggetti che costituiscono il risultato della query.

L'esempio di codice seguente non viene compilato senza un errore perché la classe QuerySink non è stata definita. Per la definizione della classe QuerySink, vedere [**IWbemObjectSink**](iwbemobjectsink.md). L'esempio di codice richiede anche le istruzioni reference e \# include seguenti.


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



Nell'esempio di codice seguente viene illustrato come effettuare una chiamata asincrona per eseguire una query.


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



Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

 

 



