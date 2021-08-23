---
title: Scripting in Windows Remote Management
description: L'API scripting in WinRM e l'API COM per C++ sono progettate per riflettere da vicino le operazioni WS-Management protocollo.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Scripting in Windows Remote Management
- Windows Gestione remota, scripting in
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c10d36420b2826162a6ed5e3fb6bf69408a74032faafac75c84c25a754cf534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795431"
---
# <a name="scripting-in-windows-remote-management"></a>Scripting in Windows Remote Management

[L'API scripting in WinRM](winrm-scripting-api.md) e l'API COM per C++ sono progettate per riflettere da vicino le operazioni WS-Management protocollo.

L'API di scripting winrm in Windows remota supporta tutte le operazioni WS-Management protocollo, ad eccezione di una. Non consente sottoscrizioni agli eventi. Per sottoscrivere eventi dal registro eventi di sistema BMC, è necessario usare gli strumenti da riga di comando Wecutil o Wevtutil. Per altre informazioni, vedere [Eventi](events.md).

L'API di scripting WinRM viene chiamata da Winrm.vbs, uno strumento da riga di comando, scritto in Visual Basic Scripting Edition (VBScript). Winrm.vbs esempi di come usare [l'API di scripting WinRM](winrm-scripting-api.md).

## <a name="using-wsman-compared-to-using-wmi-scripting"></a>Uso di WSman rispetto all'uso di scripting WMI

WMI si connette a computer remoti tramite DCOM, che richiede la configurazione descritta in [Connessione a WMI in un computer remoto](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer). WinRM non usa DCOM per connettersi a un computer remoto. Al contrario, il WS-Management invia messaggi SOAP e il servizio usa una singola porta per HTTP e una porta per il trasporto HTTPS.

A differenza dello strumento da riga di comando **winrm,** gli script devono fornire il codice XML necessario per passare al WS-Management di protocollo. Devono anche fornire URI. Per altre informazioni, vedere [URI delle risorse](resource-uris.md) e Windows gestione remota e [WMI.](windows-remote-management-and-wmi.md)

L'API scripting WMI funziona con oggetti, ad esempio istanze di [**\_ LogicalDisk Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)che rappresentano le risorse in un computer. Questa classe WMI è definita nei [*Managed Object Format (MOF),*](/windows/desktop/WmiSdk/gloss-m) archiviati in formato binario nel repository WMI. In WMI un'operazione Get per una singola risorsa o una query per più istanze restituisce oggetti WMI.

Uno script WinRM non restituisce oggetti, ma piuttosto flussi di testo XML. Per altre informazioni, vedere Windows [Gestione remota e WMI.](windows-remote-management-and-wmi.md)

## <a name="displaying-xml-output-from-winrm-scripts"></a>Visualizzazione dell'output XML dagli script winrm

L'API di scripting WinRM ottiene e riceve stringhe XML che descrivono le risorse. Il codice XML risultante è sotto forma di flusso di testo e richiede la visualizzazione di una trasformazione XML in altro modo.

Lo script WinRM seguente produce output XML non elaborato.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



Il blocco di testo seguente mostra l'output XML dello script WinRM.


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



Gli script possono usare una trasformazione XML per rendere l'output più leggibile. Per altre informazioni, vedere [Visualizzazione dell'output XML dagli script WinRM.](displaying-xml-output-from-winrm-scripts.md)

La versione seguente dello script formatta il codice XML in un output leggibile dall'utente.


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



La trasformazione XSL crea l'output seguente.


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



## <a name="winrm-script-and-winrmcmd-output"></a>Script WinRM e output di Winrm.cmd

L'output di uno script WinRM è codificato in Unicode. Se si crea un [oggetto FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) e si scrive un file dallo script, il file risultante è Unicode. Tuttavia, se si reindirizza l'output a un file, la codifica è ANSI. Se si reindirizza l'output a un file XML e nell'output sono presenti caratteri Unicode, il codice XML non sarà valido. Tenere presente che lo strumento da riga di **comando Winrm** restituisce l'output ANSI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))
</dt> <dt>

[Informazioni di riferimento su DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))
</dt> </dl>

 

 