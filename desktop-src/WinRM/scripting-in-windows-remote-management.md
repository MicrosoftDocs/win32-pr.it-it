---
title: Creazione di script in Gestione remota Windows
description: L'API di scripting in WinRM e l'API COM associata per C++ sono progettate per riflettere attentamente le operazioni del protocollo WS-Management.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Creazione di script in Gestione remota Windows
- Gestione remota Windows, creazione di script in
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 75af10fea03853de99c884eda0a74ce340683b49
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117786"
---
# <a name="scripting-in-windows-remote-management"></a><span data-ttu-id="033a3-105">Creazione di script in Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="033a3-105">Scripting in Windows Remote Management</span></span>

<span data-ttu-id="033a3-106">L' [API di scripting in WinRM](winrm-scripting-api.md) e l'API COM associata per C++ sono progettate per riflettere attentamente le operazioni del protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="033a3-106">The [Scripting API in WinRM](winrm-scripting-api.md) and the accompanying COM API for C++ are designed to closely reflect the operations of the WS-Management protocol.</span></span>

<span data-ttu-id="033a3-107">L'API di scripting WinRM in Gestione remota Windows supporta tutte le operazioni del protocollo WS-Management ad eccezione di una.</span><span class="sxs-lookup"><span data-stu-id="033a3-107">The WinRM Scripting API in Windows Remote Management supports all the WS-Management protocol operations except one.</span></span> <span data-ttu-id="033a3-108">Non consente sottoscrizioni agli eventi.</span><span class="sxs-lookup"><span data-stu-id="033a3-108">It does not allow subscriptions to events.</span></span> <span data-ttu-id="033a3-109">Per sottoscrivere gli eventi dal registro eventi di sistema BMC, è necessario usare gli strumenti da riga di comando wecutil o wevtutil.</span><span class="sxs-lookup"><span data-stu-id="033a3-109">To subscribe to events from the BMC System Event Log, you must use the Wecutil or Wevtutil command-line tools.</span></span> <span data-ttu-id="033a3-110">Per altre informazioni, vedere [Eventi](events.md).</span><span class="sxs-lookup"><span data-stu-id="033a3-110">For more information, see [Events](events.md).</span></span>

<span data-ttu-id="033a3-111">L'API di scripting WinRM viene chiamata da Winrm.vbs, uno strumento da riga di comando, scritto in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="033a3-111">The WinRM Scripting API is called by Winrm.vbs, a command-line tool, which is written in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="033a3-112">Winrm.vbs fornisce esempi su come usare l' [API di scripting WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="033a3-112">Winrm.vbs provides examples of how to use the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

## <a name="using-wsman-compared-to-using-wmi-scripting"></a><span data-ttu-id="033a3-113">Utilizzo di WSman rispetto all'utilizzo di script WMI</span><span class="sxs-lookup"><span data-stu-id="033a3-113">Using WSman Compared to Using WMI Scripting</span></span>

<span data-ttu-id="033a3-114">WMI si connette a computer remoti tramite DCOM, che richiede la configurazione descritta in [connessione a WMI in un computer remoto](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="033a3-114">WMI connects to remote computers through DCOM, which requires the configuration described in [Connecting to WMI on a Remote Computer](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span></span> <span data-ttu-id="033a3-115">WinRM non utilizza DCOM per connettersi a un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="033a3-115">WinRM does not use DCOM to connect to a remote computer.</span></span> <span data-ttu-id="033a3-116">Il protocollo WS-Management Invia invece messaggi SOAP e il servizio usa una singola porta per HTTP e una porta per il trasporto HTTPS.</span><span class="sxs-lookup"><span data-stu-id="033a3-116">Instead, the WS-Management protocol sends SOAP messages and the service uses a single port for HTTP and a port for HTTPS transport.</span></span>

<span data-ttu-id="033a3-117">A differenza dello strumento da riga di comando **WinRM** , gli script devono fornire il codice XML necessario per passare ai messaggi di protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="033a3-117">Unlike the **winrm** command-line tool, scripts must provide the XML required to pass to the WS-Management protocol messages.</span></span> <span data-ttu-id="033a3-118">Devono inoltre fornire URI.</span><span class="sxs-lookup"><span data-stu-id="033a3-118">They must also provide URIs.</span></span> <span data-ttu-id="033a3-119">Per ulteriori informazioni, vedere [URI di risorsa](resource-uris.md) e [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="033a3-119">For more information, see [Resource URIs](resource-uris.md) and [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="033a3-120">L'API di scripting WMI funziona con gli oggetti, ad esempio le istanze di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), che rappresentano le risorse in un computer.</span><span class="sxs-lookup"><span data-stu-id="033a3-120">The WMI Scripting API works with objects, such as instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which represent resources on a computer.</span></span> <span data-ttu-id="033a3-121">Questa classe WMI è definita in file di [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) , che vengono archiviati in formato binario nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="033a3-121">This WMI class is defined in [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) files, which are stored in binary form in the WMI repository.</span></span> <span data-ttu-id="033a3-122">In WMI un'operazione get per una singola risorsa o una query per più istanze restituisce oggetti WMI.</span><span class="sxs-lookup"><span data-stu-id="033a3-122">In WMI, a Get operation for a single resource or a query for multiple instances returns WMI objects.</span></span>

<span data-ttu-id="033a3-123">Uno script WinRM non restituisce oggetti, bensì flussi di testo XML.</span><span class="sxs-lookup"><span data-stu-id="033a3-123">A WinRM script does not return objects, but rather streams of XML text.</span></span> <span data-ttu-id="033a3-124">Per ulteriori informazioni, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="033a3-124">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="033a3-125">Visualizzazione dell'output XML dagli script WinRM</span><span class="sxs-lookup"><span data-stu-id="033a3-125">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="033a3-126">L'API di scripting WinRM ottiene e riceve stringhe XML che descrivono le risorse.</span><span class="sxs-lookup"><span data-stu-id="033a3-126">The WinRM Scripting API gets and receives XML strings that describe resources.</span></span> <span data-ttu-id="033a3-127">Il codice XML risultante è sotto forma di flusso di testo e richiede la visualizzazione di una trasformazione XML in altro modo.</span><span class="sxs-lookup"><span data-stu-id="033a3-127">The resultant XML is in the form of a text stream and requires an XML transform to be displayed in some other way.</span></span>

<span data-ttu-id="033a3-128">Lo script WinRM seguente genera un output XML non elaborato.</span><span class="sxs-lookup"><span data-stu-id="033a3-128">The following WinRM script produces raw XML output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



<span data-ttu-id="033a3-129">Il blocco di testo seguente mostra l'output XML dello script WinRM.</span><span class="sxs-lookup"><span data-stu-id="033a3-129">The following block of text shows the XML output from the WinRM script.</span></span>


```XML
<p:Win32_Service xmlns:xsi="https://www.w3.org/2001/XMLSchema-
instance" xmlns:p="http://schemas.microsoft.com/wbem/wsman/1
/wmi/root/cimv2/Win32_Service" xmlns:cim="https://schemas.dmtf
.org/wbem/wsman/1/base" cim:Class="Win32_Service"><p:AcceptP
ause>false</p:AcceptPause><p:AcceptStop>true</p:AcceptStop>
<p:Caption>Print Spooler</p:Caption><p:CheckPoint>0</p:CheckP
oint><p:CreationClassName>Win32_Service</p:CreationClassName>
<p:Description>Loads files to memory for later printing</p:De
scription><p:DesktopInteract>true</p:DesktopInteract><p:Displ
ayName>Print Spooler</p:DisplayName><p:ErrorControl>Normal</p
:ErrorControl><p:ExitCode>0</p:ExitCode><p:InstallDate xsi:ni
l="true"/><p:Name>spooler</p:Name><p:PathName>C:\Windows\Syst
em32\spoolsv.exe</p:PathName><p:ProcessId>1720</p:ProcessId><
p:ServiceSpecificExitCode>0</p:ServiceSpecificExitCode><p:Ser
viceType>Own Process</p:ServiceType><p:Started>true</p:Starte
d><p:StartMode>Auto</p:StartMode><p:StartName>LocalSystem</p:
StartName><p:State>Running</p:State><p:Status>OK</p:Status><p
:SystemCreationClassName>Win32_ComputerSystem</p:SystemCreati
onClassName><p:SystemName>wsplab6-4</p:SystemName><p:TagId>0<
/p:TagId><p:WaitHint>0</p:WaitHint><cim:Location xmlns:cim="h
ttp://schemas.dmtf.org/wbem/wsman/1/base" xmlns:a="https://sc
hemas.xmlsoap.org/ws/2004/08/addressing" xmlns:w="https://sche
mas.dmtf.org/wbem/wsman/1/wsman"><a:Address>https://schemas.xm
lsoap.org/ws/2004/08/addressing/role/anonymous</a:Address><a:
ReferenceParameters><w:ResourceURI>https://schemas.microsoft.c
om/wbem/wsman/1/wmi/root/cimv2/Win32_Service</w:ResourceURI><
w:SelectorSet><w:Selector Name="Name">spooler</w:Selector></w
:SelectorSet></a:ReferenceParameters></cim:Location></p:Win32
_Service>
```



<span data-ttu-id="033a3-130">Gli script possono usare una trasformazione XML per rendere più leggibile questo output.</span><span class="sxs-lookup"><span data-stu-id="033a3-130">Your scripts can use an XML transform to make this output more readable.</span></span> <span data-ttu-id="033a3-131">Per ulteriori informazioni, vedere [visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="033a3-131">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="033a3-132">La versione seguente dello script formatta il codice XML in output leggibile.</span><span class="sxs-lookup"><span data-stu-id="033a3-132">The following version of the script formats the XML into human-readable output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xslFile.Load( "WsmTxt.xsl" )
Wscript.Echo xmlFile.TransformNode( xslFile )
```



<span data-ttu-id="033a3-133">La trasformazione XSL crea il seguente output.</span><span class="sxs-lookup"><span data-stu-id="033a3-133">The XSL transform creates the following output.</span></span>


```XML
Win32_Service
    AcceptPause = false
    AcceptStop = true
    Caption = Print Spooler
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = Loads files to memory for later printing
    DesktopInteract = true
    DisplayName = Print Spooler
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = Spooler
    PathName = C:\Windows\System32\spoolsv.exe
    ProcessId = 1720
    ServiceSpecificExitCode = 0
    ServiceType = Own Process
    Started = true
    StartMode = Auto
    StartName = LocalSystem
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = wsplab6-4
    TagId = 0
    WaitHint = 0
```



## <a name="winrm-script-and-winrmcmd-output"></a><span data-ttu-id="033a3-134">Script WinRM e output WinRM. cmd</span><span class="sxs-lookup"><span data-stu-id="033a3-134">WinRM Script and Winrm.cmd Output</span></span>

<span data-ttu-id="033a3-135">L'output di uno script WinRM è codificato in Unicode.</span><span class="sxs-lookup"><span data-stu-id="033a3-135">The output from a WinRM script is encoded in Unicode.</span></span> <span data-ttu-id="033a3-136">Se si crea un [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) e si scrive un file dallo script, il file risultante sarà Unicode.</span><span class="sxs-lookup"><span data-stu-id="033a3-136">If you create a [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) and write a file from the script, the resulting file is Unicode.</span></span> <span data-ttu-id="033a3-137">Tuttavia, se si reindirizza l'output a un file, la codifica è ANSI.</span><span class="sxs-lookup"><span data-stu-id="033a3-137">However, if you redirect the output to a file, the encoding is ANSI.</span></span> <span data-ttu-id="033a3-138">Se l'output viene reindirizzato a un file XML e sono presenti caratteri Unicode nell'output, il codice XML non sarà valido.</span><span class="sxs-lookup"><span data-stu-id="033a3-138">If you redirect the output to an XML file and there are Unicode characters in the output, the XML will be invalid.</span></span> <span data-ttu-id="033a3-139">Tenere presente che lo strumento da riga di comando **WinRM** restituisce ANSI.</span><span class="sxs-lookup"><span data-stu-id="033a3-139">Be aware that the **Winrm** command-line tool outputs ANSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="033a3-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="033a3-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="033a3-141">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="033a3-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="033a3-142">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="033a3-142">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

<span data-ttu-id="033a3-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="033a3-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="033a3-144">[Riferimento DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="033a3-144">[DOM Reference](/previous-versions/windows/desktop/ms764730(v=vs.85))</span></span>
</dt> </dl>

 

 