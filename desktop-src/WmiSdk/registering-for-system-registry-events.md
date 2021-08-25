---
description: Per ricevere notifiche dal provider del Registro di sistema, un'applicazione di gestione deve registrarsi come consumer di eventi temporaneo.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrazione per gli eventi del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c6f60b21dee729a879aaeab676da67b06ca0a822bcfd6509bc0f406f96fecec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554246"
---
# <a name="registering-for-system-registry-events"></a>Registrazione per gli eventi del Registro di sistema

Per ricevere notifiche dal provider del [Registro di sistema,](/previous-versions/windows/desktop/regprov/system-registry-provider) un'applicazione di gestione deve registrarsi come consumer di eventi temporaneo. La maggior parte dei requisiti per la registrazione per il provider del Registro di sistema è uguale a qualsiasi altra registrazione degli eventi, con la differenza che è necessario eseguire anche la procedura seguente.

Il provider del Registro di sistema fornisce classi di eventi per gli eventi nel Registro di sistema. Per altre informazioni sulla registrazione generale degli eventi, vedere [Ricezione di un evento WMI](receiving-a-wmi-event.md).

La procedura seguente descrive come eseguire la registrazione per gli eventi del Registro di sistema.

**Per eseguire la registrazione per gli eventi del Registro di sistema**

1.  Chiamare un metodo di query di notifica.

    Nello script o in C++, usare una query di notifica, ad esempio [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) o [**IWbemServices::ExecNotificationQueryAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) Creare una stringa di query per il *parametro bstrQuery* **di IWbemServices::ExecNotificationQueryAsync** o *strQuery* nello script.

2.  Determinare il tipo di evento da ricevere e creare la query.

    Nella tabella seguente sono elencate le classi di eventi del Registro di sistema che è possibile usare.

    

    | classe di evento                                                      | Posizione hive        | Descrizione                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)                       | N/A<br/>       | Classe di base astratta per le modifiche nel Registro di sistema.<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | Monitora le modifiche apportate a una gerarchia di chiavi.<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | KeyPath<br/>   | Monitora le modifiche apportate a una singola chiave.<br/>                |
    | [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Monitora le modifiche apportate a un singolo valore.<br/>              |

    

     

    Queste classi hanno una proprietà denominata **Hive** che identifica la gerarchia di chiavi da monitorare per la modifica, ad esempio **HKEY \_ LOCAL \_ MACHINE**.

    Le modifiche agli hive **HKEY \_ CLASSES \_ ROOT** e **HKEY \_ CURRENT \_ USER** non sono supportate da [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) o dalle classi derivate da esso, ad esempio [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).

3.  Creare la clausola WHERE per la registrazione dell'evento.

    Il provider del Registro di sistema ha regole specifiche per le clausole WHERE. Per altre informazioni, vedere [Creazione di una clausola WHERE appropriata per il provider del Registro di sistema](creating-a-proper-where-clause-for-the-registry-provider.md). Per informazioni più generali sulla creazione di una clausola WHERE, vedere [Esecuzione di query con WQL.](querying-with-wql.md)

4.  Determinare se il consumer sta ricevendo eventi.

    Il provider del Registro di sistema non garantisce che tutti gli eventi inviati siano recapitati. Per altre informazioni, vedere [Ricezione di eventi del Registro di sistema](receiving-registry-events.md).

Nell'esempio di codice VBScript seguente viene illustrato come rilevare una modifica del Registro di sistema nell'hive o nel sottoalbero **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft.** Si tratta di uno script di monitoraggio che, a scopo dimostrativo, viene eseguito in un processo denominato Wscript.exe finché non viene terminato **in Gestione attività**, WMI viene arrestato o il sistema operativo non viene riavviato. Lo script usa una [*chiamata semisincrona*](gloss-s.md) a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Per altre informazioni sulle chiamate semisincronose, vedere Esecuzione di una chiamata [semisincrona con VBScript.](making-a-semisynchronous-call-with-vbscript.md)


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



Nell'esempio di codice VBScript seguente viene illustrato come monitorare la modifica dei valori di una chiave registrando per il tipo di evento del provider del Registro di sistema [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Lo script chiama un metodo asincrono, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Per altre informazioni sulle chiamate asincrone e sulla sicurezza, vedere [Esecuzione di una chiamata asincrona con VBScript.](making-an-asynchronous-call-with-vbscript.md)

Lo script seguente viene eseguito a tempo indeterminato fino al riavvio del computer, all'arresto di WMI o all'arresto dello script. Per arrestare manualmente lo script, usare Gestione attività per arrestare il processo. Per arrestarlo a livello di codice, usare [**il metodo Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) nella classe Win32 \_ Process.


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



 

