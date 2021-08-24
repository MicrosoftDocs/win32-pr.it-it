---
title: Enumerazione o elenco di tutte le istanze di una risorsa
description: Il metodo Session.Enumerate è l'Windows di gestione remota per ottenere tutte le istanze di una risorsa specificata.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f510d0e0cc8115ca4dca7c7e46dd5e987ef0dd15dd4fa7d92e47d737e467d8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679991"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Enumerazione o elenco di tutte le istanze di una risorsa

Il [**metodo Session.Enumerate**](session-enumerate.md) è l'Windows di gestione remota per ottenere tutte le istanze di una risorsa specificata.

Il metodo [**Session.Enumerate**](session-enumerate.md) non ottiene una raccolta in un oggetto [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) come una chiamata [**cQuerySWbemService.Exe**](/windows/desktop/WmiSdk/swbemservices-execquery) con una [query WMI](/windows/desktop/WmiSdk/querying-wmi) come parametro (ad esempio, ) o una chiamata a un metodo come `ExecQuery("SELECT * from Win32_LogicalDisk")` [**SWbemObject.Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-). **I metodi dell'oggetto Session.Enumerate** e [**Enumerator**](enumerator.md) sono molto più simili al funzionamento dell'oggetto [TextStream](/previous-versions//312a5kbt(v=vs.85)) di scripting usato per la lettura di file come flusso.

Per leggere i file come flusso di testo, è necessario creare l'oggetto [TextStream](/previous-versions//312a5kbt(v=vs.85)) di scripting e chiamare il metodo [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) per leggere ogni riga del file. In modo analogo, è possibile chiamare il metodo [**Session.Enumerate**](session-enumerate.md) per ottenere un oggetto [**Enumerator**](enumerator.md) e chiamare il metodo [**Enumerator.ReadItem**](enumerator-readitem.md) per ottenere l'elemento successivo. Come nel caso della lettura dal file di testo, è possibile chiamare la proprietà [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) per verificare se è stata raggiunta la fine degli elementi di dati.

**Per enumerare una risorsa**

1.  Crea una sessione.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  Costruire l'URI per identificare la risorsa.

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  Chiamare il [**metodo Session.Enumerate.**](session-enumerate.md) Questa chiamata avvia un'enumerazione. In WinRM, un'operazione di enumerazione non ottiene una raccolta allo stesso modo di WMI. Il metodo **Session.Enumerate stabilisce** invece un contesto WS-Management di enumerazione del protocollo gestito nell'oggetto [**Enumerator.**](enumerator.md)

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Chiamare il [**metodo Enumerator.ReadItem**](enumerator-readitem.md) per ottenere l'elemento successivo dei risultati. Nel WS-Management, corrisponde all'operazione pull. Usare il [**metodo Enumerator.AtEndOfStream**](enumerator-atendofstream.md) come controllo per sapere quando interrompere la lettura.

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

Nell'esempio di codice VBScript seguente viene illustrato lo script completo.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[Windows Informazioni di riferimento sulla gestione remota](windows-remote-management-reference.md)
</dt> </dl>

 

 