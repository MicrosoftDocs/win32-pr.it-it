---
title: Visualizzazione dell'output XML dagli script WinRM
description: Gli script di Gestione remota Windows restituiscono XML anziché oggetti. Il formato XML non è leggibile. È possibile utilizzare i metodi dell'API MSXML e il file XSL preinstallato per trasformare i dati in un formato leggibile.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c70dd0a61181f6fc61e685641ff0ed5e3d43ffe8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047137"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Visualizzazione dell'output XML dagli script WinRM

Gli script di Gestione remota Windows restituiscono XML anziché oggetti. Il formato XML non è leggibile. È possibile utilizzare i metodi dell'API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) e il file XSL preinstallato per trasformare i dati in un formato leggibile.

Per ulteriori informazioni sull'output XML di WinRM ed esempi di codice XML non elaborato e formattato, vedere [scripting in gestione remota Windows](scripting-in-windows-remote-management.md).

Lo strumento da riga di comando **WinRM** include un file di trasformazione denominato WsmTxt. xsl che Visualizza l'output in un formato tabulare. Se lo script fornisce questo file ai metodi MSXML che eseguono trasforma, l'output viene visualizzato come output dello strumento **WinRM** .

**Per formattare l'output XML non elaborato**

1.  Creare l'oggetto [**WSMan**](wsman.md) e creare una sessione.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  Creare oggetti MSXML che rappresentano l'output della risposta XML e la trasformazione XSL.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Ottenere i dati tramite i metodi dell'oggetto [**Session**](session.md) .

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  Fornire la risposta al metodo MSXML [LoadXml](/previous-versions/windows/desktop/ms754585(v=vs.85)) e il metodo [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) per archiviare il file di trasformazione.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Usare il metodo MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) e visualizzare o salvare l'output.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>Aggiunta di una subroutine portatile per trasformare XML negli script

È possibile aggiungere una subroutine agli script che utilizzano il file XSL preinstallato per convertire l'output XML non elaborato da uno script WinRM in un formato tabulare.

La subroutine seguente usa le chiamate ai metodi di scripting MSXML per fornire l'output a WsmTxt. Xsl.


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



La subroutine seguente trasforma ogni riga dei dati come illustrato nell'esempio seguente.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
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

 

 