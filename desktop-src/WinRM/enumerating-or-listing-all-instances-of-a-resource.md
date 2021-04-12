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
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a><span data-ttu-id="34cf9-103">Enumerazione o elenco di tutte le istanze di una risorsa</span><span class="sxs-lookup"><span data-stu-id="34cf9-103">Enumerating or Listing All Instances of a Resource</span></span>

<span data-ttu-id="34cf9-104">Il metodo [**Session. enumerate**](session-enumerate.md) è l'approccio gestione remota Windows per ottenere tutte le istanze di una risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="34cf9-104">The [**Session.Enumerate**](session-enumerate.md) method is the Windows Remote Management approach to obtaining all the instances of a specified resource.</span></span>

<span data-ttu-id="34cf9-105">Il metodo [**Session. enumerate**](session-enumerate.md) non ottiene una raccolta in un oggetto [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) come un [**SWbemService.Exechiamata cQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) con una [query WMI](/windows/desktop/WmiSdk/querying-wmi) come parametro (ad esempio, `ExecQuery("SELECT * from Win32_LogicalDisk")` ) o una chiamata a un metodo come [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="34cf9-105">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in a [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) object like a [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) call with a [WMI query](/windows/desktop/WmiSdk/querying-wmi) as a parameter (for example, `ExecQuery("SELECT * from Win32_LogicalDisk")`), or a call to a method like [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span> <span data-ttu-id="34cf9-106">**Session. enumerate** e i metodi dell'oggetto [**Enumerator**](enumerator.md) sono molto più simili all'operazione dell'oggetto [TextStream](/previous-versions//312a5kbt(v=vs.85)) di scripting utilizzato per la lettura dei file come flusso.</span><span class="sxs-lookup"><span data-stu-id="34cf9-106">**Session.Enumerate** and the [**Enumerator**](enumerator.md) object methods are much more similar to the operation of the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object that is used for reading files as a stream.</span></span>

<span data-ttu-id="34cf9-107">Per leggere i file come flusso di testo, è necessario creare l'oggetto [TextStream](/previous-versions//312a5kbt(v=vs.85)) di scripting e chiamare il metodo [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) per leggere ogni riga del file.</span><span class="sxs-lookup"><span data-stu-id="34cf9-107">To read files as a text stream, you must create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="34cf9-108">In modo analogo, è possibile chiamare il metodo [**Session. enumerate**](session-enumerate.md) per ottenere un oggetto [**enumeratore**](enumerator.md) e chiamare il metodo [**Enumerator. ReadItem**](enumerator-readitem.md) per ottenere l'elemento successivo.</span><span class="sxs-lookup"><span data-stu-id="34cf9-108">In a similar way, you can call the [**Session.Enumerate**](session-enumerate.md) method to obtain an [**Enumerator**](enumerator.md) object and call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to get the next item.</span></span> <span data-ttu-id="34cf9-109">Come nel caso della lettura dal file di testo, è possibile chiamare la proprietà [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) per verificare se è stata raggiunta la fine degli elementi di dati.</span><span class="sxs-lookup"><span data-stu-id="34cf9-109">As is the case when reading from the text file, you can call the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

<span data-ttu-id="34cf9-110">**Per enumerare una risorsa**</span><span class="sxs-lookup"><span data-stu-id="34cf9-110">**To enumerate a resource**</span></span>

1.  <span data-ttu-id="34cf9-111">Crea una sessione.</span><span class="sxs-lookup"><span data-stu-id="34cf9-111">Create a session.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  <span data-ttu-id="34cf9-112">Costruire l'URI per identificare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="34cf9-112">Construct the URI to identify the resource.</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  <span data-ttu-id="34cf9-113">Chiamare il metodo [**Session. enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="34cf9-113">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="34cf9-114">Questa chiamata avvia un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="34cf9-114">This call starts an enumeration.</span></span> <span data-ttu-id="34cf9-115">In WinRM un'operazione di enumerazione non ottiene una raccolta in modo analogo a WMI.</span><span class="sxs-lookup"><span data-stu-id="34cf9-115">In WinRM, an enumeration operation does not obtain a collection in the same way that WMI does.</span></span> <span data-ttu-id="34cf9-116">Il metodo **Session. enumerate** stabilisce invece un WS-Management contesto di enumerazione del protocollo gestito nell'oggetto [**enumeratore**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="34cf9-116">Instead, the **Session.Enumerate** method establishes a WS-Management protocol enumeration context that is maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  <span data-ttu-id="34cf9-117">Chiamare il metodo [**Enumerator. ReadItem**](enumerator-readitem.md) per ottenere l'elemento successivo dei risultati.</span><span class="sxs-lookup"><span data-stu-id="34cf9-117">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="34cf9-118">Nel protocollo WS-Management corrisponde all'operazione pull.</span><span class="sxs-lookup"><span data-stu-id="34cf9-118">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="34cf9-119">Usare il metodo [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) come controllo per capire quando interrompere la lettura.</span><span class="sxs-lookup"><span data-stu-id="34cf9-119">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

<span data-ttu-id="34cf9-120">Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo.</span><span class="sxs-lookup"><span data-stu-id="34cf9-120">The following VBScript code example shows the complete script.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="34cf9-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34cf9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34cf9-122">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="34cf9-122">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="34cf9-123">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="34cf9-123">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="34cf9-124">Riferimento Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="34cf9-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 