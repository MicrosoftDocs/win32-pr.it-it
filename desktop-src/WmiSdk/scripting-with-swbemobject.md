---
description: L'oggetto di scripting SWbemObject è l'oggetto WMI generico, che definisce proprietà e metodi che possono essere usati indipendentemente dall'oggetto WMI specifico a cui è associato l'oggetto SWbemObject.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Esecuzione di script con SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d6ba0cccca8fcd62af490aa91ab1cc965fdad4d3682d99a8fda52151135500ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739697"
---
# <a name="scripting-with-swbemobject"></a>Esecuzione di script con SWbemObject

L'oggetto di scripting [**SWbemObject**](swbemobject.md) è l'oggetto WMI generico, che definisce proprietà e metodi che possono essere usati indipendentemente dall'oggetto WMI specifico a cui è associato **l'oggetto SWbemObject.** Tutti gli oggetti WMI, ad esempio un'istanza del processo [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) o qualsiasi altra classe di dati WMI, sono rappresentati da [**SWbemObject**](swbemobject.md) e possono usare le proprietà e i metodi comuni **di SWbemObject** oltre alle proprietà e ai metodi specifici.

Ad esempio, usare lo script seguente per ottenere tutte le istanze di un processo [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) chiamando il [**metodo SWbemObject.Instances. \_**](swbemobject-instances-.md) ClsobjProcess rappresenta sia la definizione della **classe \_ Processo Win32** che [**un oggetto SWbemObject.**](swbemobject.md)


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



L'esempio seguente ottiene un'istanza specifica del servizio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) che rappresenta il servizio Alerter e la archivia in objAlerter. È quindi possibile chiamare i metodi [**SWbemObject,**](swbemobject.md) ad esempio WScript.Echo objAlerter.Path, o i metodi definiti dalla classe di dati, ad esempio \_ WScript.Echo objAlerter.State. objAlerter che rappresenta sia un'istanza del servizio Win32 che \_ **un oggetto SWbemObject.**


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



La chiamata a [**SWbemObject.Instances \_**](swbemobject-instances-.md) ottiene un altro oggetto di scripting WMI generico, [**SWbemObjectSet.**](swbemobjectset.md) Come illustrato, **l'oggetto SWbemObjectSet** può essere considerato come una [raccolta](accessing-a-collection.md).


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



È possibile identificare i [**metodi SWbemObject**](swbemobject.md) perché terminano tutti con un carattere di sottolineatura ( ), ad \_ [**esempio, SWbemObject.Instances \_**](swbemobject-instances-.md).

[**SWbemObjectEx**](swbemobjectex.md) estende le proprietà di [**SWbemObject**](swbemobject.md). Ad esempio, è ora possibile aggiornare i dati di qualsiasi oggetto WMI, ad esempio un'istanza del processo [**Win32, \_**](/windows/desktop/CIMWin32Prov/win32-process)tramite una chiamata a [**\_ SWbemObjectEx.Refresh**](swbemobjectex-refresh-.md).

Nell'esempio seguente viene illustrato come i dati di errore di pagina del processo di sistema possono essere aggiornati ogni cinque secondi.


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



Per altre informazioni sull'aggiornamento dei dati tramite [**un oggetto SWbemRefresher,**](swbemrefresher.md) vedere Aggiornamento dei dati [WMI negli script.](refreshing-wmi-data-in-scripts.md)

[**\_ SWbemObject.Put**](swbemobject-put-.md) e [**PutAsync \_**](swbemobject-putasync-.md) consentono di scrivere di nuovo le modifiche in qualsiasi oggetto WMI. Questi metodi emettono solo il commit delle modifiche apportate a un oggetto nello spazio dei nomi in cui è stato creato l'oggetto. È possibile scrivere l'oggetto in uno spazio dei nomi diverso [**usando SWbemServicesEx.Put**](swbemservicesex-put.md) o [**SWbemServicesEx.PutAsync.**](swbemservicesex-putasync.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API di scripting per WMI](scripting-api-for-wmi.md)
</dt> <dt>

[Creazione di uno script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Aggiornamento di un'intera istanza](updating-an-entire-instance.md)
</dt> <dt>

[Chiamata di un metodo](calling-a-method.md)
</dt> </dl>

 

 
