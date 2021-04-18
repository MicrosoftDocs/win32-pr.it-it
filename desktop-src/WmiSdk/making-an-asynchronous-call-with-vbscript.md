---
description: Effettuando una chiamata asincrona a un metodo WMI o a un metodo del provider è possibile continuare l'esecuzione di uno script mentre gli oggetti restituiscono un oggetto SWbemSink e vengono gestiti da metodi come SWbemSink. OnObjectReady.
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
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312695"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a>Esecuzione di una chiamata asincrona con VBScript

Effettuando una chiamata asincrona a un [*metodo WMI*](gloss-w.md) o a un [*metodo del provider*](gloss-p.md) è possibile continuare l'esecuzione di uno script mentre gli oggetti restituiscono un oggetto [**SWbemSink**](swbemsink.md) e vengono gestiti da metodi come [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md). Tuttavia, le chiamate asincrone non sono consigliate perché è possibile che i dati non vengano restituiti allo stesso livello di sicurezza della chiamata.

Quando si usano chiamate di sink asincrone come [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) per ottenere i dati restituiti, è possibile impostare il valore del registro di sistema seguente.

**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**

L'impostazione di questo valore del registro di sistema assicura l'autenticazione degli oggetti dati restituiti al sink. Se **UnsecAppAccessControlDefault** è impostato su uno (1), WMI esegue il controllo dell'accesso dei dati restituiti. I controlli di accesso verificano che i dati provengano dall'origine corretta. Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

I metodi asincroni con nomi che terminano con "Async \_ " restituiscono sempre immediatamente dopo essere stati chiamati, in modo che un programma possa continuare l'esecuzione. Ad esempio, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) è sincrono e blocca l'esecuzione fino a quando non vengono restituiti tutti gli oggetti. Il [**SWbemServices.Exemetodo cQueryAsync**](swbemservices-execqueryasync.md) è la versione asincrona di non blocco. Un modo più sicuro per effettuare la chiamata a **SWbemServices.Exe** il non blocco cQuery consiste nell'eseguire la chiamata [*semisincrona*](gloss-s.md). Per altre informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md) ed [esecuzione di una chiamata semisincrono con VBScript](making-a-semisynchronous-call-with-vbscript.md).

Il parametro *iFlags* per le chiamate asincrone viene sempre impostato su zero (0). I metodi asincroni non forniscono una raccolta [**SWbemObjectSet**](swbemobjectset.md) alla subroutine del sink. Al contrario, la subroutine dell'evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) nello script o nell'applicazione riceve ogni oggetto così come viene fornito.

Al termine della chiamata asincrona originale, viene chiamato l'evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) del sink di oggetto e viene eseguito il codice inserito per elaborare il risultato della chiamata.

> [!Note]  
> Una pagina di Active Server (ASP) come host di script non supporta una chiamata asincrona.

 

Nella procedura riportata di seguito viene descritto come eseguire una chiamata asincrona tramite VBScript.

**Per eseguire una chiamata asincrona tramite VBScript**

1.  Connettersi a WMI e ottenere un oggetto [**SWbemServices**](swbemservices.md) .

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  Creare il sink di oggetto usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) o (solo per Windows Script Host 2,0) il tag Object con un attributo Events impostato su **true**.

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    -oppure-

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  Crea una subroutine per ogni evento che può essere attivato da un evento asincrono. Questi eventi sono definiti come metodi in [**SWbemObject**](swbemobject.md). WMI, ad esempio, effettua un callback a [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) quando ogni istanza restituisce.

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

    

    Esaminare il parametro *iHresult* restituito dall'evento [**OnCompleted**](swbemsink-oncompleted.md) per determinare se la chiamata asincrona ha avuto esito positivo o se si è verificato un errore. In caso di esito positivo, il valore passato nel parametro *iHresult* è uguale a zero (0). Qualsiasi altro valore potrebbe indicare un errore ed è necessario controllare i valori nell'oggetto Error restituito nel parametro *objErrorObject* .

4.  Eseguire una chiamata asincrona e passare il nome del sink nel parametro *objWbemSink* .

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  Eseguire una chiamata che impedisce che lo script venga terminato prima della ricezione di tutti gli eventi. Se lo script può essere eseguito con un'interfaccia schermo, un modo semplice per eseguire questa operazione consiste nell'usare un comando Windows script host (WSH) `Echo` , illustrato nell'esempio seguente.

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    Quando si esegue questo script, è possibile che la prima istanza venga restituita prima del messaggio **in attesa di istanze** o che venga visualizzata dopo. Si tratta della natura dell'elaborazione asincrona. Se si chiude troppo presto la finestra di messaggio **in attesa di istanze** , è possibile che non vengano visualizzate tutte le istanze.

6.  Se si hanno risultati di diverse chiamate asincrone che restituiscono lo stesso sink, archiviare i dati di distinzione necessari nel parametro di contesto *objWbemAsyncContext* .

7.  Al termine del sink, annullare la chiamata asincrona con il metodo [**Cancel**](swbemsink-cancel.md) .

    ```VB
    objwbemsink.Cancel()
    ```

    

    Il metodo [**Cancel**](swbemsink-cancel.md) indica a WSH di annullare tutte le chiamate asincrone associate a un oggetto sink specificato. Pertanto, è consigliabile utilizzare sink distinti per le operazioni asincrone che devono essere indipendenti.

8.  Rilasciare l'oggetto sink assegnando l'oggetto sink a `Nothing` .

    ```VB
    set objwbemsink= Nothing
    ```

    

Nell'esempio di codice seguente viene illustrata una query asincrona per tutte le istanze del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) nel computer locale. Per una versione semisincrono dello stesso metodo, vedere [chiamata a un metodo](calling-a-method.md).


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

[Chiamata a un metodo](calling-a-method.md)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
