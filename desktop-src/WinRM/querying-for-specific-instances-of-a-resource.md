---
title: Esecuzione di query per istanze specifiche di una risorsa
description: La chiamata a Session. enumerate dispone di parametri facoltativi che limitano l'enumerazione in una query.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299818"
---
# <a name="querying-for-specific-instances-of-a-resource"></a><span data-ttu-id="a342d-103">Esecuzione di query per istanze specifiche di una risorsa</span><span class="sxs-lookup"><span data-stu-id="a342d-103">Querying for Specific Instances of a Resource</span></span>

<span data-ttu-id="a342d-104">La chiamata a [**Session. enumerate**](session-enumerate.md) dispone di parametri facoltativi che limitano l'enumerazione in una query.</span><span class="sxs-lookup"><span data-stu-id="a342d-104">The call to [**Session.Enumerate**](session-enumerate.md) has optional parameters that narrow the enumeration into a query.</span></span> <span data-ttu-id="a342d-105">Poiché l' [API di scripting WinRM](winrm-scripting-api.md) e l' [API C++ WinRM](winrm-c---api.md) sono strettamente modellate sul protocollo di WS-Management sottostante, i parametri utilizzano la stessa terminologia per l'esecuzione di query come protocollo:*filtro* e *dialetto del filtro*.</span><span class="sxs-lookup"><span data-stu-id="a342d-105">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) are closely modeled on the underlying WS-Management protocol, the parameters use the same terminology for querying as the protocol—*filter* and *filter dialect*.</span></span>

<span data-ttu-id="a342d-106">È possibile usare i parametri Filter e dialetto di [**Session. enumerate**](session-enumerate.md) oppure è possibile creare e fornire un oggetto [**resourceLocator**](resourcelocator.md) e il metodo [**AddSelector**](resourcelocator-addselector.md) , ma non è possibile eseguire entrambe le operazioni.</span><span class="sxs-lookup"><span data-stu-id="a342d-106">You can either use the filter and dialect parameters of [**Session.Enumerate**](session-enumerate.md) or you can construct and supply a [**ResourceLocator**](resourcelocator.md) object and the [**AddSelector**](resourcelocator-addselector.md) method, but you cannot do both.</span></span>

<span data-ttu-id="a342d-107">Questa procedura consente di eseguire una query per le schede di rete con binding TCP/IP e abilitati.</span><span class="sxs-lookup"><span data-stu-id="a342d-107">This procedure executes a query for network adapters that have TCP/IP bound and enabled.</span></span> <span data-ttu-id="a342d-108">La query richiede tutte le istanze di [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) con la proprietà **IpEnabled** impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="a342d-108">The query requests all the instances of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) that have the **IpEnabled** property set to **True**.</span></span> <span data-ttu-id="a342d-109">Fatta eccezione per l'aggiunta del *filtro* e del *dialetto*, la query viene gestita come una semplice enumerazione.</span><span class="sxs-lookup"><span data-stu-id="a342d-109">Except for the addition of the *filter* and *dialect*, the query is handled like a simple enumeration.</span></span>

<span data-ttu-id="a342d-110">In questo esempio, il nome della risorsa per la costante di risorsa è rappresentato da un asterisco " \* " perché il nome della classe, [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), è già indicato nella stringa *strFilter* .</span><span class="sxs-lookup"><span data-stu-id="a342d-110">In this example, the resource name for the Resource constant is represented by an asterisk "\*" because the class name, [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), is already mentioned in the *strFilter* string.</span></span>

<span data-ttu-id="a342d-111">**Per eseguire una query per istanze specifiche di una risorsa**</span><span class="sxs-lookup"><span data-stu-id="a342d-111">**To query for specific instances of a resource**</span></span>

1.  <span data-ttu-id="a342d-112">Per semplificare la lettura, definire gli URI come costanti.</span><span class="sxs-lookup"><span data-stu-id="a342d-112">For ease-of-reading, define URIs as constants.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  <span data-ttu-id="a342d-113">Crea una sessione.</span><span class="sxs-lookup"><span data-stu-id="a342d-113">Create a session.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  <span data-ttu-id="a342d-114">Costruire la stringa di filtro.</span><span class="sxs-lookup"><span data-stu-id="a342d-114">Construct the filter string.</span></span> <span data-ttu-id="a342d-115">Gestione remota Windows supporta [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) come dialetto del filtro.</span><span class="sxs-lookup"><span data-stu-id="a342d-115">Windows Remote Management supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as the filter dialect.</span></span>

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  <span data-ttu-id="a342d-116">Impostare le [**costanti di enumerazione**](enumeration-constants.md) necessarie nel parametro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="a342d-116">Set any required [**enumeration constants**](enumeration-constants.md) in the *flags* parameter.</span></span>

    <span data-ttu-id="a342d-117">Tenere presente che se i flag includono le [**costanti di enumerazione**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow** , il servizio WinRM restituisce il codice di errore **errore \_ WSMan \_ modalità di polimorfismo non \_ \_ supportata**.</span><span class="sxs-lookup"><span data-stu-id="a342d-117">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then WinRM service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

5.  <span data-ttu-id="a342d-118">Chiamare il metodo [**Session. enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="a342d-118">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="a342d-119">Questa chiamata avvia un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="a342d-119">This call starts an enumeration.</span></span> <span data-ttu-id="a342d-120">Il metodo **Session. enumerate** stabilisce un contesto di enumerazione del protocollo WS-Management, gestito nell'oggetto [**enumeratore**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="a342d-120">The **Session.Enumerate** method establishes a WS-Management protocol enumeration context, maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  <span data-ttu-id="a342d-121">Chiamare il metodo [**Enumerator. ReadItem**](enumerator-readitem.md) per ottenere l'elemento successivo dei risultati.</span><span class="sxs-lookup"><span data-stu-id="a342d-121">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="a342d-122">Nel protocollo WS-Management corrisponde all'operazione pull.</span><span class="sxs-lookup"><span data-stu-id="a342d-122">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="a342d-123">Usare il metodo [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) come controllo per capire quando interrompere la lettura.</span><span class="sxs-lookup"><span data-stu-id="a342d-123">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

<span data-ttu-id="a342d-124">Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo.</span><span class="sxs-lookup"><span data-stu-id="a342d-124">The following VBScript code example shows the complete script.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="a342d-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a342d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a342d-126">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="a342d-126">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="a342d-127">Enumerazione o elenco di tutte le istanze di una risorsa</span><span class="sxs-lookup"><span data-stu-id="a342d-127">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="a342d-128">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="a342d-128">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 