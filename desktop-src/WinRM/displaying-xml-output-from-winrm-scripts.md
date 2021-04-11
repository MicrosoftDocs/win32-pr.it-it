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
# <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="34d40-105">Visualizzazione dell'output XML dagli script WinRM</span><span class="sxs-lookup"><span data-stu-id="34d40-105">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="34d40-106">Gli script di Gestione remota Windows restituiscono XML anziché oggetti.</span><span class="sxs-lookup"><span data-stu-id="34d40-106">Windows Remote Management scripts return XML rather than objects.</span></span> <span data-ttu-id="34d40-107">Il formato XML non è leggibile.</span><span class="sxs-lookup"><span data-stu-id="34d40-107">The XML is not in a human-readable format.</span></span> <span data-ttu-id="34d40-108">È possibile utilizzare i metodi dell'API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) e il file XSL preinstallato per trasformare i dati in un formato leggibile.</span><span class="sxs-lookup"><span data-stu-id="34d40-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API and the preinstalled XSL file to transform the data into human-readable format.</span></span>

<span data-ttu-id="34d40-109">Per ulteriori informazioni sull'output XML di WinRM ed esempi di codice XML non elaborato e formattato, vedere [scripting in gestione remota Windows](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="34d40-109">For more information about WinRM XML output and examples of raw and formatted XML, see [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="34d40-110">Lo strumento da riga di comando **WinRM** include un file di trasformazione denominato WsmTxt. xsl che Visualizza l'output in un formato tabulare.</span><span class="sxs-lookup"><span data-stu-id="34d40-110">The **Winrm** command-line tool comes with a transform file named WsmTxt.xsl that displays output in a tabular form.</span></span> <span data-ttu-id="34d40-111">Se lo script fornisce questo file ai metodi MSXML che eseguono trasforma, l'output viene visualizzato come output dello strumento **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="34d40-111">If your script supplies this file to the MSXML methods that perform tranforms, the output appears the same as the output from the **Winrm** tool.</span></span>

<span data-ttu-id="34d40-112">**Per formattare l'output XML non elaborato**</span><span class="sxs-lookup"><span data-stu-id="34d40-112">**To format raw XML output**</span></span>

1.  <span data-ttu-id="34d40-113">Creare l'oggetto [**WSMan**](wsman.md) e creare una sessione.</span><span class="sxs-lookup"><span data-stu-id="34d40-113">Create the [**WSMan**](wsman.md) object and create a session.</span></span>

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  <span data-ttu-id="34d40-114">Creare oggetti MSXML che rappresentano l'output della risposta XML e la trasformazione XSL.</span><span class="sxs-lookup"><span data-stu-id="34d40-114">Create MSXML objects that represent the XML response output and the XSL transform.</span></span>

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  <span data-ttu-id="34d40-115">Ottenere i dati tramite i metodi dell'oggetto [**Session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="34d40-115">Obtain data through [**Session**](session.md) object methods.</span></span>

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  <span data-ttu-id="34d40-116">Fornire la risposta al metodo MSXML [LoadXml](/previous-versions/windows/desktop/ms754585(v=vs.85)) e il metodo [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) per archiviare il file di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="34d40-116">Supply the response to the MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) method and the [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) method to store the transform file.</span></span>

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  <span data-ttu-id="34d40-117">Usare il metodo MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) e visualizzare o salvare l'output.</span><span class="sxs-lookup"><span data-stu-id="34d40-117">Use the MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) method and display or save the output.</span></span>

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

<span data-ttu-id="34d40-118">Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo.</span><span class="sxs-lookup"><span data-stu-id="34d40-118">The following VBScript code example shows the complete script.</span></span>


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



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a><span data-ttu-id="34d40-119">Aggiunta di una subroutine portatile per trasformare XML negli script</span><span class="sxs-lookup"><span data-stu-id="34d40-119">Adding a Portable Subroutine to Transform XML to Your Scripts</span></span>

<span data-ttu-id="34d40-120">È possibile aggiungere una subroutine agli script che utilizzano il file XSL preinstallato per convertire l'output XML non elaborato da uno script WinRM in un formato tabulare.</span><span class="sxs-lookup"><span data-stu-id="34d40-120">You can add a subroutine to your scripts that uses the preinstalled XSL file to convert the raw XML output from a WinRM script to a tabular form.</span></span>

<span data-ttu-id="34d40-121">La subroutine seguente usa le chiamate ai metodi di scripting MSXML per fornire l'output a WsmTxt. Xsl.</span><span class="sxs-lookup"><span data-stu-id="34d40-121">The following subroutine uses calls to the MSXML scripting methods to supply the output to WsmTxt.xsl.</span></span>


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



<span data-ttu-id="34d40-122">La subroutine seguente trasforma ogni riga dei dati come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="34d40-122">The following subroutine transforms each line of your data as shown in the following example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="34d40-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34d40-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34d40-124">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="34d40-124">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="34d40-125">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="34d40-125">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="34d40-126">Riferimento Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="34d40-126">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 