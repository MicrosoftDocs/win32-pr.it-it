---
description: Per ricevere notifiche dal provider del registro di sistema, un'applicazione di gestione deve registrarsi come consumer di eventi temporanei.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrazione per eventi registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318540"
---
# <a name="registering-for-system-registry-events"></a>Registrazione per eventi registro di sistema

Per ricevere notifiche dal provider [del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) , un'applicazione di gestione deve registrarsi come consumer di eventi temporanei. La maggior parte dei requisiti per la registrazione per il provider del registro di sistema è identica a quella di qualsiasi altra registrazione di eventi, ad eccezione del fatto che è necessario eseguire anche la procedura riportata di seguito.

Il provider del registro di sistema fornisce le classi di evento per gli eventi nel registro di sistema. Per ulteriori informazioni sulla registrazione di eventi generali, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).

Nella procedura seguente viene descritto come eseguire la registrazione per gli eventi del registro di sistema.

**Per eseguire la registrazione per gli eventi del registro di sistema**

1.  Chiamare un metodo di query di notifica.

    In uno script o in C++ usare una query di notifica, ad esempio [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) o [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync). Creare una stringa di query per il parametro *bstrQuery* di **IWbemServices:: ExecNotificationQueryAsync** o *strQuery* nello script.

2.  Determinare il tipo di evento che si desidera ricevere e creare la query.

    Nella tabella seguente sono elencate le classi di eventi del registro di sistema che è possibile utilizzare.

    

    | classe di evento                                                      | Posizione hive        | Descrizione                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)                       | N/D<br/>       | Classe di base astratta per le modifiche nel registro di sistema.<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | Monitora le modifiche apportate a una gerarchia di chiavi.<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | KeyPath<br/>   | Monitora le modifiche apportate a una singola chiave.<br/>                |
    | [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Monitora le modifiche apportate a un singolo valore.<br/>              |

    

     

    Queste classi hanno una proprietà denominata **hive** che identifica la gerarchia delle chiavi da monitorare per la modifica, ad esempio **il \_ \_ computer locale HKEY**.

    Le modifiche apportate alle **\_ classi HKEY \_ radice** e HKEY gli hive **\_ correnti \_ dell'utente** non sono supportate da [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) o dalle classi derivate, ad esempio [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).

3.  Creare la clausola WHERE per la registrazione dell'evento.

    Il provider del registro di sistema ha regole specifiche per le clausole WHERE. Per ulteriori informazioni, vedere [creazione di una clausola WHERE corretta per il provider del registro di sistema](creating-a-proper-where-clause-for-the-registry-provider.md). Per informazioni generali sulla creazione di una clausola WHERE, vedere [esecuzione di query con WQL](querying-with-wql.md).

4.  Determinare se il consumer riceve gli eventi.

    Il provider del registro di sistema non garantisce che tutti gli eventi inviati vengano recapitati. Per ulteriori informazioni, vedere [ricezione degli eventi del registro di sistema](receiving-registry-events.md).

Nell'esempio di codice VBScript seguente viene illustrato come rilevare una modifica del registro di sistema nel software del **\_ \_ computer locale HKEY** \\  \\ **Microsoft** hive o sottoalbero. Si tratta di uno script di monitoraggio che, a scopo dimostrativo, viene eseguito in un processo denominato Wscript.exe fino a quando non viene terminato in **Gestione attività**, WMI viene arrestato o il sistema operativo viene riavviato. Lo script usa una chiamata [*semisincrono*](gloss-s.md) per [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Per ulteriori informazioni sulle chiamate semisincrono, vedere [creazione di una chiamata semisincrono con VBScript](making-a-semisynchronous-call-with-vbscript.md).


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



Nell'esempio di codice VBScript seguente viene illustrato come monitorare la modifica nei valori di una chiave eseguendo la registrazione per il tipo di evento del provider del registro di sistema [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Lo script chiama un metodo asincrono, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Per ulteriori informazioni sulle chiamate asincrone e sulla sicurezza, vedere [creazione di una chiamata asincrona con VBScript](making-an-asynchronous-call-with-vbscript.md).

Lo script seguente viene eseguito a tempo indefinito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato. Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo. Per arrestarla a livello di codice, usare il metodo [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) nella \_ classe del processo Win32.


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

