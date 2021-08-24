---
description: Negli script di monitoraggio è possibile evitare chiamate successive a GetObject usando un oggetto SWbemRefresher. L'oggetto SWbemRefresher è un contenitore che può contenere diversi oggetti WMI i cui dati possono essere aggiornati in un'unica chiamata.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Aggiornamento dei dati WMI negli script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 969a97c6300ac256e08c79e4f4aaeaa8d05bda072a2c310812ce3b2061c791fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050449"
---
# <a name="refreshing-wmi-data-in-scripts"></a>Aggiornamento dei dati WMI negli script

Negli script di monitoraggio è possibile evitare chiamate successive a **GetObject** usando un [**oggetto SWbemRefresher.**](swbemrefresher.md) **L'oggetto SWbemRefresher** è un contenitore che può contenere diversi oggetti WMI i cui dati possono essere aggiornati in un'unica chiamata.

L'uso di un oggetto [**SWbemRefresher**](swbemrefresher.md) è necessario per ottenere dati accurati dalle classi di prestazioni WMI, ad esempio [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) o altre classi preinstallate derivate da [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf).

La procedura seguente descrive come aggiornare i dati negli script.

**Per aggiornare i dati negli script**

1.  Chiamare **CreateObject** per creare un [**oggetto di aggiornamento SWbemRefresher.**](swbemrefresher.md)

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  Connessione allo spazio dei nomi WMI. Per usare classi di prestazioni [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf) preinstallate, connettersi alla **radice \\ cimv2**.

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  Aggiungere un singolo oggetto (chiamare [**SWbemRefresher.Add)**](swbemrefresher-add.md)o una raccolta (chiamare [**SWbemRefresher.AddEnum)**](swbemrefresher-addenum.md)all'aggiornamento.

    Usare le classi di dati precalcolate derivate da [**Win32 \_ PerfFormattedData,**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)ad esempio [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) anziché [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk.**](./retrieving-raw-and-formatted-performance-data.md) In caso contrario, è necessario calcolare i valori per tutte le proprietà diverse da contatori semplici.

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  Aggiornare i dati una volta per ottenere i dati sulle prestazioni iniziali.

    Chiamare il [**metodo SWbemRefresher.Refresh**](swbemrefresher-refresh.md) o il metodo [**SWbemObjectEx.Refresh \_**](swbemobjectex-refresh-.md) generico.

    ```VB
    objRefresher.Refresh
    ```

    

5.  Se si monitora le prestazioni e si dispone di una raccolta nell'oggetto di aggiornamento, scorrere gli oggetti raccolta.

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  Cancellare gli elementi dall'aggiornamento chiamando [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) o rimuovendo elementi specifici chiamando [**SwbemRefresher.Remove**](swbemrefresher-remove.md).

Nell'esempio di codice VBScript seguente viene illustrato come aggiornare un singolo oggetto nel computer locale. Lo script crea un contenitore di aggiornamento e aggiunge un'istanza di un enumeratore per le istanze di [**Win32 \_ PerfFormattedData \_ PerfProc \_ Process.**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) La [**chiamata Refresh**](swbemrefresher-refresh.md) viene effettuata tre volte per illustrare le modifiche nella proprietà **PercentProcessorTime** per i processi che usano più dell'1% del tempo del processore.


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



La [**proprietà Index**](swbemrefreshableitem-index.md) dell'oggetto [**SWbemRefreshableItem restituito**](swbemrefreshableitem.md) rappresenta l'indice dell'oggetto nella raccolta dell'aggiornamento. È possibile chiamare la proprietà [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) per determinare se un elemento di un aggiornamento è un singolo elemento o una raccolta. Per accedere a un singolo elemento, usare la [**proprietà SWbemRefreshableItem.Object.**](swbemrefreshableitem-object.md) Se non si effettua la chiamata a **SWbemRefreshableItem.Object**, lo script ha esito negativo quando si tenta di accedere all'oggetto. Per accedere a una raccolta, usare la [**proprietà SWbemRefreshableItem.ObjectSet.**](swbemrefreshableitem-objectset.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi di contatori delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Accesso ai dati sulle prestazioni nello script](accessing-performance-data-in-script.md)
</dt> <dt>

[Attività WMI: Monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
