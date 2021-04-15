---
title: Novità di Windows Server 2008
description: Windows Server 2008 introduce i nuovi elementi di programmazione seguenti per Servizi terminal.
ms.assetid: a2299b03-5e06-4984-a33f-b44c7cded513
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab74f22c41fa88147a1ef30a8f55f158e34990c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104399826"
---
# <a name="whats-new-in-windows-server-2008"></a>Novità di Windows Server 2008

Windows Server 2008 introduce i nuovi elementi di programmazione seguenti per Servizi terminal.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento di programmazione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Guida di riferimento ai canali virtuali dinamici<br/></td>
<td>Le API del canale virtuale dinamico (DVC) estendono le API del canale virtuale esistente per Servizi terminal, note come API del canale virtuale statico (SVC).<br/>
<ul>
<li><a href="dynamic-virtual-channels.md">Canali virtuali dinamici</a></li>
<li><a href="dynamic-virtual-channels-reference.md">Guida di riferimento ai canali virtuali dinamici</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Riferimento Connessione Web Desktop remoto<br/></td>
<td>Le interfacce seguenti (e i metodi e le proprietà associati) sono state aggiunte al <a href="remote-desktop-web-connection-reference.md">riferimento connessione Web Desktop remoto</a>:<br/>
<ul>
<li><a href="imsrdpclient5.md"><strong>Interfaccia IMsRdpClient5</strong></a></li>
<li><a href="imsrdpclient6.md"><strong>Interfaccia IMsRdpClient6</strong></a></li>
<li><a href="imsrdpclientadvancedsettings5.md"><strong>Interfaccia IMsRdpClientAdvancedSettings5</strong></a></li>
<li><a href="imsrdpclientadvancedsettings6.md"><strong>Interfaccia IMsRdpClientAdvancedSettings6</strong></a></li>
<li><a href="imsrdpclientnonscriptable3.md"><strong>Interfaccia IMsRdpClientNonScriptable3</strong></a></li>
<li><a href="imsrdpclientshell.md"><strong>Interfaccia IMsRdpClientShell</strong></a></li>
<li><a href="imsrdpclienttransportsettings.md"><strong>Interfaccia IMsRdpClientTransportSettings</strong></a></li>
<li><a href="imsrdpclienttransportsettings2.md"><strong>Interfaccia IMsRdpClientTransportSettings2</strong></a></li>
<li><a href="imsrdpdevice.md"><strong>Interfaccia IMsRdpDevice</strong></a></li>
<li><a href="imsrdpdevicecollection.md"><strong>Interfaccia IMsRdpDeviceCollection</strong></a></li>
<li><a href="imsrdpdrive.md"><strong>Interfaccia IMsRdpDrive</strong></a></li>
<li><a href="imsrdpdrivecollection.md"><strong>Interfaccia IMsRdpDriveCollection</strong></a></li>
<li><a href="itsremoteprogram.md"><strong>Interfaccia ITSRemoteProgram</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Informazioni di riferimento sull'API Servizi terminal<br/></td>
<td>Le funzioni seguenti sono state aggiunte alle informazioni di <a href="terminal-services-api-reference.md">riferimento sulle API di Servizi terminal</a>:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona"><strong>WTSConnectSession (funzione)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex"><strong>WTSRegisterSessionNotificationEx (funzione)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona"><strong>WTSStartRemoteControlSession (funzione)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession"><strong>WTSStopRemoteControlSession (funzione)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex"><strong>WTSUnRegisterSessionNotificationEx (funzione)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex"><strong>WTSVirtualChannelOpenEx (funzione)</strong></a></li>
</ul>
Sono state aggiunte le strutture seguenti:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta"><strong>Struttura WTSCLIENT</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa"><strong>Struttura WTSINFO</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Provider WMI di Servizi terminal<br/></td>
<td>Sono stati aggiunti i metodi e le classi seguenti al <a href="terminal-services-wmi-provider.md">provider WMI per Servizi terminal</a>.<br/>
<ul>
<li><a href="terminal-services-gateway-classes.md">Classi gateway di Servizi terminal (e metodi associati)</a></li>
<li><a href="terminal-services-license-server-classes.md">Classi del server licenze di Servizi terminal (e metodi associati)</a></li>
<li><a href="terminal-services-remoteapp-classes.md">Classi RemoteApp (e metodi associati)</a></li>
<li><a href="win32-tsdiscoveredlicenseserver.md"><strong>Classe Win32_TSDiscoveredLicenseServer</strong></a></li>
<li><a href="create-win32-terminal.md"><strong>Metodo Create della classe Win32_Terminal</strong></a></li>
<li><a href="delete-win32-terminal.md"><strong>Metodo Delete della classe Win32_Terminal</strong></a></li>
<li><a href="canaccesslicenseserver-win32-terminalservicesetting.md"><strong>Metodo CanAccessLicenseServer della classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="findlicenseservers-win32-terminalservicesetting.md"><strong>Metodo FindLicenseServers della classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getdomain-win32-terminalservicesetting.md"><strong>Metodo GetDomain della classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getgraceperioddays-win32-terminalservicesetting.md"><strong>Metodo GetGracePeriodDays della classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getwinstationdrivernames-win32-terminalservicesetting.md"><strong>Metodo GetWinstationDriverNames della classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="pinglicenseserver-win32-terminalservicesetting.md"><strong>Metodo PingLicenseServer della classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="updatedirectconnectlicenseserver-win32-terminalservicesetting.md"><strong>Metodo UpdateDirectConnectLicenseServer della classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="setuserauthenticationrequired-win32-tsgeneralsetting.md"><strong>Metodo SetUserAuthenticationRequired della classe Win32_TSGeneralSetting</strong></a></li>
<li><a href="getcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Metodo GetCurrentRedirectableAddresses della classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="setcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Metodo SetCurrentRedirectableAddresses della classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="getredirectableaddresses-win32-tssessiondirectory.md"><strong>Metodo GetRedirectableAddresses della classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="pingsessiondirectory-win32-tssessiondirectory.md"><strong>Metodo PingSessionDirectory della classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="setloadbalancingstate-win32-tssessiondirectory.md"><strong>Metodo SetLoadBalancingState della classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="setserverweight-win32-tssessiondirectory.md"><strong>Metodo SetServerWeight della classe Win32_TSSessionDirectory</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Riferimento al plug-in Gestore sessioni Servizi terminal<br/></td>
<td>Il plug-in Gestore sessioni Servizi terminal viene utilizzato per estendere le funzionalità di gestore sessioni Servizi terminal.<br/>
<ul>
<li><a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">Riferimento al plug-in Gestore sessioni Servizi terminal</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

