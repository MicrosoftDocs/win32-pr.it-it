---
description: WMI fornisce i metodi nell'API COM e nell'API di scripting per ottenere informazioni o modificare gli oggetti in un sistema aziendale.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Chiamata a un metodo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319308"
---
# <a name="calling-a-wmi-method"></a>Chiamata a un metodo WMI

WMI fornisce i metodi nell' [API com](com-api-for-wmi.md) e nell' [API di scripting](scripting-api-for-wmi.md) per ottenere informazioni o modificare gli oggetti in un sistema aziendale. Ad esempio, il metodo di scripting WMI [**SWbemServices.ExecQuery**](swbemservices-execquery.md) query per i dati. I provider dispongono anche di metodi definiti nelle classi da essi registrate. Gli esempi sono i metodi [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) e [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) forniti dal [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider).

Le sezioni seguenti sono illustrate in questo argomento:

-   [Metodi WMI rispetto ai metodi del provider](#wmi-methods-compared-to-provider-methods)
-   [Modalità di chiamata di metodo in WMI](#method-calling-modes-in-wmi)
    -   [Modalità sincrona](#synchronous-mode)
    -   [Modalità asincrona](#asynchronous-mode)
    -   [Modalità semisincrono](#semisynchronous-mode)
-   [Argomenti correlati](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>Metodi WMI rispetto ai metodi del provider

Utilizzando le chiamate al [*metodo WMI*](gloss-w.md) combinate con le chiamate al [*metodo del provider*](gloss-p.md) , è possibile recuperare e modificare le informazioni sull'azienda. Per ulteriori informazioni, vedere [chiamata a un metodo WMI](calling-a-wmi-method.md) e [chiamata a un metodo del provider](calling-a-provider-method.md).

I metodi dell'oggetto [**SWbemObject**](swbemobject.md) di scripting WMI hanno uno stato speciale perché possono essere applicati a qualsiasi classe di dati WMI. Per ulteriori informazioni, vedere Creazione di [script con SWbemObject](scripting-with-swbemobject.md).

Nell'esempio di codice seguente vengono chiamati i metodi WMI e provider.

I seguenti metodi WMI e provider si trovano nell' [API di scripting per WMI](scripting-api-for-wmi.md):

-   **objWMIService.ExecQuery** chiama il metodo di scripting WMI [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **objService. StopService ()** chiama il metodo del provider [ **Win32 \_ Service. StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

È possibile cercare il codice che può essere visualizzato in "Return" nella sezione codici restituiti per il [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).


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





## <a name="method-calling-modes-in-wmi"></a>Modalità Method-Calling in WMI

La modalità di chiamata semisincrono in genere fornisce il migliore equilibrio tra sicurezza e prestazioni.

Per ulteriori informazioni su ognuna delle modalità possibili, vedere gli argomenti seguenti:

-   [Sincrono](#synchronous-mode)
-   [Asincrono](#asynchronous-mode)
-   [Semisincrono](#semisynchronous-mode)

### <a name="synchronous-mode"></a>Modalità sincrona

La modalità sincrona si verifica quando il programma o gli script vengono sospesi fino a quando la chiamata al metodo non restituisce un oggetto raccolta [**SWbemObjectSet**](swbemobjectset.md) . WMI compila questa raccolta in memoria prima di restituire l'oggetto raccolta al programma o allo script chiamante.

La modalità sincrona può avere un effetto negativo sulle prestazioni di programmi o script nel computer in cui è in esecuzione il programma o lo script. Ad esempio, il recupero sincrono di migliaia di eventi dal registro eventi può richiedere molto tempo e usare una grande quantità di memoria perché WMI crea un oggetto da ogni evento e quindi inserisce tali oggetti in una raccolta prima di passare la raccolta al metodo.

È consigliabile chiamare solo i metodi che non restituiscono set di dati di grandi dimensioni in modalità sincrona. I metodi [**SWbemServices**](swbemservices.md) seguenti possono essere chiamati in modo sicuro in modalità sincrona:

-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices. Get**](swbemservices-get.md)

Tutti i metodi [**SWbemServices**](swbemservices.md) senza la parola "Async" nel nome possono essere chiamati in modalità sincrona impostando il valore **WbemFlagReturnWhenComplete** nel parametro *iFlags* .

### <a name="asynchronous-mode"></a>Modalità asincrona

La modalità asincrona si verifica quando il programma o lo script continua l'esecuzione dopo la chiamata al metodo. WMI restituisce tutti gli oggetti dal metodo a un oggetto [**SWbemSink**](swbemsink.md) quando viene creato un oggetto. Per elaborare gli oggetti restituiti, il programma o lo script chiamante deve avere un oggetto **SWbemSink** e un gestore dell'evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) . Per ulteriori informazioni sulla creazione di un gestore eventi per la modalità asincrona, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).

Sebbene questa modalità non abbia le prestazioni e la penalizzazione delle risorse della modalità sincrona, la modalità asincrona può creare gravi rischi per la sicurezza perché i risultati archiviati nell'oggetto [**SWbemSink**](swbemsink.md) potrebbero non provenire dal programma chiamante o dallo script. WMI abbassa il livello di autenticazione per l'oggetto **SWbemSink** fino a quando il metodo non riesce. Per ulteriori informazioni su come attenuare questi rischi per la sicurezza, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

I metodi aggiunti con la parola Async sono metodi per la modalità asincrona. I metodi seguenti sono chiamate asincrone:

-   [**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
-   [**SWbemServices. DeleteAsync**](swbemservices-deleteasync.md)
-   [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
-   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)
-   [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
-   [**SWbemServices. InstancesOfAsync**](swbemservices-instancesofasync.md)
-   [**SWbemServices. ReferencesToAsync**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOfAsync**](swbemservices-subclassesofasync.md)

Per ulteriori informazioni sulla modalità asincrona, vedere:

-   [Esecuzione di una chiamata asincrona con C++](making-an-asynchronous-call-with-c--.md)
-   [Esecuzione di una chiamata asincrona con VBScript](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>Modalità semisincrono

La modalità semisincrono è simile alla modalità asincrona in quanto il programma o lo script continua l'esecuzione dopo la chiamata al metodo. In modalità semisincrono, WMI recupera gli oggetti in background quando lo script o il programma continua a essere eseguito. WMI restituisce ogni oggetto restituito al metodo chiamante subito dopo la creazione dell'oggetto.

Poiché WMI gestisce l'oggetto, la modalità semisincrono è più sicura della modalità asincrona. Tuttavia, se si usa la modalità semisincrono con più di 1.000 istanze, il recupero delle istanze può monopolizzare le risorse disponibili, che possono influire negativamente sulle prestazioni del programma o dello script e del computer con il programma o lo script. Ogni oggetto prende le risorse necessarie fino a quando non viene rilasciata la memoria.

Per ovviare a questa condizione, è possibile chiamare il metodo con il set di parametri *iFlags* con i flag **wbemFlagForwardOnly** e **wbemFlagReturnImmediately** per indicare a WMI di restituire un [**SWbemObjectSet**](swbemobjectset.md)di sola trasmissione. Un **SWbemObjectSet** di sola trasmissione elimina il problema di prestazioni causato da un set di dati di grandi dimensioni rilasciando la memoria dopo l'enumerazione dell'oggetto.

Qualsiasi metodo [**SWbemServices**](swbemservices.md) che non può essere chiamato in modalità sincrona o asincrona viene chiamato in modalità semisincrono.

I metodi seguenti vengono chiamati in modalità semisincrono:

-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices. Get**](swbemservices-get.md)
-   [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)
-   [**SWbemServices. Put**](swbemservicesex-put.md)

Per ulteriori informazioni sulla modalità semisincrono, vedere [creazione di una chiamata semisincrono con C++](making-a-semisynchronous-call-with-c--.md) ed [esecuzione di una chiamata semisincrono con VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento delle prestazioni di enumerazione](improving-enumeration-performance.md)
</dt> <dt>

[Creazione di script con SWbemObject](scripting-with-swbemobject.md)
</dt> <dt>

[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
