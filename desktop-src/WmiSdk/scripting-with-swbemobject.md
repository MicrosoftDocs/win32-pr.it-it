---
description: L'oggetto di scripting SWbemObject è l'oggetto WMI generico, che definisce proprietà e metodi che possono essere utilizzati indipendentemente dall'oggetto WMI specifico a cui è associato l'oggetto SWbemObject.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Creazione di script con SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131007"
---
# <a name="scripting-with-swbemobject"></a>Creazione di script con SWbemObject

L'oggetto di scripting [**SWbemObject**](swbemobject.md) è l'oggetto WMI generico, che definisce proprietà e metodi che possono essere utilizzati indipendentemente dall'oggetto WMI specifico a cui è associato l'oggetto **SWbemObject** . Tutti gli oggetti WMI, ad esempio un'istanza [**del \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) o qualsiasi altra classe di dati WMI, sono rappresentati da [**SWbemObject**](swbemobject.md) e possono utilizzare le proprietà e i metodi comuni di **SWbemObject** , oltre alle proprietà e ai metodi specifici.

Usare, ad esempio, lo script seguente per ottenere tutte le istanze di un [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) chiamando il metodo [**SWbemObject. instances \_**](swbemobject-instances-.md) . ClsobjProcess rappresenta sia la definizione della classe di **\_ processo Win32** sia una [**SWbemObject**](swbemobject.md).


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



Nell'esempio seguente viene ottenuta un'istanza specifica [**del \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) che rappresenta il servizio Alerter e la archivia in objAlerter. È quindi possibile chiamare i metodi [**SWbemObject**](swbemobject.md) , ad esempio WScript. Echo ObjAlerter. Path \_ , o i metodi definiti dalla classe di dati, ad esempio WScript. Echo objAlerter. state. objAlerter che rappresenta un'istanza del servizio Win32 \_ e un **SWbemObject**.


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



La chiamata a [**SWbemObject. instances \_**](swbemobject-instances-.md) ottiene un altro oggetto generico di script WMI, [**SWbemObjectSet**](swbemobjectset.md). Come illustrato, l'oggetto **SWbemObjectSet** può essere considerato come una [raccolta](accessing-a-collection.md).


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



È possibile identificare i metodi [**SWbemObject**](swbemobject.md) perché tutti terminano con un carattere di sottolineatura ( \_ ), ad esempio [**SWbemObject \_ . Instances**](swbemobject-instances-.md).

[**SWbemObjectEx**](swbemobjectex.md) estende le proprietà di [**SWbemObject**](swbemobject.md). Ad esempio, è ora possibile aggiornare i dati di qualsiasi oggetto WMI, ad esempio un'istanza del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process), mediante una chiamata a [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md).

Nell'esempio seguente viene illustrato come i dati di errore della pagina processo di sistema possono essere aggiornati ogni cinque secondi.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



Per ulteriori informazioni sull'aggiornamento dei dati tramite un oggetto [**SWbemRefresher**](swbemrefresher.md) , vedere [aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md).

[**SWbemObject. put \_**](swbemobject-put-.md) e [**PutAsync \_**](swbemobject-putasync-.md) consentono di scrivere di nuovo le modifiche in qualsiasi oggetto WMI. Questi metodi consentono di eseguire il commit delle modifiche a un oggetto nello spazio dei nomi in cui è stato creato l'oggetto. È possibile scrivere l'oggetto in uno spazio dei nomi diverso usando [**SWbemServicesEx. Put**](swbemservicesex-put.md) o [**SWbemServicesEx. PutAsync**](swbemservicesex-putasync.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API di scripting per WMI](scripting-api-for-wmi.md)
</dt> <dt>

[Creazione di uno script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Aggiornamento di un'intera istanza](updating-an-entire-instance.md)
</dt> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> </dl>

 

 
