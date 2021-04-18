---
description: Le applicazioni WMI scritte in C++ possono eseguire chiamate asincrone utilizzando molti dei metodi dell'interfaccia COM IWbemServices.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Esecuzione di una chiamata asincrona con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318868"
---
# <a name="making-an-asynchronous-call-with-c"></a>Esecuzione di una chiamata asincrona con C++

Le applicazioni WMI scritte in C++ possono eseguire chiamate asincrone utilizzando molti dei metodi dell'interfaccia com [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Tuttavia, la procedura consigliata per chiamare un metodo [*WMI*](gloss-w.md) o un [*metodo del provider*](gloss-p.md) consiste nell'utilizzare chiamate semisincrono perché le chiamate semisincrono sono più sicure delle chiamate asincrone. Per ulteriori informazioni, vedere [creazione di una chiamata semisincrono con C++](making-a-semisynchronous-call-with-c--.md) e [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

Nella procedura riportata di seguito viene descritto come eseguire una chiamata asincrona utilizzando il sink nel processo.

**Per eseguire una chiamata asincrona con C++**

1.  Implementare l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .

    Tutte le applicazioni che effettuano chiamate asincrone devono implementare [**IWbemObjectSink**](iwbemobjectsink.md). I consumer di eventi temporanei implementano anche **IWbemObjectSink** per ricevere la notifica degli eventi.

2.  Accedere allo spazio dei nomi WMI di destinazione.

    Le applicazioni devono sempre chiamare la funzione COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) durante la fase di inizializzazione. In caso contrario prima di effettuare una chiamata asincrona, WMI rilascia il sink dell'applicazione senza completare la chiamata asincrona. Per ulteriori informazioni, vedere [inizializzazione di com per un'applicazione WMI](initializing-com-for-a-wmi-application.md).

3.  Impostare la sicurezza per il sink.

    Le chiamate asincrone creano una serie di problemi di sicurezza che potrebbe essere necessario gestire, ad esempio, per consentire l'accesso WMI all'applicazione. Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

4.  Eseguire la chiamata asincrona.

    Il metodo restituisce immediatamente il codice **di \_ \_ \_ Errore WBEM** . L'applicazione può procedere con altre attività durante l'attesa del completamento dell'operazione. WMI segnala all'applicazione chiamando i metodi nell'implementazione [**IWbemObjectSink**](iwbemobjectsink.md) dell'applicazione.

5.  Se necessario, controllare periodicamente l'implementazione per gli aggiornamenti.

    Le applicazioni possono ricevere notifiche dello stato intermedio impostando il parametro *è* nella chiamata asincrona **allo \_ \_ \_ stato di invio del flag WBEM**. WMI segnala lo stato della chiamata impostando il parametro *è* di [**IWbemObjectSink**](iwbemobjectsink.md) **\_ sullo stato di stato \_ WBEM**.

6.  Se necessario, è possibile annullare la chiamata prima di completare l'elaborazione di WMI chiamando il metodo [**IWbemServices:: CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .

    Il metodo [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) Annulla l'elaborazione asincrona rilasciando immediatamente il puntatore all'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) e garantisce che il puntatore venga rilasciato prima della restituzione di **CancelAsyncCall** .

    Se si usa un oggetto wrapper che implementa l'interfaccia **IUnsecured** per ospitare [**IWbemObjectSink**](iwbemobjectsink.md), è possibile riscontrare alcune complicazioni aggiuntive. Poiché l'applicazione deve passare lo stesso puntatore a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) passato nella chiamata asincrona originale, l'applicazione deve mantenere l'oggetto wrapper fino a quando non diventa chiaro che l'annullamento non è necessario. Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

7.  Al termine, pulire i puntatori e arrestare l'applicazione.

    WMI fornisce la chiamata di stato finale tramite il metodo [**sestatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) .

    > [!Note]  
    > Dopo l'invio dell'aggiornamento dello stato finale, WMI rilascia il sink di oggetto chiamando il metodo **Release** per la classe che implementa l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) . Nell'esempio precedente si tratta del metodo **QuerySink:: Release** . Se si desidera controllare la durata dell'oggetto sink, è possibile implementare il sink con un conteggio dei riferimenti iniziale pari a uno (1).

     

    Se un'applicazione client passa la stessa interfaccia di sink in due diverse chiamate asincrone sovrapposte, WMI non garantisce l'ordine di callback. Un'applicazione client che esegue chiamate asincrone sovrapposte deve passare oggetti sink diversi o serializzare le chiamate.

Nell'esempio seguente sono richieste le seguenti istruzioni Reference e \# include.


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



Nell'esempio seguente viene descritto come eseguire una query asincrona utilizzando il metodo [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) , ma non vengono create impostazioni di sicurezza o viene rilasciato l'oggetto [**IWbemObjectSink**](iwbemobjectsink.md) . Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> Il codice precedente non viene compilato senza errori perché la classe **QuerySink** non è stata definita. Per ulteriori informazioni su **QuerySink**, vedere [**IWbemObjectSink**](iwbemobjectsink.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> </dl>

 

 
