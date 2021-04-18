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
# <a name="creating-active-server-pages-for-wmi"></a><span data-ttu-id="6e99e-103">Creazione di Active Server pagine per WMI</span><span class="sxs-lookup"><span data-stu-id="6e99e-103">Creating Active Server Pages for WMI</span></span>

<span data-ttu-id="6e99e-104">Microsoft Active Server Pages (ASP) può creare pagine Web dinamiche includendo gli script lato server e lato client.</span><span class="sxs-lookup"><span data-stu-id="6e99e-104">Microsoft Active Server Pages (ASP) can create dynamic webpages by including both server-side and client-side scripts.</span></span> <span data-ttu-id="6e99e-105">Le pagine ASP possono essere molto più veloci rispetto alle pagine HTML del client perché la maggior parte del lavoro viene eseguita sul server.</span><span class="sxs-lookup"><span data-stu-id="6e99e-105">ASP pages can be much faster than client HTML pages because most of the work is done on the server.</span></span> <span data-ttu-id="6e99e-106">È inoltre possibile utilizzare le pagine ASP per visualizzare informazioni sui computer remoti in altri computer in cui non è installato Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6e99e-106">You can also use ASP pages to display information about remote computers to other computers that do not have Windows Management Instrumentation (WMI) installed.</span></span>

<span data-ttu-id="6e99e-107">Nella procedura seguente viene descritto come utilizzare WMI con ASP.</span><span class="sxs-lookup"><span data-stu-id="6e99e-107">The following procedure describes how to use WMI with ASP.</span></span>

<span data-ttu-id="6e99e-108">**Per utilizzare WMI con ASP**</span><span class="sxs-lookup"><span data-stu-id="6e99e-108">**To use WMI with ASP**</span></span>

1.  <span data-ttu-id="6e99e-109">Scrivere una pagina ASP (. asp) che utilizza WMI e posizionarla in una directory accessibile al server Web.</span><span class="sxs-lookup"><span data-stu-id="6e99e-109">Write an ASP page (.asp) that uses WMI, and place it in a directory accessible to your web server.</span></span>

    <span data-ttu-id="6e99e-110">Gli script ASP per WMI possono essere sviluppati con diversi linguaggi di scripting, incluso VBScript.</span><span class="sxs-lookup"><span data-stu-id="6e99e-110">ASP scripts for WMI can be developed with several scripting languages, including VBScript.</span></span> <span data-ttu-id="6e99e-111">È possibile costruire la parte script WMI di una pagina ASP esattamente come si costruisce qualsiasi altro script che utilizza WMI, con una restrizione importante: non è possibile utilizzare metodi WMI asincroni nelle pagine ASP.</span><span class="sxs-lookup"><span data-stu-id="6e99e-111">You can construct the WMI script part of an ASP page exactly as you construct any other script that uses WMI, with one important restriction: you cannot use asynchronous WMI methods within ASP pages.</span></span> <span data-ttu-id="6e99e-112">Si noti inoltre che tutte le chiamate a **GetObject** o **CreateObject** devono trovarsi nel codice sul lato server.</span><span class="sxs-lookup"><span data-stu-id="6e99e-112">Note also that any calls to **GetObject** or **CreateObject** must be in the server-side code.</span></span> <span data-ttu-id="6e99e-113">Per ulteriori informazioni, vedere [scripting API for WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6e99e-113">For more information, see [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="6e99e-114">Configurare la configurazione dell'autenticazione per Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="6e99e-114">Set up authentication configuration for Internet Information Services (IIS).</span></span> <span data-ttu-id="6e99e-115">Per ulteriori informazioni, vedere [la pagina relativa alla configurazione di IIS 5 e versioni successive per lo scripting ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="6e99e-115">For more information, see [Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>
3.  <span data-ttu-id="6e99e-116">Disabilitare l'accesso anonimo e abilitare l'autenticazione integrata di Windows per il file ASP.</span><span class="sxs-lookup"><span data-stu-id="6e99e-116">Disable anonymous access, and enable Windows Integrated Authentication for the ASP file.</span></span> <span data-ttu-id="6e99e-117">È possibile configurare queste impostazioni per la pagina ASP tramite lo snap-in IIS disponibile nella cartella **strumenti di amministrazione** del pannello di **controllo**.</span><span class="sxs-lookup"><span data-stu-id="6e99e-117">You can configure these settings for your ASP page by using the IIS snap-in located in the **Administrative Tools** folder of the **Control Panel**.</span></span>

## <a name="wmi-asp-page-example"></a><span data-ttu-id="6e99e-118">Esempio di pagina ASP WMI</span><span class="sxs-lookup"><span data-stu-id="6e99e-118">WMI ASP Page Example</span></span>

<span data-ttu-id="6e99e-119">Nell'esempio seguente viene utilizzato Strumentazione gestione Windows (WMI) in una pagina di Active Server (ASP) per visualizzare le impostazioni indirizzo IP e gateway IP predefinito per il server da cui viene eseguito lo script.</span><span class="sxs-lookup"><span data-stu-id="6e99e-119">The following example uses Windows Management Instrumentation (WMI) within an Active Server Page (ASP) to display the IP address and default IP gateway settings for the server from which this script is executed.</span></span>


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



 

 



