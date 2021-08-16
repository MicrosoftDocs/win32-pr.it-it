---
description: Gli script WMI possono accedere alle classi dei contatori delle prestazioni WMI preinstallate, nel computer locale o in remoto.
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
ms.openlocfilehash: 42fe1ecdbaf5cdc5cbafc53117ad7c8f370dae2b4e1a3adcee3a4fcf719c995a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320444"
---
# <a name="accessing-performance-data-in-script"></a>Accesso ai dati sulle prestazioni nello script

Gli script WMI possono accedere alle classi dei contatori delle prestazioni [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes)preinstallate, nel computer locale o in remoto. Mentre gli script possono ottenere dati da classi non calcolate, ad esempio [**Win32 \_ PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)o classi formattate, [**Win32 \_ PerfFormattedData \_ PerfOS \_ Memory,**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)le classi di dati formattate possono essere più facili da usare.

Il monitoraggio dei dati sulle prestazioni con le classi dei contatori delle prestazioni richiede l'uso di un [*aggiornamento*](gloss-r.md). Usare [**l'oggetto SWbemRefresher**](swbemrefresher.md) per archiviare uno o più oggetti prestazioni per l'aggiornamento o l'aggiornamento di un singolo oggetto tramite la [**chiamata SWbemObjectEx.Refresh.**](swbemobjectex-refresh-.md) Per altre informazioni, vedere [Aggiornamento dei dati WMI negli script.](refreshing-wmi-data-in-scripts.md)

Impostando la proprietà [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) su **TRUE,** WMI si riconnette automaticamente a un provider remoto se la connessione viene interrotta in modo che non sia necessario verificare lo stato della connessione.

Come illustrato nello script di esempio di codice di script seguente, è necessario effettuare una chiamata di aggiornamento iniziale per ottenere un valore iniziale per l'oggetto che si sta aggiornando. Le chiamate di aggiornamento successive contengono quindi dati.

> [!Note]  
> Quando uno script accede ai dati dei contatori delle prestazioni WMI da un computer remoto, lo script può essere eseguito solo con l'account utente connesso corrente. WMI non supporta una [**chiamata SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) che passa credenziali utente diverse. Pertanto, l'account che chiama il computer remoto deve avere già i privilegi appropriati su tale computer.

 

Nell'esempio di codice script seguente viene illustrato come utilizzare un [**oggetto SWbemRefresher**](swbemrefresher.md) per aggiornare i dati negli oggetti contatore delle prestazioni. Per altre informazioni sull'uso dei contatori delle prestazioni in WMI, vedere [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).


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

Nell'esempio di codice script seguente viene illustrato che è necessario effettuare una chiamata di aggiornamento iniziale per ottenere un valore iniziale per l'oggetto aggiornato. Le chiamate di aggiornamento successive contengono quindi dati.

Nell'esempio di codice script seguente viene illustrato come utilizzare un [**oggetto SWbemRefresher**](swbemrefresher.md) per aggiornare i dati negli oggetti contatore delle prestazioni. Per altre informazioni sull'uso dei contatori delle prestazioni in WMI, vedere [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).


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

[Classi dei contatori delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Attività WMI: Monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
