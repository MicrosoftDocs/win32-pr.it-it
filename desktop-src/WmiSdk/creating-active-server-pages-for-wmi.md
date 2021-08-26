---
description: Viene descritto come creare Microsoft Active Server Pages (ASP) che visualizzano informazioni sui computer remoti in computer in cui non è installato WMI.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Creazione di Active Server per WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee7b31a5f4874e0ae4431ac452ea604da9c154bbb78e8debb91aad7ea892fa09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030611"
---
# <a name="creating-active-server-pages-for-wmi"></a>Creazione di Active Server per WMI

Microsoft Active Server Pages (ASP) può creare pagine Web dinamiche includendo script lato server e lato client. Le pagine ASP possono essere molto più veloci delle pagine HTML client perché la maggior parte delle operazioni viene eseguita sul server. È inoltre possibile utilizzare le pagine ASP per visualizzare informazioni sui computer remoti in altri computer in cui non è installato Windows Management Instrumentation (WMI).

La procedura seguente descrive come usare WMI con ASP.

**Per usare WMI con ASP**

1.  Scrivere una pagina ASP (.asp) che usa WMI e posizionarla in una directory accessibile al server Web.

    Gli script ASP per WMI possono essere sviluppati con diversi linguaggi di scripting, tra cui VBScript. È possibile costruire la parte di script WMI di una pagina ASP esattamente come si costruisce qualsiasi altro script che usa WMI, con una restrizione importante: non è possibile usare metodi WMI asincroni all'interno delle pagine ASP. Si noti anche che tutte **le chiamate a GetObject** **o CreateObject** devono essere nel codice lato server. Per altre informazioni, vedere [Scripting API for WMI](scripting-api-for-wmi.md).

2.  Configurare la configurazione dell'autenticazione Internet Information Services (IIS). Per altre informazioni, vedere [Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).
3.  Disabilitare l'accesso anonimo e Windows'autenticazione integrata per il file ASP. È possibile configurare queste impostazioni per la pagina ASP usando  lo snap-in IIS disponibile nella cartella Strumenti di amministrazione **del Pannello di controllo**.

## <a name="wmi-asp-page-example"></a>Esempio di pagina ASP WMI

L'esempio seguente usa Windows Management Instrumentation (WMI) all'interno di una pagina Active Server (ASP) per visualizzare l'indirizzo IP e le impostazioni predefinite del gateway IP per il server da cui viene eseguito lo script.


```VB
<%@ LANGUAGE="VBSCRIPT"%>
<HTML>
<HEAD>
<TITLE>WMI ASP Example:
    Read Default Gateway and IP Address information </TITLE>
</HEAD>

<BODY>

<%
On Error Resume Next
set IPConfigSet = GetObject("winmgmts:" _
   & "{impersonationLevel=impersonate}!root\cimv2").ExecQuery" _
    & "("SELECT IPAddress, DefaultIPGateway "" _ 
    & " FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=TRUE")
%>

<%If Err <> 0 Then %>
    <%if err.number = -2147217405 then%>
        <p>Error 0x80041003: Access Denied: 
           Check permissions and file security for this ASP file.</p>
    <%else%>
        <p>Error description: <%=Err.description%> 
           error number <%=Err.number%></p>
    <%end if%>

<%end if %>

<%for each IPConfig in IPConfigSet%>

    <%if Not IsNull(IPConfig.IPAddress) then %>
        <%for i=LBound(IPConfig.IPAddress) 
            to UBound(IPConfig.IPAddress)%>
            <p>IP Address: <%=IPConfig.IPAddress(i)%></p>
        <%next%>
    <%end if%>
    

    <%if Not IsNull(IPConfig.DefaultIPGateway) then %>
        <%for i=LBound(IPConfig.DefaultIPGateway) 
            to UBound(IPConfig.DefaultIPGateway)%>
            <p>Default IP Gateway: 
                <%=IPConfig.DefaultIPGateway(i)%></p>
        <%next%>
    <%end if%>
<%next%>

<%If Err <> 0 Then %>
    <p>error description: <%=Err.description%> 
       error number <%=Err.number%></p>
<%end if %>

</BODY>
</HTML>
```



 

 



