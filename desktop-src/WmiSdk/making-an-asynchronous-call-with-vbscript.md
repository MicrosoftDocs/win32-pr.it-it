---
description: L'esecuzione di una chiamata asincrona a un metodo WMI o a un metodo provider consente a uno script di continuare l'esecuzione mentre gli oggetti restituiscono un oggetto SWbemSink e vengono gestiti da metodi come SWbemSink.OnObjectReady.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Esecuzione di una chiamata asincrona con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee8c4737ff7513441532275e24f2cfe20f8e30fa2932e854cc566eb032c49d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555143"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a>Esecuzione di una chiamata asincrona con VBScript

L'esecuzione di una chiamata asincrona a un metodo [*WMI*](gloss-w.md) o a un metodo [*provider*](gloss-p.md) consente a uno script di continuare l'esecuzione mentre gli oggetti restituiscono un [**oggetto SWbemSink**](swbemsink.md) e vengono gestiti da metodi come [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md). Tuttavia, le chiamate asincrone non sono consigliate perché i dati potrebbero non essere restituiti allo stesso livello di sicurezza della chiamata.

Quando si usano chiamate sink asincrone [**come SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) per ottenere i dati restituiti, è possibile impostare il valore del Registro di sistema seguente.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**

L'impostazione di questo valore del Registro di sistema garantisce l'autenticazione degli oggetti dati restituiti al sink. Se **UnsecAppAccessControlDefault è** impostato su uno (1), WMI esegue il controllo di accesso dei dati restituiti. I controlli di accesso verificano che i dati provengono dall'origine corretta. Per altre informazioni, vedere [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md)

I metodi asincroni con nomi che terminano con "Async" restituiscono sempre immediatamente dopo la chiamata in modo che un \_ programma possa continuare l'esecuzione. Ad esempio, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) è sincrona e blocca l'esecuzione fino a quando non vengono restituiti tutti gli oggetti. Il [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) è la versione asincrona non bloccante. Un modo più sicuro per effettuare la chiamata **SWbemServices.ExecQuery** nonblocking è effettuare la chiamata in modo [*semisincronousamente*](gloss-s.md). Per altre informazioni, vedere [Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md) e Esecuzione di una chiamata [semisincrona con VBScript.](making-a-semisynchronous-call-with-vbscript.md)

Il *parametro iFlags* per le chiamate asincrone ha sempre il valore predefinito zero (0). I metodi asincroni non forniscono una [**raccolta SWbemObjectSet**](swbemobjectset.md) alla subroutine sink. Al contrario, la subroutine dell'evento [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) nello script o nell'applicazione riceve ogni oggetto così come viene fornito.

Al termine della chiamata asincrona originale, chiama l'evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) dell'oggetto sink ed esegue il codice che si trova in questa posizione per elaborare il risultato della chiamata.

> [!Note]  
> Una Active Server pagina (ASP) come host script non supporta una chiamata asincrona.

 

La procedura seguente descrive come effettuare una chiamata asincrona usando VBScript.

**Per effettuare una chiamata asincrona usando VBScript**

1.  Connessione a WMI e ottenere un [**oggetto SWbemServices.**](swbemservices.md)

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  Creare il sink di oggetto usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) o (solo per Windows Script Host 2.0) il tag OBJECT con un attributo events impostato su **TRUE.**

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    -oppure-

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  Creare una subroutine per ogni evento che può essere attivato da un evento asincrono. Questi eventi sono definiti come metodi in [**SWbemObject**](swbemobject.md). Ad esempio, WMI esegue un callback a [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) quando viene restituita ogni istanza.

    Quando si crea la subroutine, inserire il codice nella subroutine per gestire ogni evento quando viene ricevuto.

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    Esaminare il *parametro iHresult* restituito dall'evento [**OnCompleted**](swbemsink-oncompleted.md) per determinare se la chiamata asincrona ha esito positivo o meno o se si è verificato un errore. In caso di esito positivo, il valore passato nel *parametro iHresult* è uguale a zero (0). Qualsiasi altro valore può indicare un errore ed è necessario controllare i valori nell'oggetto errore restituito nel *parametro objErrorObject.*

4.  Eseguire una chiamata asincrona e passare il nome del sink nel *parametro objWbemSink.*

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  Effettuare una chiamata che impedisca la fine dello script prima della ricezione di tutti gli eventi. Se lo script può essere eseguito con un'interfaccia dello schermo, un modo semplice per eseguire questa operazione è usare un comando WSH (Windows Script Host), come illustrato `Echo` nell'esempio seguente.

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    Quando si esegue questo script, è possibile che la prima istanza venga restituita prima del **messaggio Waiting for instances** (Attesa di istanze) oppure che venga visualizzato dopo. Questa è la natura dell'elaborazione asincrona. Se si chiude la **finestra di messaggio In** attesa di istanze troppo presto, è possibile che non venga visualizzata tutte le istanze.

6.  Se si hanno risultati da diverse chiamate asincrone che tornano allo stesso sink, archiviare tutti i dati di distinzione necessari nel parametro di contesto *objWbemAsyncContext.*

7.  Al termine del sink, annullare la chiamata asincrona con il [**metodo Cancel.**](swbemsink-cancel.md)

    ```VB
    objwbemsink.Cancel()
    ```

    

    Il [**metodo Cancel**](swbemsink-cancel.md) indica a WSH di annullare tutte le chiamate asincrone associate a un oggetto sink specificato. È quindi possibile usare sink separati per le operazioni asincrone che devono essere indipendenti.

8.  Rilasciare l'oggetto sink assegnando l'oggetto sink a `Nothing` .

    ```VB
    set objwbemsink= Nothing
    ```

    

Nell'esempio di codice seguente viene illustrata una query asincrona per tutte le istanze del [**processo Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) nel computer locale. Per una versione semisincronosa dello stesso metodo, vedere [Chiamata di un metodo](calling-a-method.md).


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata di un metodo](calling-a-method.md)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
