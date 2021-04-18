---
description: Viene descritto come creare Microsoft Active Server Pages (ASP) che visualizza informazioni sui computer remoti nei computer in cui non è installato WMI.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Creazione di Active Server pagine per WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 52143284be54868d36b55a6dd86e0b49c82d863d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319301"
---
# <a name="creating-active-server-pages-for-wmi"></a>Creazione di Active Server pagine per WMI

Microsoft Active Server Pages (ASP) può creare pagine Web dinamiche includendo gli script lato server e lato client. Le pagine ASP possono essere molto più veloci rispetto alle pagine HTML del client perché la maggior parte del lavoro viene eseguita sul server. È inoltre possibile utilizzare le pagine ASP per visualizzare informazioni sui computer remoti in altri computer in cui non è installato Strumentazione gestione Windows (WMI).

Nella procedura seguente viene descritto come utilizzare WMI con ASP.

**Per utilizzare WMI con ASP**

1.  Scrivere una pagina ASP (. asp) che utilizza WMI e posizionarla in una directory accessibile al server Web.

    Gli script ASP per WMI possono essere sviluppati con diversi linguaggi di scripting, incluso VBScript. È possibile costruire la parte script WMI di una pagina ASP esattamente come si costruisce qualsiasi altro script che utilizza WMI, con una restrizione importante: non è possibile utilizzare metodi WMI asincroni nelle pagine ASP. Si noti inoltre che tutte le chiamate a **GetObject** o **CreateObject** devono trovarsi nel codice sul lato server. Per ulteriori informazioni, vedere [scripting API for WMI](scripting-api-for-wmi.md).

2.  Configurare la configurazione dell'autenticazione per Internet Information Services (IIS). Per ulteriori informazioni, vedere [la pagina relativa alla configurazione di IIS 5 e versioni successive per lo scripting ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).
3.  Disabilitare l'accesso anonimo e abilitare l'autenticazione integrata di Windows per il file ASP. È possibile configurare queste impostazioni per la pagina ASP tramite lo snap-in IIS disponibile nella cartella **strumenti di amministrazione** del pannello di **controllo**.

## <a name="wmi-asp-page-example"></a>Esempio di pagina ASP WMI

Nell'esempio seguente viene utilizzato Strumentazione gestione Windows (WMI) in una pagina di Active Server (ASP) per visualizzare le impostazioni indirizzo IP e gateway IP predefinito per il server da cui viene eseguito lo script.


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



 

 



