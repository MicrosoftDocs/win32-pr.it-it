---
description: Gli script WMI possono accedere alle classi del contatore delle prestazioni WMI preinstallate, sia nel computer locale che in remoto.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Accesso ai dati sulle prestazioni nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e203acfc7fc23fe0dab466eee383223aad0bf889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319311"
---
# <a name="accessing-performance-data-in-script"></a>Accesso ai dati sulle prestazioni nello script

Gli script WMI possono accedere alle [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI preinstallate, sia nel computer locale che in remoto. Sebbene gli script possano ottenere dati da classi non calcolate, ad esempio la [**\_ \_ \_ memoria PerfRawData di prestazioni Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)o le classi formattate, [**Win32 \_ PerfFormattedData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), le classi di dati formattate possono essere più facili da usare.

Il monitoraggio dei dati sulle prestazioni con le classi del contatore delle prestazioni richiede l'utilizzo di un [*aggiornamento*](gloss-r.md). Utilizzare l'oggetto [**SWbemRefresher**](swbemrefresher.md) per archiviare uno o più oggetti prestazioni per l'aggiornamento o l'aggiornamento di un singolo oggetto da parte della chiamata [**SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) . Per ulteriori informazioni, vedere [aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md).

Impostando la proprietà [**SWbemRefresher. AutoReconnect**](swbemrefresher-autoreconnect.md) su **true**, WMI si riconnette automaticamente a un provider remoto se la connessione è interruppe, in modo da non dover controllare lo stato della connessione.

Come illustrato nello script di esempio di codice di script seguente, è necessario effettuare una chiamata di aggiornamento iniziale per ottenere un valore iniziale per l'oggetto che si sta aggiornando. Le chiamate di aggiornamento successive contengono quindi i dati.

> [!Note]  
> Quando uno script accede ai dati dei contatori delle prestazioni WMI da un computer remoto, lo script può essere eseguito solo con l'account utente connesso corrente. WMI non supporta una chiamata [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) che passa le credenziali utente diverse. Pertanto, l'account che chiama il computer remoto deve disporre già dei privilegi appropriati per tale computer.

 

Nell'esempio di codice di script seguente viene illustrato come utilizzare un oggetto [**SWbemRefresher**](swbemrefresher.md) per aggiornare i dati negli oggetti contatore delle prestazioni. Per ulteriori informazioni sull'utilizzo dei contatori delle prestazioni in WMI, vedere [accesso alle classi di prestazioni preinstallate di WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:Win32_PerfRawdata_Perfproc_process.name='wscript'")
set CookedProc = GetObject("winmgmts:Win32_Perfformatteddata_Perfproc_process.name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="example"></a>Esempio

Nell'esempio di codice di script seguente viene illustrato che è necessario effettuare una chiamata di aggiornamento iniziale per ottenere un valore iniziale per l'oggetto aggiornato. Le chiamate di aggiornamento successive contengono quindi i dati.

Nell'esempio di codice di script seguente viene illustrato come utilizzare un oggetto [**SWbemRefresher**](swbemrefresher.md) per aggiornare i dati negli oggetti contatore delle prestazioni. Per ulteriori informazioni sull'utilizzo dei contatori delle prestazioni in WMI, vedere [accesso alle classi di prestazioni preinstallate di WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:" _
                        & "Win32_PerfRawdata_Perfproc_process." _
                        & "name='wscript'")
set CookedProc = GetObject("winmgmts:" _ 
                & "Win32_Perfformatteddata_Perfproc_process." _
                & "name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = " _
                 & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " _
                 & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Attività WMI: monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
