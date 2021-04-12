---
title: Enumerazione o elenco di tutte le istanze di una risorsa
description: Il metodo Session. enumerate è l'approccio Gestione remota Windows per ottenere tutte le istanze di una risorsa specificata.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54587ce97ec6ed5e87af8b0424a6a18d684f7698
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223977"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Enumerazione o elenco di tutte le istanze di una risorsa

Il metodo [**Session. enumerate**](session-enumerate.md) è l'approccio gestione remota Windows per ottenere tutte le istanze di una risorsa specificata.

Il metodo [**Session. enumerate**](session-enumerate.md) non ottiene una raccolta in un oggetto [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) come un [**SWbemService.Exechiamata cQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) con una [query WMI](/windows/desktop/WmiSdk/querying-wmi) come parametro (ad esempio, `ExecQuery("SELECT * from Win32_LogicalDisk")` ) o una chiamata a un metodo come [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-). **Session. enumerate** e i metodi dell'oggetto [**Enumerator**](enumerator.md) sono molto più simili all'operazione dell'oggetto [TextStream](/previous-versions//312a5kbt(v=vs.85)) di scripting utilizzato per la lettura dei file come flusso.

Per leggere i file come flusso di testo, è necessario creare l'oggetto [TextStream](/previous-versions//312a5kbt(v=vs.85)) di scripting e chiamare il metodo [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) per leggere ogni riga del file. In modo analogo, è possibile chiamare il metodo [**Session. enumerate**](session-enumerate.md) per ottenere un oggetto [**enumeratore**](enumerator.md) e chiamare il metodo [**Enumerator. ReadItem**](enumerator-readitem.md) per ottenere l'elemento successivo. Come nel caso della lettura dal file di testo, è possibile chiamare la proprietà [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) per verificare se è stata raggiunta la fine degli elementi di dati.

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

    

3.  Chiamare il metodo [**Session. enumerate**](session-enumerate.md) . Questa chiamata avvia un'enumerazione. In WinRM un'operazione di enumerazione non ottiene una raccolta in modo analogo a WMI. Il metodo **Session. enumerate** stabilisce invece un WS-Management contesto di enumerazione del protocollo gestito nell'oggetto [**enumeratore**](enumerator.md) .

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Chiamare il metodo [**Enumerator. ReadItem**](enumerator-readitem.md) per ottenere l'elemento successivo dei risultati. Nel protocollo WS-Management corrisponde all'operazione pull. Usare il metodo [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) come controllo per capire quando interrompere la lettura.

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo.


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

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> <dt>

[Riferimento Gestione remota Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 