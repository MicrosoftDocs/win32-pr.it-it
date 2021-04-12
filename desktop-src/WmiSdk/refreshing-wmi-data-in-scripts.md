---
description: Negli script di monitoraggio è possibile evitare chiamate successive a GetObject usando un oggetto SWbemRefresher. L'oggetto SWbemRefresher è un contenitore che può contenere diversi oggetti WMI i cui dati possono essere aggiornati in una sola chiamata.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Aggiornamento dei dati WMI negli script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232398"
---
# <a name="refreshing-wmi-data-in-scripts"></a>Aggiornamento dei dati WMI negli script

Negli script di monitoraggio è possibile evitare chiamate successive a **GetObject** usando un oggetto [**SWbemRefresher**](swbemrefresher.md) . L'oggetto **SWbemRefresher** è un contenitore che può contenere diversi oggetti WMI i cui dati possono essere aggiornati in una sola chiamata.

L'utilizzo di un oggetto [**SWbemRefresher**](swbemrefresher.md) è necessario per ottenere dati accurati dalle classi delle prestazioni WMI, ad esempio [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) o altre classi preinstallate derivate da [**\_ Perf Win32**](/windows/desktop/CIMWin32Prov/win32-perf).

Nella procedura riportata di seguito viene descritto come aggiornare i dati negli script.

**Per aggiornare i dati negli script**

1.  Chiamare **CreateObject** per creare un oggetto di aggiornamento [**SWbemRefresher**](swbemrefresher.md) .

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  Connettersi allo spazio dei nomi WMI. Per usare le classi performance [**performance \_ Win32**](/windows/desktop/CIMWin32Prov/win32-perf) preinstallate, connettersi alla **radice \\ CIMV2**.

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  Aggiungere un singolo oggetto (Call [**SWbemRefresher. Add**](swbemrefresher-add.md)) o una raccolta (Call [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) all'aggiornamento.

    Usare le classi di dati precalcolate derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), ad esempio [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) anziché [**Win32 \_ PerfRawData \_ \_**](./retrieving-raw-and-formatted-performance-data.md)perfdisk disco logico. In caso contrario, è necessario calcolare i valori per tutte le proprietà diverse da semplici contatori.

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  Aggiornare i dati una volta per ottenere i dati sulle prestazioni iniziali.

    Chiamare il metodo [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) o il metodo generico [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) .

    ```VB
    objRefresher.Refresh
    ```

    

5.  Se si esegue il monitoraggio delle prestazioni e si dispone di una raccolta nell'oggetto di aggiornamento, eseguire il ciclo degli oggetti della raccolta.

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  Cancellare gli elementi dall'aggiornamento chiamando [**SWbemRefresher. DeleteAll**](swbemrefresher-deleteall.md) o rimuovere elementi specifici chiamando [**SWbemRefresher. Remove**](swbemrefresher-remove.md).

Nell'esempio di codice VBScript riportato di seguito viene illustrato come aggiornare un singolo oggetto nel computer locale. Lo script crea un contenitore di aggiornamento e aggiunge un'istanza di un enumeratore per le istanze di [**\_ \_ \_ processo PerfProc Win32 PerfFormattedData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) . La chiamata di [**aggiornamento**](swbemrefresher-refresh.md) viene effettuata tre volte per illustrare le modifiche apportate alla proprietà **PercentProcessorTime** per i processi che utilizzano più di una percentuale del tempo del processore.


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



La proprietà [**index**](swbemrefreshableitem-index.md) dell'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) restituito rappresenta l'indice dell'oggetto nella raccolta di aggiornamenti. È possibile chiamare la proprietà [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) per determinare se un elemento in un aggiornamento è un singolo elemento o una raccolta. Per accedere a un singolo elemento, utilizzare la proprietà [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) . Se non si effettua la chiamata a **SWbemRefreshableItem. Object**, lo script avrà esito negativo quando si tenta di accedere all'oggetto. Per accedere a una raccolta, usare la proprietà [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Accesso ai dati sulle prestazioni nello script](accessing-performance-data-in-script.md)
</dt> <dt>

[Attività WMI: monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
