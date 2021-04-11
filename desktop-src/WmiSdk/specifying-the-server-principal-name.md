---
description: Il servizio di autenticazione Kerberos specifica il nome dell'entità server per garantire l'identità del computer a cui si connette.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Specifica del nome dell'entità server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a2f5aa4053b5ae7452e5f5e9c0ddcac15630ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131003"
---
# <a name="specifying-the-server-principal-name"></a><span data-ttu-id="cb1a7-103">Specifica del nome dell'entità server</span><span class="sxs-lookup"><span data-stu-id="cb1a7-103">Specifying the Server Principal Name</span></span>

<span data-ttu-id="cb1a7-104">Il servizio di autenticazione Kerberos specifica il nome dell'entità server per garantire l'identità del computer a cui si connette.</span><span class="sxs-lookup"><span data-stu-id="cb1a7-104">The Kerberos authentication service specifies the server principal name to ensure the identity of the computer to which it is connecting.</span></span> <span data-ttu-id="cb1a7-105">Specificare il nome dell'entità server nella chiamata al metodo di scripting [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) assegnando il nome del computer remoto.</span><span class="sxs-lookup"><span data-stu-id="cb1a7-105">Specify the server principal name in the call to the scripting method [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) by giving the name of the remote computer.</span></span> <span data-ttu-id="cb1a7-106">In C++ specificare il nome dell'entità server nel parametro *pServerPrincName* quando si chiama [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per il proxy.</span><span class="sxs-lookup"><span data-stu-id="cb1a7-106">In C++, specify the server principal name in the *pServerPrincName* parameter when calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) for the proxy.</span></span> <span data-ttu-id="cb1a7-107">Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="cb1a7-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="cb1a7-108">Questo parametro è obbligatorio per Kerberos per supportare l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="cb1a7-108">This parameter is required for Kerberos to support mutual authentication.</span></span> <span data-ttu-id="cb1a7-109">Tuttavia, l'utilizzo del nome dell'entità server predefinito non consente l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="cb1a7-109">However, using the default server principal name does not allow mutual authentication.</span></span> <span data-ttu-id="cb1a7-110">I client per i quali l'autenticazione reciproca è critica, è necessario specificare un nome di entità server corrispondente all'identità del server utilizzata dal servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="cb1a7-110">Clients for which mutual authentication is critical, must specify a server principal name that matches the server identity that the WMI service is using.</span></span> <span data-ttu-id="cb1a7-111">Per ulteriori informazioni sull'impostazione della sicurezza del proxy e un esempio di C++ che Mostra come impostare il nome dell'entità server, vedere [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="cb1a7-111">For more information about setting proxy security and a C++ example showing how to set the server principal name, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="cb1a7-112">Per ulteriori informazioni sull'impostazione del nome dell'entità server in script e Visual Basic, vedere [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) e [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="cb1a7-112">For more information about setting the server principal name in script and Visual Basic, see [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) and [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="cb1a7-113">Diversamente dalla maggior parte dei protocolli di sicurezza per Strumentazione gestione Windows (WMI) e Component Object Model (COM), non è possibile impostare l'entità server in una chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="cb1a7-113">Unlike most security protocols for Windows Management Instrumentation (WMI) and Component Object Model (COM), you cannot set the server principal in a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="cb1a7-114">Tuttavia, è possibile impostare l'entità server con il parametro *bstrAuthority* per [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)o il parametro *pServerPrincName* per [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="cb1a7-114">However, you can set the server principal with the *bstrAuthority* parameter for [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), or the *pServerPrincName* parameter for [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="cb1a7-115">Per eseguire correttamente la compilazione, l'esempio di codice in questo argomento richiede la seguente \# istruzione include.</span><span class="sxs-lookup"><span data-stu-id="cb1a7-115">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="cb1a7-116">Nell'esempio di codice seguente viene illustrato come impostare il nome dell'entità server con [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="cb1a7-116">The following code example shows how to set the server principal name with [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a><span data-ttu-id="cb1a7-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb1a7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb1a7-118">Impostazione del servizio di autenticazione tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="cb1a7-118">Setting the Authentication Service Using VBScript</span></span>](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="cb1a7-119">Impostazione dell'autenticazione mediante C++</span><span class="sxs-lookup"><span data-stu-id="cb1a7-119">Setting Authentication Using C++</span></span>](setting-authentication-using-c-.md)
</dt> <dt>

[<span data-ttu-id="cb1a7-120">Impostazione della sicurezza in IWbemServices e in altri proxy</span><span class="sxs-lookup"><span data-stu-id="cb1a7-120">Setting the Security on IWbemServices and Other Proxies</span></span>](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
