---
title: Visualizzazione dell'output XML dagli script winrm
description: Windows Gli script di gestione remota restituiscono xml anziché oggetti. Il formato XML non è leggibile. È possibile usare i metodi dell'API MSXML e il file XSL preinstallato per trasformare i dati in formato leggibile dall'utente.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df5c27c1fe22ae87395357aeefe681af7c041420d32b7bccbf595fab38bb060b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680021"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Visualizzazione dell'output XML dagli script winrm

Windows Gli script di gestione remota restituiscono xml anziché oggetti. Il formato XML non è leggibile. È possibile usare i metodi dell'API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) e il file XSL preinstallato per trasformare i dati in formato leggibile dall'utente.

Per altre informazioni sull'output XML di WinRM ed esempi di codice XML non elaborato e formattato, vedere [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).

Lo strumento da riga di comando **Winrm** viene fornito con un file di trasformazione denominato WsmTxt.xsl che visualizza l'output in formato tabulare. Se lo script fornisce questo file ai MSXML che eseguono tranform, l'output viene visualizzato come l'output dello **strumento Winrm.**

**Per formattare l'output XML non elaborato**

1.  Creare [**l'oggetto WSMan**](wsman.md) e creare una sessione.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  Creare MSXML oggetti che rappresentano l'output della risposta XML e la trasformazione XSL.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Ottenere dati tramite [**i metodi dell'oggetto**](session.md) Session.

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  Fornire la risposta al metodo MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) e al [metodo load](/previous-versions/windows/desktop/ms762722(v=vs.85)) per archiviare il file di trasformazione.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Usare il MSXML [metodo transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) e visualizzare o salvare l'output.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

Nell'esempio di codice VBScript seguente viene illustrato lo script completo.


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



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>Aggiunta di una subroutine portabile per trasformare il codice XML negli script

È possibile aggiungere una subroutine agli script che usa il file XSL preinstallato per convertire l'output XML non elaborato da uno script WinRM in un formato tabulare.

La subroutine seguente usa le chiamate ai MSXML di scripting per fornire l'output a WsmTxt.xsl.


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



La subroutine seguente trasforma ogni riga dei dati, come illustrato nell'esempio seguente.


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

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[Windows Informazioni di riferimento sulla gestione remota](windows-remote-management-reference.md)
</dt> </dl>

 

 