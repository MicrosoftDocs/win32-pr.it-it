---
description: Le applicazioni WMI scritte in C++ possono effettuare chiamate asincrone usando molti dei metodi dell'interfaccia COM IWbemServices.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Esecuzione di una chiamata asincrona con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd988382399f3fc377476c486b363cf51db6c4d9ef559c787236e41bb74117a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131193"
---
# <a name="making-an-asynchronous-call-with-c"></a>Esecuzione di una chiamata asincrona con C++

Le applicazioni WMI scritte in C++ possono effettuare chiamate asincrone usando molti dei metodi dell'interfaccia COM [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Tuttavia, la procedura consigliata per chiamare un metodo [*WMI*](gloss-w.md) o un metodo [*provider*](gloss-p.md) è l'uso di chiamate semisincronose perché le chiamate semisincrone sono più sicure delle chiamate asincrone. Per altre informazioni, vedere Esecuzione di una chiamata [semisincrona con C++](making-a-semisynchronous-call-with-c--.md) e [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md)

La procedura seguente descrive come effettuare una chiamata asincrona usando il sink nel processo.

**Per effettuare una chiamata asincrona usando C++**

1.  Implementare [**l'interfaccia IWbemObjectSink.**](iwbemobjectsink.md)

    Tutte le applicazioni che effettuano chiamate asincrone devono implementare [**IWbemObjectSink**](iwbemobjectsink.md). I consumer di eventi temporanei implementano **anche IWbemObjectSink** per ricevere la notifica degli eventi.

2.  Accedere allo spazio dei nomi WMI di destinazione.

    Le applicazioni devono sempre chiamare la funzione COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) durante la fase di inizializzazione. Se non lo fanno prima di effettuare una chiamata asincrona, WMI rilascia il sink dell'applicazione senza completare la chiamata asincrona. Per altre informazioni, vedere [Inizializzazione di COM per un'applicazione WMI.](initializing-com-for-a-wmi-application.md)

3.  Impostare la sicurezza per il sink.

    Le chiamate asincrone creano un'ampia gamma di problemi di sicurezza che potrebbe essere necessario gestire, ad esempio consentire l'accesso WMI all'applicazione. Per altre informazioni, vedere [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md)

4.  Effettuare la chiamata asincrona.

    Il metodo restituisce immediatamente con il **codice di esito positivo WBEM S NO \_ \_ \_ ERROR.** L'applicazione può procedere con altre attività durante l'attesa del completamento dell'operazione. WMI restituisce all'applicazione chiamando i metodi [**nell'implementazione IWbemObjectSink**](iwbemobjectsink.md) dell'applicazione.

5.  Se necessario, controllare periodicamente l'implementazione per gli aggiornamenti.

    Le applicazioni possono ricevere una notifica dello stato intermedio impostando il *parametro lFlags* nella chiamata asincrona a **WBEM \_ FLAG SEND \_ \_ STATUS**. WMI segnala lo stato della chiamata impostando il *parametro lFlags* di [**IWbemObjectSink**](iwbemobjectsink.md) su **WBEM \_ STATUS \_ PROGRESS**.

6.  Se necessario, è possibile annullare la chiamata prima del completamento dell'elaborazione di WMI chiamando il metodo [**IWbemServices::CancelCallAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)

    Il [**metodo CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) annulla l'elaborazione asincrona rilasciando immediatamente il puntatore all'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) e garantisce che il puntatore venga rilasciato prima del ritorno **di CancelAsyncCall.**

    Se si usa un oggetto wrapper che implementa **l'interfaccia IUnsecured** per ospitare [**IWbemObjectSink,**](iwbemobjectsink.md)potrebbero verificarsi altre complicazioni. Poiché l'applicazione deve passare lo stesso puntatore a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) passato nella chiamata asincrona originale, l'applicazione deve mantenere l'oggetto wrapper fino a quando non diventa chiaro che l'annullamento non è necessario. Per altre informazioni, vedere [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md)

7.  Al termine, pulire i puntatori e arrestare l'applicazione.

    WMI fornisce la chiamata di stato finale tramite il [**metodo SetStatus.**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)

    > [!Note]  
    > Dopo aver inviato l'aggiornamento dello stato finale, WMI rilascia il sink di oggetto chiamando il **metodo Release** per la classe che implementa l'interfaccia [**IWbemObjectSink.**](iwbemobjectsink.md) Nell'esempio precedente si tratta del **metodo QuerySink::Release.** Se si vuole avere il controllo sulla durata dell'oggetto sink, è possibile implementare il sink con un conteggio dei riferimenti iniziale di uno (1).

     

    Se un'applicazione client passa la stessa interfaccia sink in due diverse chiamate asincrone sovrapposte, WMI non garantisce l'ordine del callback. Un'applicazione client che effettua chiamate asincrone sovrapposte deve passare oggetti sink diversi o serializzare le chiamate.

L'esempio seguente richiede le istruzioni reference e \# include seguenti.


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



L'esempio seguente descrive come eseguire una query asincrona usando il metodo [**ExecQueryAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) ma non crea impostazioni di sicurezza né rilascia [**l'oggetto IWbemObjectSink.**](iwbemobjectsink.md) Per altre informazioni, vedere [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md)


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
> Il codice precedente non viene compilato senza errori perché la **classe QuerySink** non è stata definita. Per altre informazioni su **QuerySink,** vedere [**IWbemObjectSink**](iwbemobjectsink.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata di un metodo](calling-a-method.md)
</dt> </dl>

 

 
