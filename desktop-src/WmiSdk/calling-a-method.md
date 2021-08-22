---
description: WMI fornisce metodi nell'API COM e nell'API di scripting per ottenere informazioni o modificare oggetti in un sistema aziendale.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Chiamata di un metodo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db6c8a74c8125e0bb1727839b8f59f4b486161d5ae629a0c7351481ade016ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820087"
---
# <a name="calling-a-wmi-method"></a>Chiamata di un metodo WMI

WMI fornisce metodi [nell'API COM e nell'API](com-api-for-wmi.md) [di scripting](scripting-api-for-wmi.md) per ottenere informazioni o modificare oggetti in un sistema aziendale. Ad esempio, il metodo di scripting WMI [**SWbemServices.Exequery cQuery**](swbemservices-execquery.md) per i dati. I provider hanno anche metodi definiti nelle classi che registrano. Ad esempio, [**i metodi \_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) e [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) forniti dal [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider).

In questo argomento vengono illustrate le sezioni seguenti:

-   [Metodi WMI rispetto ai metodi del provider](#wmi-methods-compared-to-provider-methods)
-   [Modalità di chiamata al metodo in WMI](#method-calling-modes-in-wmi)
    -   [Modalità sincrona](#synchronous-mode)
    -   [Modalità asincrona](#asynchronous-mode)
    -   [Modalità semisincronia](#semisynchronous-mode)
-   [Argomenti correlati](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>Metodi WMI rispetto ai metodi del provider

Usando le [*chiamate al metodo WMI*](gloss-w.md) combinate con le chiamate al metodo del [*provider,*](gloss-p.md) è possibile recuperare e modificare le informazioni sull'azienda. Per altre informazioni, vedere [Chiamata di un metodo WMI](calling-a-wmi-method.md) e Chiamata di un metodo [provider](calling-a-provider-method.md).

I metodi dell'oggetto di scripting WMI [**SWbemObject**](swbemobject.md) hanno uno stato speciale perché possono essere applicati a qualsiasi classe di dati WMI. Per altre informazioni, vedere [Scripting with SWbemObject](scripting-with-swbemobject.md).

L'esempio di codice seguente chiama sia i metodi WMI che i metodi del provider.

I metodi WMI e provider seguenti si trovano [nell'API di scripting per WMI:](scripting-api-for-wmi.md)

-   **objWMIService.ExecQuery** chiama il metodo di scripting WMI [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **objService.StopService()** chiama il metodo del provider [ **Win32 \_ Service.StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

È possibile cercare il codice che può essere visualizzato in "Return" nella sezione Codici restituiti per [**il servizio \_ Win32.**](/windows/desktop/CIMWin32Prov/win32-service)


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a>Method-Calling in WMI

La modalità di chiamata semisincrona offre in genere il miglior equilibrio tra sicurezza e prestazioni.

Per altre informazioni su ognuna delle modalità possibili, vedere quanto segue:

-   [Sincrono](#synchronous-mode)
-   [Asincrono](#asynchronous-mode)
-   [Semisincronous](#semisynchronous-mode)

### <a name="synchronous-mode"></a>Modalità sincrona

La modalità sincrona si verifica quando il programma o gli script vengono sospesi finché la chiamata al metodo non restituisce un oggetto raccolta [**SWbemObjectSet.**](swbemobjectset.md) WMI compila questa raccolta in memoria prima di restituire l'oggetto raccolta al programma o allo script chiamante.

La modalità sincrona può influire negativamente sulle prestazioni del programma o dello script nel computer che esegue il programma o lo script. Ad esempio, il recupero sincrono di migliaia di eventi dal log eventi può richiedere molto tempo e usare una grande quantità di memoria perché WMI crea un oggetto da ogni evento e quindi li inserisce in una raccolta prima di passare la raccolta al metodo .

È consigliabile chiamare solo metodi che non restituiscono set di dati di grandi dimensioni in modalità sincrona. I metodi [**SWbemServices**](swbemservices.md) seguenti possono essere chiamati in modo sicuro in modalità sincrona:

-   [**SWbemServices.Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.Get**](swbemservices-get.md)

Qualsiasi metodo [**SWbemServices**](swbemservices.md) senza la parola "Async" nel nome può essere chiamato in modalità sincrona impostando il **valore wbemFlagReturnWhenComplete** nel *parametro iFlags.*

### <a name="asynchronous-mode"></a>Modalità asincrona

La modalità asincrona si verifica quando il programma o lo script continua a essere eseguito dopo la chiamata al metodo . WMI restituisce tutti gli oggetti dal metodo a un [**oggetto SWbemSink**](swbemsink.md) durante la creazione di ogni oggetto. Il programma o lo script chiamante deve avere un **oggetto SWbemSink** e un gestore eventi [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) per elaborare gli oggetti restituiti. Per altre informazioni sulla creazione di un gestore eventi per la modalità asincrona, vedere [Ricezione di un evento WMI](receiving-a-wmi-event.md).

Anche se questa modalità non comporta la penalità delle prestazioni e delle risorse della modalità sincrona, la modalità asincrona può creare gravi rischi per la sicurezza perché i risultati archiviati nell'oggetto [**SWbemSink**](swbemsink.md) potrebbero non derivare dal programma o dallo script chiamante. WMI riduce il livello di autenticazione **nell'oggetto SWbemSink** finché il metodo non riesce. Per altre informazioni su come attenuare questi rischi per la sicurezza, vedere [Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

I metodi aggiunti con la parola Async sono metodi per la modalità asincrona. I metodi seguenti sono chiamate asincrone:

-   [**SWbemServices.AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
-   [**SWbemServices.DeleteAsync**](swbemservices-deleteasync.md)
-   [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
-   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)
-   [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
-   [**SWbemServices.InstancesOfAsync**](swbemservices-instancesofasync.md)
-   [**SWbemServices.ReferencesToAsync**](swbemservices-referencesto.md)
-   [**SWbemServices.SubclassesOfAsync**](swbemservices-subclassesofasync.md)

Per altre informazioni sulla modalità asincrona, vedere:

-   [Esecuzione di una chiamata asincrona con C++](making-an-asynchronous-call-with-c--.md)
-   [Esecuzione di una chiamata asincrona con VBScript](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>Modalità semisincronous

La modalità semisincrona è simile alla modalità asincrona in cui il programma o lo script continua a essere eseguito dopo la chiamata al metodo . In modalità semisincrona, WMI recupera gli oggetti in background mentre lo script o il programma continua a essere eseguito. WMI restituisce ogni oggetto restituito al metodo chiamante subito dopo la creazione dell'oggetto.

Poiché WMI gestisce l'oggetto, la modalità semisincrona è più sicura della modalità asincrona. Tuttavia, se si usa la modalità semisincronous con più di 1.000 istanze, il recupero dell'istanza può monopolizzare le risorse disponibili, con un possibile peggioramento delle prestazioni del programma o dello script e del computer usando il programma o lo script. Ogni oggetto occupa le risorse necessarie fino al rilascio della memoria.

Per risolvere questa condizione, è possibile chiamare il metodo con il parametro *iFlags* impostato con i flag **wbemFlagForwardOnly** e **wbemFlagReturnImmediately** per indicare a WMI di restituire un [**oggetto SWbemObjectSet**](swbemobjectset.md)forward-only. **SWbemObjectSet** forward-only elimina il problema di prestazioni causato da un set di dati di grandi dimensioni rilasciando la memoria dopo l'enumerazione dell'oggetto.

Qualsiasi [**metodo SWbemServices**](swbemservices.md) che non può essere chiamato in modalità sincrona o asincrona viene chiamato in modalità semisincrona.

I metodi seguenti vengono chiamati in modalità semisincronous:

-   [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices.Get**](swbemservices-get.md)
-   [**SWbemServices.InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)
-   [**SWbemServices.Put**](swbemservicesex-put.md)

Per altre informazioni sulla modalità semisincronous, vedere Esecuzione di una chiamata [semisincronosa con C++](making-a-semisynchronous-call-with-c--.md) e Esecuzione di una chiamata [semisincrona con VBScript.](making-a-semisynchronous-call-with-vbscript.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento delle prestazioni di enumerazione](improving-enumeration-performance.md)
</dt> <dt>

[Scripting con SWbemObject](scripting-with-swbemobject.md)
</dt> <dt>

[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
